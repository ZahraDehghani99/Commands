In this page we should learn about finda and replace option in vscode. In the beginning we should press `ctrl` + `F` in vscode and then follow these instructions.


## Delete lines start with specific words
For this goal, we should enable regex search in find box using `.*` button.Then write this command:

```
^.*(word1|word2).*\n?
```
above command find your desired lines, to delete them you should first press `alt` + `enter` to select those lines and then delete them using 'del'.


## Find everything between ""
you should write this command in the find box:

```
(["'])(?:(?=(\\?))\2.)*?\1
```
