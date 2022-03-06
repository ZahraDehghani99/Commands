# Linux
Here I gathered some of important commands in linux.

## Version of ubuntu
```
lsb_release -a
```

## Connecting to SSH Over LAN 
when you want to connect to another ubuntu system from your ubuntu system you should install openssh-server (in this [link](https://linuxize.com/post/how-to-enable-ssh-on-ubuntu-18-04/) you can see this process)then run the following command:
```
ssh username@ip_address
```

## Copy file to another ubuntu system Using SCP
SCP or secure copy is a means of securley transferring files between two machines on a network. 
```
scp [path to source file] [user_name@remote_host]:[path to destination file]
```

## Check status of a program

```
systemctl status <program_name>
```
If the status of the program is not activate, run the following command for activating it:
```
systemctl start <program_name>
```

## History of terminal
If you want to see the history of commands you run in terminal you should run this command:
```
history
```
If you want to see the commads you run with keyboad for example `docker`, you should run this commad:
```
history |grep docker
```

## Kill the process on specific port
```
sudo kill -9 $(sudo lsof -t -i:<port>)
```

## Setting DNS
If you can't access to internet, then you should configure your dns as follows:
```
sudo nano /etc/resolv.conf
```
and then add `nameserver 8.8.8.8` to this file.

## List Direcotriy with volumes
```
ls -sh
```
