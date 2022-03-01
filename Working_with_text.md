# Working with text on Terminal
Here I gathered some of important commands in linux for working with text.
useful link: https://www.maketecheasier.com/working-with-text-on-linux-command-line/

## cat
you can display content of a single file using `cat`.
```
cat <file_name>
```

## wc
prints the number of bytes, lines, words or characters in a file.
```
wc --bytes <file_name> # or wc --byte
wc -l <file_name> # or wc --lines <file_name>
wc -w <file_name>
wc --chars <file_name>
```
## Split
You can use `split` to divide a file into smaller files, by number of lines, by size, or to a specific number of files.
### Splitting by number of lines
```
split -l num_lines input_file output_prefix
```

### Splitting by bytes
```
split -b bytes input_file output_prefix
```

### Splitting to a specific number of files
```
split -n num_files input_file output_prefix
```

## head
Display `n` first lines of a file using `head`.
```
head -n <file_name>
```
## sed
```
sed s/pattern/replacement/g filename
```
To modify the original file instead, you can use the `-i` flag.
