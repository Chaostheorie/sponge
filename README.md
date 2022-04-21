# Sponge — Slurping your pipes

Sponge is a simple python tool for reading from stdin and writing the collected input to a file. It was inspired by [moreutils sponge](https://www.putorius.net/moreutils.html) but rewritten for my personal use as a portable python script. This version of sponge also features the ability to buffer stdin data in a tmp file on disk and later on write in chunks to the destination file for large amounts of data.

The intended use case is for oneliners in POSIX shells: `grep pattern data.txt | sponge data.txt`. Since alternative solutions like `grep pattern data.txt > data.txt` will not work or require writing results in a separate file.

## Usage

`sponge -h`:

```
Usage: sponge [OPTION]... [FILE]
Read full stdin input (until EOF) and write to FILE
  -h, --help               Print this help message
  -t                       Buffer stdin output in tmp file before writing
  -e                       Read from stderr instead of stdin
```
