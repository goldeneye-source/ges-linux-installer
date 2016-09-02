# install_ges.sh
Installer for the GoldenEye: Source linux server

This does not currently work as the linux server SO file is not publicly available.

##Currently tested disro's
(please let me know if you test any other distros so i can update this)
* ubuntu server 16.04
* Debian 8.5

##Usage

There are a few options for usage.

###First:
=====
```bash
wget https://raw.githubusercontent.com/goldeneye-source/ges-linux-installer/master/install_ges.sh
chmod +x install_ges.sh
sudo ./install_ges.sh
```

Follow the prompts:

* Username:
* Install as Service:
* Server Name:
* Max Players:
* Server Password:
* Rcon Password:
* Server Region:
* Server launch options:
* Install Source Mod:
* Steam ID for Source Mod:

###Second:
=====
Automation

This requires you to pass command line arguments to the script
so if you are using a standard account and need to pass sudo
use `su -c './install.sh commands'`

Current automation commands,

-a : run script in auto mode

* First: -a automated (required)
* Second: user account to use (required)
* Third: your Steam ID (required)
* Fourth: game launch options in "" (NOT required) if left blank default will be used

ex. `su -c './install_ges.sh -a death STEAM:0:0:12345'`  
or. `su -c './install_ges.sh -a death STEAM:0:0:12345 "-game ./gesource/ -console +maxplayers 16 +map ge_archives +exec server.cfg"`

###Third:
=====

Uninstalling server:

`su -c './install_ges.sh -uninstall'`

The script will then promp to verify you want to uninstall the server and it will remove all files added


