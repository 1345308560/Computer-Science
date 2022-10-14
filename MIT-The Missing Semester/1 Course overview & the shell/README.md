# The Shell
2. Create a new directory called missing under /tmp.
``` shell
cd /tmp 
mkdir missing 
cd missing 
```
3. Look up the touch program. The man program is your friend.
```shell
man touch
```
4. Use touch to create a new file called semester in missing.
```shell
touch semester
```
5. Write the following into that file, one line at a time:
```
#!/bin/sh
curl --head --silent https://missing.csail.mit.edu
```
```shell
echo \#\!/bin/sh > semester
echo "curl --head --silent https://missing.csail.mit.edu" >> semester
```
6. Try to execute the file
```shell
./semester
ls -l
```
7. Run the command by explicitly starting the sh interpreter
```shell
sudo apt update
sudo apt install curl
sh ./semester
```
You can open or run .sh file in the terminal on Linux or Unix-like system. The .sh file is nothing but the shell script to install given application or to perform other tasks under Linux and UNIX like operating systems.

8. Look up the chmod program
```shell
man chmod
```
The chmod command is used to change the permissions of a file or directory.

9. Use chmod to make it possible to run the command ./semester rather than having to type sh semester. 
```shell
chmod +rwx ./semester
./semester
```
10. Use | and > to write the “last modified” date output by semester into a file called last-modified.txt in your home directory.
```shell
./semester | grep Date > last-modified.txt
```
11. Write a command that reads out your laptop battery’s power level or your desktop machine’s CPU temperature from /sys.
```shell
Don't have that file.
```