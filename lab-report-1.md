# **Lab Report 1**
## **Basic Filesystem Commands Learned About**
`cd` Using the command with no arguments:
```
marit@doofenshmirtz MINGW64 ~ $ cd
marit@doofenshmirtz MINGW64 ~
```
This output is not an error. I called `cd` while in `/c/Users/marit`. Calling `cd` without any arguments means that you will not move into a different directory. This means I was still in `/c/Users/marit` after calling the `cd` command with no arguments.

---
Using the command with a path to a directory as an argument:
```
marit@doofenshmirtz MINGW64 ~ $ cd lecture1/
marit@doofenshmirtz MINGW64 ~/lecture1 (main) $
```
This output is not an error. I called `cd lecture1/` while in `/c/Users/marit`. I successfully moved to the `lecture1` directory. 

---
Using the command with a path to a file as an argument:
```
marit@doofenshmirtz MINGW64 ~/lecture1 (main) $ cd Hello.java
bash: cd: Hello.java: Not a directory
```

`ls` --- Using the command with no arguments:
```
marit@doofenshmirtz MINGW64 ~/lecture1 (main) $ ls
Hello.class Hello.java messages/ README
marit@doofenshmirtz MINGW64 ~/lecture1 (main) $
```
This output is not an error. The `ls` command used without an argument shows the files and folders under the current directory. Since we were in the `lecture1` directory, the `ls` command showed `Hello.class`, `Hello.java`, `messages/`, and `README`.

---
Using the command with a path to a directory as an argument:
```
marit@doofenshmirtz MINGW64 ~/lecture1 (main) $ ls messages/
en-us.txt  es-mx.txt  zh-cn.txt

marit@doofenshmirtz MINGW64 ~/lecture1 (main) $
```
This output is not an error. The `ls` command can be used with a specified path. In this case, I used the `messages/` path, and the output were the three text files with different languages.

---
Using the command with a path to a file as an argument:
```
marit@doofenshmirtz MINGW64 ~/lecture1 (main) $ ls Hello.java
Hello.java

marit@doofenshmirtz MINGW64 ~/lecture1 (main) $
```
This output is not an error. The `ls` command can be used with a specified file. Because `Hello.java` is a file and has no further files and folders, the output is just a print of the file `Hello.java`.

---
`cat` --- Using the command with no arguments:
```
marit@doofenshmirtz MINGW64 ~/lecture1 (main)
$ cat







marit@doofenshmirtz MINGW64 ~/lecture1 (main)
$
```
This output is an error. `cat` is not meant to be used without at least one argument. Without an argument, the `cat` command will print back the empty space until recieving an end of file signal.

---
Using the command with a path to a directory as an argument:
```
marit@doofenshmirtz MINGW64 ~ $ cat lecture1/
cat: lecture1/: Is a directory

marit@doofenshmirtz MINGW64 ~ $
```
This output is an error. The `cat` command does not take one directory path as arguments. Using the `lecture1` path results in the error because the command does not know what to do with one path.

---
Using the command with a path to a file as an argument:
```
marit@doofenshmirtz MINGW64 ~/lecture1 (main) $ cat README
To use this program:

javac Hello.java
java Hello messages/en-us.txt

marit@doofenshmirtz MINGW64 ~/lecture1 (main) $
```
This output is not an error. The `cat` command reads the contents of the `README` file and prints them to the terminal line by line.
