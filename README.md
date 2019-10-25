# Unix Cookbook

While I am generally very comfortable on the command line without external reference beyond glancing at options in man pages,
there are enough times where I have to go search the internet for a way to do something that seems relatively basic.

This document is my personal collection of useful actions that I am unlikely to memorize.

## Print matching line and all subsequent lines in file

`-n` suppresses the normal output echoing that `sed` does.

```sh
sed -n '/^exact match$/,$p' FILE
```

## Print two files side-by-side

`-w` specifies the total output width.
`-m` indicates to merge multiple files.
`-t` suppresses normal headers and trailers that `pr` sets.

```sh
pr -w 160 -m -t FILE1 FILE2
```
