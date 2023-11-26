# Simple Shell 🐚
![download](https://github.com/therealmahmoud/simple_shell/assets/127629621/233054e1-49c3-480a-8240-2ac1c53a77ce)

## Description

By Spencer Cheng, featuring Julien Barbier Project to be done in teams of 2 people (your team: Mahmoud Magdy Mahmoud, Mohammed Essam)

## Files

| Name | Description |
| ------------------------------ | -------------------------------------------- |
| shell.h | Header file program. |
| main.c | Main function, interactive and non-interactive. |
| new_procees.c | Function that creates a new process. |
| my_cd.c | Change the working directory. |
| my_env.c | Function that prints environment variables. |
| my_exit.c | Exit shell with a given state. |
| my_help.c | Function that prints help (get information about a command) |
| read_line.c | Read a line from stdin. |
| read_stream.c | Read a line from the stream. |
| shell_interactive.c | Run shell interactive mode. |
| shell_no_interactive.c | Run shell non-interactive mode. |
| split_line.c | Split a string into tokens. |
| execute_args.c | Number of builtin functions. |

## List of functions and system calls.

* ```chdir``` (man 2 chdir)
* ```exit``` (man 3 exit)
* ```fork``` (man 2 fork)
* ```free``` (man 3 free)
* ```getline``` (man 3 getline)
* ```isatty``` (man 3 isatty)
* ```malloc``` (man 3 malloc)
* ```perror``` (man 3 perror)
* ```strtok``` (man 3 strtok)
* ```waitpid``` (man 2 waitpid)

## Install

Clone this repo and compile as follow:

> gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh

## Usage

Interactive mode: ```./hsh```

Non-interactive mode: ```echo "/bin/ls" | ./hsh```

### Built-ins

* [x] ```cd```
* [x] ```env```
* [x] ```help```
* [x] ```exit```

### Examples

* **Run shell in interactive mode:**

```
 $ ./hsh
 simple_prompt$ ls -l
 total 72
-rw-r--r-- 1 root root   771 Nov 16 12:01 execute_args.c
-rwxr-xr-x 1 root root 20192 Nov 16 12:31 hsh
-rw-r--r-- 1 root root   307 Nov 16 08:39 main.c
-rw-r--r-- 1 root root   646 Nov 16 11:59 new_process.c
-rw-r--r-- 1 root root   384 Nov 16 12:28 own_cd.c
-rw-r--r-- 1 root root   338 Nov 16 12:28 own_env.c
-rw-r--r-- 1 root root   284 Nov 16 12:29 own_exit.c
-rw-r--r-- 1 root root   591 Nov 16 12:31 own_help.c
-rw-r--r-- 1 root root   590 Nov 16 09:13 read_line.c
-rw-r--r-- 1 root root   815 Nov 16 12:26 read_stream.c
-rw-r--r-- 1 root root   677 Nov 16 12:27 shell.h
-rw-r--r-- 1 root root   516 Nov 16 08:38 shell_interactive.c
-rw-r--r-- 1 root root   442 Nov 16 12:07 shell_no_interactive.c
-rw-r--r-- 1 root root   848 Nov 16 09:35 split_line.c
```
```
 $ /hsh
 simple_prompt$ echo “Hello, World!”
 “Hello, World!”
```
* **Run shell in non-interactive mode:**

```
 $ echo "/bin/ls" | ./hsh
 execute_args.c  new_process.c  own_exit.c   read_stream.c        shell_no_interactive.c
hsh             own_cd.c       own_help.c   shell.h              split_line.c
main.c          own_env.c      read_line.c  shell_interactive.c
```
