## Add a User mit predefinied UID, SHELL and HOME_DIRECTORY

````
sudo useradd -m -d /home/mirmiray  -s /bin/bash -u 1453 miray

````

![users1](images/users1.png)

----
## How to delete a user with its home directory

_"userdell" command with "-r" option dletes home directory._

````
sudo userdel -r <userName>
````

![users1](images/users2.png)

----

## How to create a user specifiying a primary/secondary Group


````
sudo useradd  -g printadmin  -G docker kamil 
````

![users1](images/users3.png)

----

## How to change the Primary Group of a Useer


````
sudo groupadd kamil

sudo  usermod -g kamil kamil

id kamil
````

![users4](images/users4.png)

----