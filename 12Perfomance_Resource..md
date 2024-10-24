### improve performance , how we can safely to set limit of precess for the suoeruser root to be unlimited.

to see all ts set for root 
````
ulimit -a
````
![ulimit](images/ulimit.png)


to see maximum user processes alowed-
````
ulimit -u
````
![ulimit1](images/ulimit1.png)

to change ulimit tu unlimited
````
ulimit -u unlimited
````

 to change ulimitback to default 
````
ulimit -u 14269
````
![ulimit2](images/ulimit1.png)

### Where can you set the resources limits fot users logged in via PAM?
For any user logged in , thereis a file that we can look into, and set the user limit.
 We did it by typing ulimit command , but  we do it for any user through configuration file. 
 ***/etc/security/limits.conf*** 

````
nano /etc/security/limits.conf
````


### How to check mit for a user.
*** ulimit -a *** checks for a user. 

-----
### How to check and increase the limit of opened files in Linux? 
This is a system-wide setting. 
Check the limit of open file in linux or maximum files we can open in linux fpr everyone.
````
cat /proc/sys/fs/file-max
````
![perf1](images/perf1.png)


how to increase/change limit
````
vi /etc/sysctl.conf
````
and add line 
````
fs.file-max-98321
grep 98321 /etc/sysctl.conf
````
![perf2](images/perf2.png)

the line is added 
to take effect
````
sysctl -p
cat /proc/sys/fs/file-max
````


### How to view run time kernel Parameters?

````
sysctl -a
````

![perf3](images/perf3.png)

### How to change runtime kernel parameters for maximal shared segment size in bytes? 

````
sysctl -a |
nano /etc/sysctl.conf
--> kernel.shmmax = 18446744073692774399
sysctl -p

````

![perf4](images/perf4.png)

### How to view Boot time parameters and which file is modified to change these parameters?

````
cat /proc/cmdline
````
![perf5](images/perf5.png)

_these are the boot time parameters. So when the system is booting, this is what you get on the screen.
And yes, you can edit those and you can modify those, but you cannot go and modify those in this file.
The way to modify those actually these are supplied or the system gets these from grub.cfg file, which
is for which is Grub2 on rheL seven we're using._


````
cat /boot/grub2/grub.cfg
````
![perf6](images/perf6.png)
_This is where the boot time parameters are, which we can control.
So if you make change, make if you want to make any changes to boot time parameters, this is where
you will come and do it._

