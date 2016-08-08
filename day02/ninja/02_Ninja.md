# 02 Ninja

> Ninja: replace_with_your_name

[TOC]

## Practice

> Resources files have been included in src directory

``` shell
src/
├── data
│   ├── NC-EST2015-AGESEX-RES.csv
│   └── grades.csv
└── drama
    └── midsummer_nights_dream.html

2 directories, 3 files
```

### Echo and redirect

> 1. Use `echo` and redirect `>` or `>>` to create a file which contains the following content
> 2. Use `cat` to check if the result is correct

``` shell
Hello World
The quick brown fox jumps over the lazy dog
A journey of a thousand miles begins with a single step
```

``` shell
peter@peter-VirtualBox:~/workspace/a$ echo "Hello World" > Hello
peter@peter-VirtualBox:~/workspace/a$ echo "The quick brown fox jumps the lazy dog" >> Hello 
peter@peter-VirtualBox:~/workspace/a$ echo "A journay of a thousand miles begins with a single step" >> Hello\ World 
peter@peter-VirtualBox:~/workspace/a$ cat Hello 
Hello World
The quick brown fox jumps the lazy dog
A journay of a thousand miles begins with a single step
```

### Midsummer nights dream

> Everything can be regarded as data
>
> The play script has been stored in `linux-essentials/day02/` directory with suffix `.html`, if you don't see it, use `find` to find it.
>
> After you find the file, use `grep` to find:
>
> * Line numbers of the character `QUINCE`'s dialog.
> * (Hint: use option `-n` to display line numbers)

``` shell
peter@peter-VirtualBox:~/workspace/linux-essentials/day02/src/drama$ grep -n QUINCE midsummer_nights_dream.html 
484:<h3>SCENE II. Athens. QUINCE'S house.</h3>
486:<i>Enter QUINCE, SNUG, BOTTOM, FLUTE, SNOUT, and STARVELING</i>
489:<A NAME=speech1><b>QUINCE</b></a>
500:<A NAME=speech3><b>QUINCE</b></a>
515:<A NAME=speech5><b>QUINCE</b></a>
528:<A NAME=speech7><b>QUINCE</b></a>
538:<A NAME=speech9><b>QUINCE</b></a>
548:<A NAME=speech11><b>QUINCE</b></a>
574:<A NAME=speech13><b>QUINCE</b></a>
584:<A NAME=speech15><b>QUINCE</b></a>
594:<A NAME=speech17><b>QUINCE</b></a>
604:<A NAME=speech19><b>QUINCE</b></a>
618:<A NAME=speech21><b>QUINCE</b></a>
628:<A NAME=speech23><b>QUINCE</b></a>
638:<A NAME=speech25><b>QUINCE</b></a>
649:<A NAME=speech27><b>QUINCE</b></a>
662:<A NAME=speech29><b>QUINCE</b></a>
675:<A NAME=speech31><b>QUINCE</b></a>
697:<A NAME=speech34><b>QUINCE</b></a>
711:<A NAME=speech36><b>QUINCE</b></a>
724:<A NAME=speech38><b>QUINCE</b></a>
744:<A NAME=speech40><b>QUINCE</b></a>
1464:<i>Enter QUINCE, SNUG, BOTTOM, FLUTE, SNOUT, and STARVELING</i>
1472:<A NAME=speech2><b>QUINCE</b></a>
1485:<A NAME=speech4><b>QUINCE</b></a>
1519:<A NAME=speech9><b>QUINCE</b></a>
1568:<A NAME=speech16><b>QUINCE</b></a>
1586:<A NAME=speech19><b>QUINCE</b></a>
1598:<A NAME=speech21><b>QUINCE</b></a>
1622:<A NAME=speech24><b>QUINCE</b></a>
1640:<A NAME=speech26><b>QUINCE</b></a>
1650:<A NAME=speech28><b>QUINCE</b></a>
1675:<A NAME=speech32><b>QUINCE</b></a>
1690:<A NAME=speech34><b>QUINCE</b></a>
1710:<A NAME=speech37><b>QUINCE</b></a>
1714:<p><i>Exeunt QUINCE, SNUG, FLUTE, SNOUT, and STARVELING</i></p>
1745:<p><i>Re-enter QUINCE</i></p>
1748:<A NAME=speech42><b>QUINCE</b></a>
3353:<h3>SCENE II. Athens. QUINCE'S house.</h3>
3355:<i>Enter QUINCE, FLUTE, SNOUT, and STARVELING</i>
3358:<A NAME=speech1><b>QUINCE</b></a>
3375:<A NAME=speech4><b>QUINCE</b></a>
3387:<A NAME=speech6><b>QUINCE</b></a>
3424:<A NAME=speech11><b>QUINCE</b></a>
3436:<A NAME=speech13><b>QUINCE</b></a>
3669:<p><i>Enter QUINCE for the Prologue</i></p>
```

### Look into the data

> [Population estimates of America](http://www.census.gov/popest/data/datasets.html) data has been put into `linux-essentials/day02/src/data/`, file name `NC-EST2015-AGESEX-RES.csv`. Let's look into the data:

``` shell
# How many lines in this file?
  307
# Which fields (headers) are presented in this data file?
SEX,AGE,CENSUS2010POP,ESTIMATESBASE2010,POPESTIMATE2010,POPESTIMATE2011,POPESTIMATE2012,POPESTIMATE2013,POPESTIMATE2014,POPESTIMATE2015
# How many types of SEX do you see in the data?
# 3
# How many lines of SEX=2 in the data? (Hint: use grep with pattern: ^2, )
    102
# What's the POPESTIMATE2015 value of AGE=25 for different SEX? (Hint: think about the pattern before grep)
# Your answers:
```
SEX=0 4729564; SEX=1 2407515; SEX=2 2322049 
``` shell
# paste your command and output here.
# if the output is too long, don't paste all, use ... ... instead.
```

## Challenge

### Find the difference

> In this section, you are going to learn a new command `diff` which will help you to find the difference between files. Like `cp`, use `diff` is easy:

``` shell
$ diff file1 file2 # compare difference between file1 and file2
```

**Example**

``` shell
$ cat fruits1 # what inside file fruits1
apple
banana
peach
$ cat fruits2 # what inside file fruits2
appppple
banana
blueberry
peachd
$ diff fruits1 fruits2 # find difference between fruits1 and fruits2
1c1 # there is difference between 1 line in first file, 1 line in second file
< apple # what in first file
---
> appppple # what in second file
3c3,4 # there is difference between 3 line in first file, 3-4 line in second file
< peach # what in first file
---
> blueberry # what in second file
> peachd
```

> Try to create two files like above and and use `diff` to find the difference
>
> Note: if `diff` output nothing, it means content of two files are the same.

**Test symbolic link**

> Remember the concept about symbolic link. Assume we have two symbolic links `a` and `b` point to the same file `1`. Either writing to `a` or `b` will result in modifying the same file.


> 1. Create a file contains only `hello` called `a`
> 2. Create a soft symbolic link file `b` linking to `a` use `ln -s`
> 3. Create a copy of `a` and name it as `c` use `cp`
> 4. Use `diff` to see if there is any difference between `a` and `b`
> 5. Use `diff` to see if there is any difference between `a` and `c`
> 6. Write `world to c` to `c` use `echo`
> 7. Use `diff` to see if there is any difference between `a` and `c`
> 8. Write `world to b` to `b` use `echo`
> 9. Use `diff` to see if there is any difference between `a` and `b`
> 10. Find something?

``` shell
peter@peter-VirtualBox:~/workspace/a$ echo hello > a
peter@peter-VirtualBox:~/workspace/a$ ls
a  b  hello1.txt  hello2.txt  hello.txt
peter@peter-VirtualBox:~/workspace/a$ cat a
hello
peter@peter-VirtualBox:~/workspace/a$ ln -s a b
peter@peter-VirtualBox:~/workspace/a$ ls
a  b  hello1.txt  hello2.txt  hello.txt
peter@peter-VirtualBox:~/workspace/a$ cp a c
peter@peter-VirtualBox:~/workspace/a$ ls
a  b  c  hello1.txt  hello2.txt  hello.txt
peter@peter-VirtualBox:~/workspace/a$ diff a b
peter@peter-VirtualBox:~/workspace/a$ diff a c
peter@peter-VirtualBox:~/workspace/a$ echo "world to c" > c 
peter@peter-VirtualBox:~/workspace/a$ diff a c
1c1
< hello
---
> world to c
peter@peter-VirtualBox:~/workspace/a$ echo "world to b" > b
peter@peter-VirtualBox:~/workspace/a$ diff a b
```

### Powerful Pipeline

> Use `history` , `grep` and `wc` to find out how many `cd` command you have used in history
>
> Only ONE SINGLE command line is enough

``` shell
peter@peter-VirtualBox:~/workspace/a$ history | grep cd | wc
    172     564    4692
```
