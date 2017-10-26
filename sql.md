# Download and install
Download the latest mysql community server from https://dev.mysql.com/downloads/mysql

Install by double clicking the `.dmg` file downloaded via installer

MySql Installer will generate a temporary password for user 'root'
> **Note:** Save this password

# Start/stop/restart MySql server
``` bash
$ sudo /usr/local/mysql/support-files/mysql.server start
$ sudo /usr/local/mysql/support-files/mysql.server stop
$ sudo /usr/local/mysql/support-files/mysql.server restart
```
# Run
Run the following command in your terminal
``` bash
$ /usr/local/mysql/bin/mysql -u root -p
```
or

add this to your .bash_profile
> export PATH=$PATH:/usr/local/mysql/bin

and run by typing the following
```bash
$ mysql -u root -p
```
or

simply create as alias in your .bash_profile
> alias sql='/usr/local/mysql/bin/mysql -u root -p'

and run by
```bash
$ sql
```
---
In either case you will be asked to enter the password. Enter the password you saved while installing MySql.

### Create .bash_profile
Create .bash_profile in your home directory if you don't have with the following command
```bash
$ cd ~
$ touch .bash_profile
```
Open in your favourite text editor by
```bash
$ open .bash_profile -a Sublime\ Text
```
Once required changes are made,  set source to .bash_profile
```bash
$ source .bash_profile
```

# Change password
In MySql client, run the following command
```mysql
mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY 'newPassword';
```
# Add MyCLI
MyCLI is a command line interface for MySQL with auto-completion and syntax highlighting.
To know more about MyCLI click [here](https://www.mycli.net).

## Prerequisite
#### Command line tools
Install command line tools by
```bash
$ xcode-select --install
```
## Install

### With pip
In your home directory run the following
```bash
$ sudo -H easy_install pip
```
followed by
```bash
$ sudo pip install -U mycli
```
or

### With home brew
Install brew by
```bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
followed by
```bash
$ brew update && brew install mycli
```

## Run
Once installed, run by
```bash
$ mycli -h localhost -u root
```

## Configure mycli
Configuration file for mycli is `.myclirc` in your home directory. You can customize this file to have your own interface.
Read full documentation [here](https://www.mycli.net/config).
