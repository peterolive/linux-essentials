# 01 Ninja

> Ninja: replace_with_your_name

[TOC]

## Practice

### Who are you

> Ninja, in this section, you are going to find out the ultimate life questions.
>
> * Who are you? (user name)
> * Where are you? (host name of the machine)
> * Which system are you in? (system information)
> * When is it now?
>
> To answer this questions, you are going to use the following command to help you.
>
> To paste output results, remember `CMD+C` or `CTRL+C` do not work in terminal, you have to right click and choose `copy`.

``` shell
$ whoami
peter
$ hostname
peter-VirtualBox
$ uname
Linux
$ uname -a
Linux peter-VirtualBox 4.4.0-31-generic #50-Ubuntu SMP Wed Jul 13 00:07:12 UTC 2016 x86_64 x86_64 x86_64 GNU/Linux
$ date
Thu Jul 28 20:37:33 CDT 2016
```

### Moving, jumping, flying

> As a ninja, you have to move very fast. In this section you are going to practice moving swiftly around directories, that is
>
> * Try to choose a good path that helps you move fast
> * Use `tab` trick for auto completion
>
> To move fast, certain commands can be useful: `cd\pwd\ls`
>
> Following are simple instructions to move around, but you are free to go anywhere
>
> 1. go to `/usr/local/lib/python2.7/dist-packages/`
> 2. check your location
> 3. go back to home `~`
> 4. check your location
> 5. go to `/etc/kernel/postinst.d/`
> 6. list details of the files in current location
> 7. jump anywhere you want to master the commands

``` shell
# paste your command and output, if output is to long, just put three lines and '# ... ...' behind
# for example
$ cd ../../etc
$ pwd
/etc
$ ls
acpi                    hosts                    profile
adduser.conf            hosts.allow              profile.d
alternatives            hosts.deny               protocols
# ... ...
```
peter@peter-VirtualBox:~$ cd '/usr/local/lib/python2.7/dist-packages/'
peter@peter-VirtualBox:/usr/local/lib/python2.7/dist-packages$ pwd
/usr/local/lib/python2.7/dist-packages
peter@peter-VirtualBox:/usr/local/lib/python2.7/dist-packages$ cd
peter@peter-VirtualBox:~$ pwd
/home/peter
peter@peter-VirtualBox:~$ 
peter@peter-VirtualBox:~$ cd '/etc/kernel/postinst.d/'
peter@peter-VirtualBox:/etc/kernel/postinst.d$ ls -l
total 20
-rwxr-xr-x 1 root root 2704 Apr 14 02:45 apt-auto-removal
-rwxr-xr-x 1 root root  858 Feb 17  2014 initramfs-tools
-rwxr-xr-x 1 root root  196 Feb 15 03:26 pm-utils
-rwxr-xr-x 1 root root   73 Feb 18 16:19 unattended-upgrades
lrwxrwxrwx 1 root root   49 Jul 11 10:50 update-notifier -> /usr/share/update-notifier/notify-reboot-required
-rwxr-xr-x 1 root root  646 Mar 15 13:08 zz-update-grub

``` shell
# paste your command and output here
```

### Building your backpacks

> Ninja, you are about to make your first travel, you need to put things in your backpacks. Remember, make things in order is always a good habit to keep.
>
> In this section, you are going to create directories that simulate the backpacks and categories and items. You want to create something has the same structure as the following directories.

``` shell
backpack/
├── backup_wallet
│   ├── cash
│   ├── credit_cards
│   └── id
├── lunchbox
│   ├── level1
│   │   └── fish_and_meat
│   ├── level2
│   │   └── rice
│   └── level3
│       └── soup
├── mainspace
│   ├── books
│   ├── iphone
│   ├── kindle
│   ├── plasticbag
│   │   └── cloth
│   └── umbrella
├── secretspace
│   ├── cash001
│   ├── cash002
│   ├── cash003
│   └── paperwarraper
│       └── million_check
└── wallet
    ├── cash
    ├── credit_cards
    └── id

10 directories, 18 files
```

> Be smart, try to use as minimum command lines as you can.

``` shell
# paste your command and output here
```
peter@peter-VirtualBox:~$ cd backpack
peter@peter-VirtualBox:~/backpack$ mkdir backup_wallet luchbox mainspace secretspace wallet
peter@peter-VirtualBox:~/backpack$ ls
backup_wallet  luchbox  mainspace  secretspace  wallet
peter@peter-VirtualBox:~/backpack$ cd backup_wallet
peter@peter-VirtualBox:~/backpack/backup_wallet$ touch cash credit_cards id
peter@peter-VirtualBox:~/backpack/backup_wallet$ ls
cash  credit_cards  id
peter@peter-VirtualBox:~/backpack/backup_wallet$ cd ./
peter@peter-VirtualBox:~/backpack/backup_wallet$ cd ../
peter@peter-VirtualBox:~/backpack$ cd lunchbox
bash: cd: lunchbox: No such file or directory
peter@peter-VirtualBox:~/backpack$ mv luchbox lunchbox
peter@peter-VirtualBox:~/backpack$ ls
backup_wallet  lunchbox  mainspace  secretspace  wallet
peter@peter-VirtualBox:~/backpack$ cd lunchbox
peter@peter-VirtualBox:~/backpack/lunchbox$ mkdir level1 level2 level3
peter@peter-VirtualBox:~/backpack/lunchbox$ touch level1/fish_and meat level2/rice level3/soup
peter@peter-VirtualBox:~/backpack/lunchbox$ ls -r
meat  level3  level2  level1
peter@peter-VirtualBox:~/backpack/lunchbox$ rm meat
peter@peter-VirtualBox:~/backpack/lunchbox$ ls
level1  level2  level3
peter@peter-VirtualBox:~/backpack/lunchbox$ touch level1/fish_and_ meat level2/rice level3/soup
peter@peter-VirtualBox:~/backpack/lunchbox$ ls -r
meat  level3  level2  level1
peter@peter-VirtualBox:~/backpack/lunchbox$ cd level1
peter@peter-VirtualBox:~/backpack/lunchbox/level1$ ls
fish_and  fish_and_
peter@peter-VirtualBox:~/backpack/lunchbox/level1$ rm -rf
peter@peter-VirtualBox:~/backpack/lunchbox/level1$ ls
fish_and  fish_and_
peter@peter-VirtualBox:~/backpack/lunchbox/level1$ rm -rf
peter@peter-VirtualBox:~/backpack/lunchbox/level1$ ls
fish_and  fish_and_
peter@peter-VirtualBox:~/backpack/lunchbox/level1$ rm -rf *
peter@peter-VirtualBox:~/backpack/lunchbox/level1$ cd ../
peter@peter-VirtualBox:~/backpack/lunchbox$ touch level1/fish_and_meat level2/rice level3/soup
peter@peter-VirtualBox:~/backpack/lunchbox$ cd ../
peter@peter-VirtualBox:~/backpack$ cd lunchbox/
peter@peter-VirtualBox:~/backpack/lunchbox$ cd ../mainspace
peter@peter-VirtualBox:~/backpack/mainspace$ cd ../../mainspace
bash: cd: ../../mainspace: No such file or directory
peter@peter-VirtualBox:~/backpack/mainspace$ cd ../../etc
bash: cd: ../../etc: No such file or directory
peter@peter-VirtualBox:~/backpack/mainspace$ cd ../
peter@peter-VirtualBox:~/backpack$ touch mainspace/books iphone
peter@peter-VirtualBox:~/backpack$ ls
backup_wallet  iphone  lunchbox  mainspace  secretspace  wallet
peter@peter-VirtualBox:~/backpack$ rm iphone
peter@peter-VirtualBox:~/backpack$ cd mainspace
peter@peter-VirtualBox:~/backpack/mainspace$ touch books iphone kindle umbrella
peter@peter-VirtualBox:~/backpack/mainspace$ mk platicbag
mk: command not found
peter@peter-VirtualBox:~/backpack/mainspace$ mkdir plasticbag
peter@peter-VirtualBox:~/backpack/mainspace$ touch plasticbag/cloth
peter@peter-VirtualBox:~/backpack/mainspace$ ls -R
.:
books  iphone  kindle  plasticbag  umbrella

./plasticbag:
cloth
peter@peter-VirtualBox:~/backpack/mainspace$ cd ../ secretspace
peter@peter-VirtualBox:~/backpack$ cd ../secretspace
bash: cd: ../secretspace: No such file or directory
peter@peter-VirtualBox:~/backpack$ cd secretspace
peter@peter-VirtualBox:~/backpack/secretspace$ cd ../
peter@peter-VirtualBox:~/backpack$ touch secretspace/cash001
peter@peter-VirtualBox:~/backpack$ cp secretspace/cash001 cash002 cash003
cp: target 'cash003' is not a directory
peter@peter-VirtualBox:~/backpack$ cp secretspace/cash001 cash002
peter@peter-VirtualBox:~/backpack$ cd secretspace
peter@peter-VirtualBox:~/backpack/secretspace$ ls
cash001
peter@peter-VirtualBox:~/backpack/secretspace$ ls -R
.:
cash001
peter@peter-VirtualBox:~/backpack/secretspace$ cp secretspace/cash001 secretspace/cash002
cp: cannot stat 'secretspace/cash001': No such file or directory
peter@peter-VirtualBox:~/backpack/secretspace$ cp cash001 cash002
peter@peter-VirtualBox:~/backpack/secretspace$ ls
cash001  cash002
peter@peter-VirtualBox:~/backpack/secretspace$ cp cash001 cash003
peter@peter-VirtualBox:~/backpack/secretspace$ ls
cash001  cash002  cash003
peter@peter-VirtualBox:~/backpack/secretspace$ mkdir paperwarrper
peter@peter-VirtualBox:~/backpack/secretspace$ touch paperwarrper/million_check
peter@peter-VirtualBox:~/backpack/secretspace$ ls -R
.:
cash001  cash002  cash003  paperwarrper

./paperwarrper:
million_check
peter@peter-VirtualBox:~/backpack/secretspace$ touch ../wallet/cash
peter@peter-VirtualBox:~/backpack/secretspace$ cd
peter@peter-VirtualBox:~$ ls -R
.:
a  backpack  Desktop  Documents  Downloads  examples.desktop  Music  Pictures  Public  Templates  Videos  workspace

./a:
b

./a/b:
c

./a/b/c:
d

./a/b/c/d:
e

./a/b/c/d/e:

./backpack:
backup_wallet  cash002  lunchbox  mainspace  secretspace  wallet

./backpack/backup_wallet:
cash  credit_cards  id

./backpack/lunchbox:
level1  level2  level3

./backpack/lunchbox/level1:
fish_and_meat

./backpack/lunchbox/level2:
rice

./backpack/lunchbox/level3:
soup

./backpack/mainspace:
books  iphone  kindle  plasticbag  umbrella

./backpack/mainspace/plasticbag:
cloth

./backpack/secretspace:
cash001  cash002  cash003  paperwarrper

./backpack/secretspace/paperwarrper:
million_check

./backpack/wallet:
cash

./Desktop:

./Documents:

./Downloads:

./Music:

./Pictures:

./Public:

./Templates:

./Videos:

./workspace:
a  b  linux-essentials

./workspace/a:
b  hello.txt

./workspace/a/b:

./workspace/b:
a

./workspace/b/a:
b  hello.txt

./workspace/b/a/b:

./workspace/linux-essentials:
day01  day02  LICENSE  README.md

./workspace/linux-essentials/day01:
ninja  note

./workspace/linux-essentials/day01/ninja:
01_Ninja.md

./workspace/linux-essentials/day01/note:
01_Linux_And_Command_Line_Introduction.md

./workspace/linux-essentials/day02:
ninja  note  src

./workspace/linux-essentials/day02/ninja:
02_Ninja.md

./workspace/linux-essentials/day02/note:
02_File_Operations_And_Permission_System.md

./workspace/linux-essentials/day02/src:
add.py  data  drama

./workspace/linux-essentials/day02/src/data:
grades.csv  NC-EST2015-AGESEX-RES.csv

./workspace/linux-essentials/day02/src/drama:
midsummer_nights_dream.html
peter@peter-VirtualBox:~$ touch ../wallet credit_cards
touch: cannot touch '../wallet': Permission denied
peter@peter-VirtualBox:~$ touch ../../wallet credit_cards
touch: cannot touch '../../wallet': Permission denied
peter@peter-VirtualBox:~$ cd backpack
peter@peter-VirtualBox:~/backpack$ touch ../wallet credit_cards
peter@peter-VirtualBox:~/backpack$ touch ../wallet credit_cards1 id
peter@peter-VirtualBox:~/backpack$ ls -R
.:
backup_wallet  cash002  credit_cards  credit_cards1  id  lunchbox  mainspace  secretspace  wallet

./backup_wallet:
cash  credit_cards  id

./lunchbox:
level1  level2  level3

./lunchbox/level1:
fish_and_meat

./lunchbox/level2:
rice

./lunchbox/level3:
soup

./mainspace:
books  iphone  kindle  plasticbag  umbrella

./mainspace/plasticbag:
cloth

./secretspace:
cash001  cash002  cash003  paperwarrper

./secretspace/paperwarrper:
million_check

./wallet:
cash
peter@peter-VirtualBox:~/backpack$ touch ./wallet credit_cards
peter@peter-VirtualBox:~/backpack$ ls -R
.:
backup_wallet  cash002  credit_cards  credit_cards1  id  lunchbox  mainspace  secretspace  wallet

./backup_wallet:
cash  credit_cards  id

./lunchbox:
level1  level2  level3

./lunchbox/level1:
fish_and_meat

./lunchbox/level2:
rice

./lunchbox/level3:
soup

./mainspace:
books  iphone  kindle  plasticbag  umbrella

./mainspace/plasticbag:
cloth

./secretspace:
cash001  cash002  cash003  paperwarrper

./secretspace/paperwarrper:
million_check

./wallet:
cash
peter@peter-VirtualBox:~/backpack$ touch ../wallet/credit_cards
touch: cannot touch '../wallet/credit_cards': Not a directory
peter@peter-VirtualBox:~/backpack$ touch ./wallet/credit_cards
peter@peter-VirtualBox:~/backpack$ cd wallet
peter@peter-VirtualBox:~/backpack/wallet$ ls
cash  credit_cards
peter@peter-VirtualBox:~/backpack/wallet$ touch id
peter@peter-VirtualBox:~/backpack/wallet$ ls
cash  credit_cards  id

### Remove items

> There is no need to take the cashes in the secretspace since you already have backup wallet, so remove all the cashes in secretspace.
>
> Someone said he would like to treat you for lunch when you visit, so there is no need to take the heavy lunchbox with you. Remove the lunchbox from your backpack.

``` shell
# paste your command and output here
```

## Challenge

### Myth of hidden files

> In Linux kingdom, everything is file. However there are some files are not easy to be seen, there are called `hidden` files. It's a convention that hidden files are named begin with a dot `.`. Your task in this section is to find out all the hidden files in home `~` directory.
>
> There is a option for `ls` command to list all hidden files, find it out and use it for finding hidden files. (Tip: try `ls --help`)

``` shell
# paste your command and output here
```
