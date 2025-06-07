# Linux
Here I gathered some of important commands in linux.

# General Commands
## Remove a file
```
rm file
```

## Remove a directory
```
rm -r folder
```

## Change directory
```
cd folder
```

## Go back to previous folder in directory
```
cd ..
```


## Version of ubuntu
```
lsb_release -a
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
## Determine size of files and directories
du (abbreviated from disk usage
```
du -h [file or foler name]
```
or
```
du -sh [file or foler name]
```

## See CPU config
```
lscpu
```

## See information about the RAM
```
free -h
```

# Server Related Commands
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

## Copy file from server to local system
First go the desired directory you want your file or folder transfer to it, then type this command:
This code transfer a folder to my local system:
```
ssh root@172.25.5.17 'cd /root  && tar -czf - [folder you want to transfer]' > server_crawler.tar.gz

```

and then this command to extract it:
```
tar -xzf server_crawler.tar.gz
```

## Run the Code with `nohup`
nohup : not hang up


```
nohup python script.py > output.log 2>&1 &
```

nohup: Prevents the process from terminating when the SSH session ends.
    
output.log: Redirects stdout (standard output) to output.log.

2>&1: Redirects stderr (errors) to the same log file.

&: Runs the command in the background.

## Check Running Background Jobs
```
jobs -l
```

## View Logs
```
tail -f output.log  # Real-time log monitoring
cat output.log     # View entire log
```


## Graceful Termination
```
kill PID  # Replace PID with the actual number (e.g., `kill 12345`)
```

## Finds any processes that have `run.py` in their command line
```
ps aux | grep run.py
```

## DNS related settings
In some situations that you want to  have access to some pages but you do not you should change the content of one of these files `/etc/resolv.conf` or `/etc/systemd/resolved.conf`. I think, based on your system it may vary that which one you should change.
For example, on my server, I wanted to push my codes to gitlab, but I had not ping on gitlab:
When I enter this command:
```
ping gitlab.[].net
```
I get that 
```
ping: gitlab.apk-group.net: Name or service not known
```
So, after searching the problem I realized that I should add the dns of the company to one of those files. But after adding `nameserver 172.[company ip]` to the `/etc/resolv.conf`, I realized that still I do not have ping. So, I added 
```
[Resolve]
DNS=172.25.5.1
```
to the `/etc/systemd/resolved.conf` and then restart the service using `sudo systemctl restart systemd-resolved`. That fixed the  problem.


## Watch the content of the file
```
cat file_address
```
## Change the content of the file
```
sudo nano file_address
```
Then press `Ctrl + O`, `Enter` for saving changes, and `Ctrl+X` for exit.



