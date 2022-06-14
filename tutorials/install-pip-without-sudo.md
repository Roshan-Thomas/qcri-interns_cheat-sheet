# Install `pip` without sudo access

On the Ubuntu server, to install `pip` you will need to have sudo access, but there is a workaround to install pip without sudo (This will install pip locally only tho, but it will work for all intents and purposes).

## Install `pip` locally

Get the *get-pip.py* file from the web. And install pip for the local user.
```sh
wget https://bootstrap.pypa.io/get-pip.py

python get-pip.py --user
```

Once you have installed pip, you will need to add it to your PATH variables so it can be accessed throughout your user and not only in one particular file.

```sh
nano ~/.bashrc
```

Concate the path of local Python in front of the path variable (This line can be added at the end of the .bashrc file or along with the other PATH variables, if you have any).
```
export PATH=$HOME/.local/bin/:$PATH
```

Reload the script
```sh
source ~/.bashrc
```

After the installation you can install any packages freely without influencing outher users on the same machine. Horray, you now have `pip`!! :tada::tada:

