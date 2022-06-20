# How to run processes in the background (Unix)

May times you will need to run processes in the background for example, you are downloading something and the estimated time is 2 or 3 hours or you are running a script which takes a long time to complete and you cant wait to go home. That is exactly the time you need to put that process in the background, so it can run while you are away from the laptop and even if the terminal session is closed. 

Below are a few methods you can do to run processes in the background.

## 1. Add an Ampersand after your Command

The easiest way to run a Linux background command is to add an Ampersand (&) symbol after the command. For example,

```sh
gedit &
```

This will open the gedit text editor from your terminal and you can immeditely start using the terminal. 

Doing this method will output a number, that is your process ID or PID which is a unique number that signifies your process running the background.

*Note: If you want to kill the process you can write*
```sh
sudo kill -9 process_id 
```

## 2. Send Commands to the Background with `nohup`

The **nohup** command in Linux allows users to run terminal commands that are immune to HUP or Hang Up signals. 

The below example runs an Nmap port scan in the background.

```sh
nohup sudo nmap -sS --top-ports=15 192.168.1.1/24
```

One key benefit of nohup is that your commands will run even if you exit the shell. Moreover, it generates log files of the execution. Look for **nohup.out** in the current directory of inside $HOME.

## Closing Note

Having the ability to run commands in the background makes system management more productive. You can background your tasks in several ways. Bash features like the **&** are convient, but the system will kill the background job when the shell closes. On the other hand, tools like **nohup** keep your command running even when you log out or terminate the shell.

If you leave your programs in the background for a long time, they may become zombie processes if they're not coded properly. These processes can slow down the system significantly. So, make sure to identify and kill zombie processes every once in a while.
