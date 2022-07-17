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

## Remove first space character 
To remove first space character in each line in `inputfile`, and store the modified file in `outputfile`, you should run the following command:
```
sed 's/ //' inputfile >outputfile
```
This applies a substitution to all lines of the file `inputfile` that will substitute the first space character with nothing (i.e. remove it). The output is stored in the file `outputfile`.

## Remove space at the end of each line file
```
sed 's/ *$//' inputfile > outputfile
```

## Calculate the frequency of each word in a text file
```
cat word.txt |tr ' ' '\n'| sort | uniq -c | sort -nr
```
tr ' ' '\n' : transforms ' ' (space) with '\n', it means this command put each word in a separate line
more information : https://wingsoftechnology.com/unix-calculate-frequency-each-word-text-file/

If you want to store the result in a file you should run the following command:
```
cat words.txt | tr -s ‘ ‘ ‘\n’ | sort | uniq -c | sort -r | awk ‘{print $2, $1}’ > result.txt
```
## Convert Large CSV file to TXT file in terminal

use this: (if you don't have dos2unix, you should install it `using sudo apt install dos2unix`)
```
dos2unix source.csv
```
then:
```
cat source.csv > destination.txt
```
