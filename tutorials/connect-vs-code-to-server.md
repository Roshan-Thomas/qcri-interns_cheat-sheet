# How to connect Visual Studio Code (VS Code) to the QCRI server?

## Prerequisites

To get started, you need to have done the following steps:
1. Install Visual Studio Code
2. Have an existing connection to the server (If you dont, ask IT or your supervisor)

## Install the extension

The Remote - SSH extension is used to connect to SSH hosts in VS Code. 

With the extension installed, you will see a new Status bar iterm (green color) at the far left. The Status bar item can quickly show you in which context VS Code is running (local or remote) and clicking on it will bring up the Remote - SSH commands.

## Create an SSH key

If you don't have an SSH key pair, open a bash shell or the command line and type in:
```sh
ssh-keygen -t rsa
```

Click enter for all the questions `ssh-keygen` asks and it will generate key in the default location (under your user directory as a folder named `.ssh`).

Once the key is generated, you will need to copy the ssh ID to your server. It is as simple as writing one command
```sh
ssh-copy-id 'QCRI\username@ip_address'
```

## Connect using SSH via VS Code

Now that you've created an SSH host, lets connect to it through VS Code!

1. In VS Code, click on the Status bar (green bar on bottom left corner) to bring up a list of Remote extension commands.
2. Choose the **Remote-SSH: Connect to Host** command and connect to the host by entering connection information for your server in the following format 'QCRI\username@ip_address' 
3. VS Code will open a new window (instance). You'll then see a notification that the "VS Code Server" is initalizing on the SSH Host. Once the VS Code Server is installed on the remote host, it can run extensions and talk to your local instance of VS Code.

*Note: You'll know you're connected to your server by looking at the indicator in the Status bar. It shows the hostname of your server (or ip address).*

**You are now all connected to VS Code and can now open folders and edit files just like you would normally :blush:.** 
