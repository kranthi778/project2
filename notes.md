# Part 1 – User Management

## 1. Create a New User

### Command

```bash

sudo useradd testuser

```

### Description

I can create an user account named testuser. This is how I add an user to my system.

### Screenshot

![Alt text](screenshots/useradd.png)

---

## 2. Set a Password for the User

### Command

```bash

sudo passwd testuser

```

### Description

I need to set a password for testuser. This is how I set or change the password for the testuser user account.

### Screenshot

![Alt text](screenshots/passwd.png)

---

## 3. Modify User Information

### Command

```bash

sudo usermod -c "Test User" testuser

```

### Description

I can. Update the comment, which is the full name for the testuser user account. This is how I modify user information for testuser.

### Screenshot

![Alt text](screenshots/usermod.png)

---

## 4. Check Password Status

### Command

```bash

sudo passwd -S testuser

```

### Description

I want to know the password status of testuser. This command helps me see the password status of the testuser user account.

### Screenshot

![Alt text](screenshots/passwd-status.png)

---

## 5. Display Password Aging Information

### Command

```bash

sudo chage -l testuser

```

### Description

I need to see password aging and account expiration information for testuser. This command shows me the password aging and account expiration information for the testuser user account.

### Screenshot

![Alt text](screenshots/chage-l.png)

---

## 6. View Last Login Information

### Command

```bash

lastlog2

```

### Description

I want to see the login information for all users, including testuser. This command displays the login information for all users.

### Screenshot

![Alt text](screenshots/lastlog2.png)

---

## 7. Lock a User Account

### Command

```bash

sudo passwd -l testuser

```

### Description

Sometimes I need to lock the testuser user account. This command locks the testuser user account.

### Screenshot

![Alt text](screenshots/passwd-lock.png)

---

## 8. Unlock a User Account

### Command

```bash

sudo passwd -u testuser

```

### Description

If I locked the testuser user account I can unlock it using this command. This command unlocks the testuser user account.

### Screenshot

![Alt text](screenshots/passwd-unlock.png)

---

## 9. Delete a User Account

### Command

```bash

sudo userdel testuser

```

### Description

If I do not need the testuser user account anymore I can delete it. This command deletes the testuser user account.

### Screenshot

![Alt text](screenshots/userdel.png)

---

## 10. Delete User and Home Directory

### Command

```bash

sudo userdel -r testuser

```

### Description

I can also delete the testuser user account and its home directory. This command deletes the testuser user account and its home directory.

lt text](screenshots/userdel.png)

---
### Screenshot

![Alt text](screenshots/userdel-r.png)

---
# Conclusion

In this part, I learned how to:

- Create a new user using `useradd`.
- Set a user password using `passwd`.
- Modify user information using `usermod`.
- Check password status using `passwd -S`.
- Display password aging information using `chage`.
- View last login details using `lastlog`.
- Lock a user account using `passwd -l`.
- Unlock a user account using `passwd -u`.
- Delete a user using `userdel`.
- Delete a user and its home directory using `userdel -r`.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


# Part 2 – Group Management

## 1. Create a New Group

### Command

```bash

sudo groupadd developers

```

### Description

I create a group called developers.

### Screenshot

![Alt text](screenshots/groupadd.png)

## 2. Display Group Information

### Command

```bash

getent group developers

```

### Description

This command shows details about the developers group.

### Screenshot

![Alt text](screenshots/getent-group.png)

## 3. Rename a Group

### Command

```bash

sudo groupmod -n security developers

```

### Description

The developers group is renamed to security.

### Screenshot

![Alt text](screenshots/groupmod.png)

## 4. Add a User to a Group

### Command

```bash

sudo gpasswd -a testuser security

```

### Description

I add testuser to the security group.

### Screenshot

![Alt text](screenshots/gpasswd-add.png)

## 5. Remove a User from a Group

### Command

```bash

sudo gpasswd -d testuser security

```

### Description

The testuser is removed from the security group.

### Screenshot

![Alt text](screenshots/gpasswd-delete.png)

## 6. Switch to a New Group

### Command

```bash

sudo gpasswd -a testuser security

```

### Description

My current session switches to the security group.

### Screenshot

![Alt text](screenshots/newgrp.png)

## 7. View All Groups

### Command

```bash

cat /etc/group

```

### Description

This shows all groups on my system.

### Screenshot

![Alt text](screenshots/etc-group.png)

## 8. Display Members of a Group

### Command

```bash

getent group security

```

### Description

The members of the security group are displayed.

### Screenshot

![Alt text](screenshots/group-members.png)
## 9. Delete a Group

### Command

```bash

sudo groupdel security

```

### Description

The security group is deleted.

### Screenshot

![Alt text](screenshots/groupdel.png)

## 10. Verify Group Deletion

### Command

```bash

getent group security

```

### Description

I check if the security group still exists.

### Screenshot

![Alt text](screenshots/group-verify.png)

# conclusion

In this part here is what I learned:

- I can create a group with `groupadd`.

- `getent group` helps me view group information.

- I rename a group using `groupmod`.

- To add a user to a group I use `gpasswd -a`.

- ` -d` removes a user from a group.

- `newgrp` switches my current session to another group.

- All system groups are shown with `cat /etc/group`.

- Group members are displayed using `getent group`.

- I delete a group, with `groupdel`.

- Finally I verify group deletion using `getent group`.



--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


# Part 3 – File Ownership & Advanced Permissions

## 1. Change File Owner

### Command

```bash

sudo chown testuser sample.txt

```

### Description

I can change the owner of sample.txt to testuser. This is how I do it. I use the command chown to change the owner of the file sample.txt to testuser.

### Screenshot

![Alt text](screenshots/chown-user.png)

---

## 2. Change Owner and Group

### Command

```bash

sudo chown testuser:security sample.txt

```

### Description

I can change both the owner and the group of the file sample.txt. This is how I do it. I use the command chown to change the owner and group of sample.txt to testuser and security.

### Screenshot

![Alt text](screenshots/owner-group.png)

---

## 3. Display Default File Permissions

### Command

```bash

umask

```

### Description

I can see the default permission mask used when I create files and directories. This is how I do it. I use the command umask to see the default permission mask.

### Screenshot

![Alt text](screenshots/umask.png)

---

## 4. Set a New Default Permission Mask

### Command

```bash

umask 022

```

### Description

I can set a default permission mask for new files and directories. This is how I do it. I use the command umask to set the default permission mask to 022.

### Screenshot

![Alt text](screenshots/umask-022.png)

---

## 5. Display File Attributes

### Command

```bash

lsattr sample.txt

```

### Description

I can see the attributes assigned to the file sample.txt. This is how I do it. I use the command lsattr to see the attributes of sample.txt.

### Screenshot

![Alt text](screenshots/lsattr.png)

---

## 6. Make a File Immutable

### Command

```bash

sudo chattr +i sample.txt

```

### Description

I can make the file sample.txt immutable. This means it cannot be changed or deleted. This is how I do it. I use the command chattr to make sample.txt immutable.

### Screenshot

![Alt text](screenshots/chattr-add.png)

---

## 7. Remove Attribute

### Command

```bash

sudo chattr -i sample.txt

```

### Description

I can remove the immutable attribute from the file sample.txt. This is how I do it. I use the command chattr to remove the attribute from sample.txt.

### Screenshot

![Alt text](screenshots/chattr-remove.png)

---

## 8. Display File Path Permissions

### Command

```bash

namei -l sample.txt

```

### Description

I can see the permissions of every directory in the path of the file sample.txt. This is how I do it. I use the command namei to see the permissions of every directory in the path of sample.txt.

### Screenshot

![Alt text](screenshots/namei.png)

---

## 9. Set an Access Control List (ACL)

### Command

```bash

sudo setfacl -m u:testuser:rwx sample.txt

```

### Description

I can give testuser read write and execute permissions to the file sample.txt using an Access Control List. This is how I do it. I use the command setfacl to give testuser these permissions.

### Screenshot

![Alt text](screenshots/setfacl.png)

---

## 10. Display the Access Control List

### Command

```bash

getfacl sample.txt

```

### Description

I can see the Access Control List entries for the file sample.txt. This is how I do it. I use the command getfacl to see the Access Control List entries for sample.txt.

### Screenshot

![Alt text](screenshots/getfacl.png)

---
#  conclusion


In this part, I learned how to:

- Change the owner of a file using `chown`.
- Change both the owner and group of a file using `chown user:group`.
- View the default permission mask using `umask`.
- Set a new default permission mask using `umask 022`.
- Display file attributes using `lsattr`.
- Make a file immutable using `chattr +i`.
- Remove the immutable attribute using `chattr -i`.
- View file path permissions using `namei -l`.
- Grant file permissions using `setfacl`.
- Display Access Control Lists using `getfacl`.


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


# Part 4 – Managing Processes

## 1. Looking at All Running Processes

### Situation

My system is running slowly. I need to see what is going on before I can fix it. So I need to look at all the processes that are currently running.

### Command

```bash

ps aux

```

### What it Does

This command shows me information about all the processes that are running on my system. This helps me understand what is going on and what might be causing the problem.

### Screenshot

![Alt text](screenshots/ps-aux.png)

---

## 2. Looking at the Process Tree

### Situation

I want to know which processes started processes. This will help me understand how everything is connected.

### Command

```bash

pstree

```

### What it Does

This command shows me a tree of all the running processes. It is like a family tree. For processes. This helps me see which processes started processes.

### Screenshot

![Alt text](screenshots/pstree.png)

---

## 3. Finding a Process by Name

### Situation

I need to find the process ID of the Firefox browser. I do not know what the ID is. I know the name of the process.

### Command

```bash

firefox

```

### What it Does

This command searches for running processes by name and returns their process IDs. This is really useful when I know the name of the process but not the ID.

### Screenshot

![Alt text](screenshots/firefox.png)

---

## 4. Finding the Process ID

### Situation

I want to know the exact process ID of the SSH service. I need this ID to do things with the process.

### Command

```bash

pidof ssh

```

### What it Does

This command shows me the process ID of the specified running program. This is really useful when I need to know the ID of a process.

### Screenshot

![Alt text](screenshots/pidof.png)

---

## 5. Stopping a Process

### Situation

A process has stopped responding. I need to stop it. This process is using up system resources. Needs to be stopped.

### Command

```bash

kill <PID>

```

### Example

```bash

kill 1234

```

### What it Does

This command stops a process using its process ID. This is really useful when a process is not responding and needs to be stopped.

### Screenshot

![Alt text](screenshots/kill.png)

---

## 6. Killing a Process by Name

### Situation

of remembering the process ID I want to stop a process directly by its name. This is easier than remembering the ID.

### Command

```bash

pkill sleep

```

### What it Does

This command stops processes that match the specified name. This is really useful when I know the name of the process but not the ID.

### Screenshot

![Alt text](screenshots/pkill.png)

---

## 7. Killing All Instances of a Program

### Situation

Multiple instances of a program are. I need to stop all of them. This program is using up system resources. Needs to be stopped.

### Command

```bash

killall 

```

### What it Does

This command stops all running instances of the program. This is really useful when I need to stop all instances of a program.

### Screenshot

![Alt text](screenshots/killall.png)

---

## 8. Starting a Process with Lower Priority

### Situation

I have a task that uses a lot of CPU. I do not want it to affect system performance. So I need to start the process with a priority.

### Command

```bash

nice - n 10 sleep 300

```

### What it Does

This command starts a process with a CPU scheduling priority. This means that the process will not use much CPU and will not affect system performance as much.

### Screenshot

![Alt text](screenshots/nice.png)

---

## 9. Changing Process Priority

### Situation

A running process needs its priority changed. I need to adjust the priority so that the process uses less CPU.

### Command

```bash

renice 5 -p <PID>

```

### Example

```bash

renice 5 -p 1234

```

### What it Does

This command changes the scheduling priority of an existing process. This means that I can adjust the priority of a process that is already running.

### Screenshot

![Alt text](screenshots/renice.png)

---

## 10. Looking at Background Jobs

### Situation

I started a command in the background. I want to check its status. I need to see if the command is still running or if it has finished.

### Command

```bash

jobs

```

### What it Does

This command shows me jobs that are running in the shell session. This means that I can see what commands are currently running in the background.

### Screenshot

![Alt text](screenshots/jobs.png)

---

# conclusion

In this part I learned how to manage processes. I learned how to:

- look at all running processes using `ps aux` command.

- display processes in a tree structure using `pstree` command.

- search for processes using `command.

- find a process ID using `pidof` command.

- stop a process using `kill` command.

- kill processes by name using `pkill` command.

- stop all instances of a program using `killall` command.

- start processes, with a custom priority using `nice` command.

- modify process priority using `renice` command.

- monitor background jobs using `jobs` command. Managing processes is a part of using a system. It helps me understand what is going on and how to fix problems.


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Part 5 – Service Management

## 1. Check Service Status

### Scenario

The web server is not working. I need to see if the apache2 service is running.

### Command

```bash

systemctl status apache2

```

### Description

This command shows me if the apache2 service is running or not.

### Screenshot

![Alt text](screenshots/systemctl-status.png)

---

## 2. Start a Service

### Scenario

The apache2 web server is stopped. I need to start it

### Command

```bash

sudo systemctl start apache2

```

### Description

This command starts the apache2 service away.

### Screenshot

![Alt text](screenshots/systemctl-start.png)

---

## 3. Stop a Service

### Scenario

A service is using many resources. I need to stop the apache2 service.

### Command

```bash

sudo systemctl stop apache2

```

### Description

This command stops the apache2 service.

### Screenshot

![Alt text](screenshots/systemctl-stop.png)

---

## 4. Restart a Service

### Scenario

I changed the apache2 service configuration. I need to apply these changes.

### Command

```bash

sudo systemctl restart apache2

```

### Description

This command stops. Then starts the apache2 service again.

### Screenshot

![Alt text](screenshots/systemctl-restart.png)

---

## 5. Enable a Service at Boot

### Scenario

I want the apache2 web server to start automatically when the system starts.

### Command

```bash

sudo systemctl enable apache2

```

### Description

This command makes the apache2 service start automatically when the system boots up.

### Screenshot

![Alt text](screenshots/systemctl-enable.png)

---

## 6. Disable a Service at Boot

### Scenario

I do not want a service to start automatically during boot.

### Command

```bash

sudo systemctl disable apache2

```

### Description

This command prevents the apache2 service from starting during boot.

### Screenshot

![Alt text](screenshots/systemctl-disable.png)

---

## 7. Check Whether a Service is

### Scenario

I need to know if the apache2 service is running now.

### Command

```bash

systemctl is-active apache2

```

### Description

This command tells me if the apache2 service is running or not.

### Screenshot

![Alt text](screenshots/systemctl-is-active.png)

---

## 8. View Service Logs

### Scenario

The apache2 service did not start. I need to see what went wrong.

### Command

```bash

journalctl -u apache2

```

### Description

This command shows me the logs, for the apache2 service.

### Screenshot

![Alt text](screenshots/journalctl-service.png)

---

## 9. List Failed Services

### Scenario

I want to see which services failed to start when the system booted up.

### Command

```bash

systemctl --failed

```

### Description

This command shows me all the services that failed to start.

### Screenshot

![Alt text](screenshots/systemctl-failed.png)

---

# conclusion

In this part I learned how to:

- Check the apache2 service status using `systemctl status`.

- Start the apache2 service using `systemctl start`.

- Stop the apache2 service using `systemctl stop`.

- Restart the apache2 service using `systemctl restart`.

- Enable the apache2 service to start using `systemctl enable`.

- Disable the apache2 service from starting automatically using `systemctl disable`.

- Check if the apache2 service is running using `systemctl is-active`.

- View the apache2 service logs using `journalctl`.

- List all the failed services using `systemctl --failed`.


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Part 6 – Storage Management

## 1. Display Block Devices

### Scenario

When I am working with Storage Management I need to see all the Storage Devices that're available. This is important because I have to identify all the Storage Devices before I can create a partition or fix a problem with a disk.

### Command

```bash

lsblk

```

### Description

The `lsblk` command is used for Storage Management. It shows me information about all the block devices, including disks and partitions. This is very useful for Storage Management.

### Screenshot

![Alt text](screenshots/lsblk.png)

---

## 2. Display Filesystem Information

### Scenario

I need to know what type of filesystem is being used by the Storage Devices and what the UUID is. This information is important for Storage Management.

### Command

```bash

lsblk -f

```

### Description

The `lsblk -f` command is used for Storage Management. It shows me the block devices, the type of filesystem the UUID and where they are mounted. This is useful for Storage Management because it gives me all the information I need about the Storage Devices.

### Screenshot

![Alt text](screenshots/lsblk-f.png)

---

## 3. Display Filesystem UUIDs

### Scenario

As a system administrator I need to know the UUID of a partition before I can edit the `/etc/fstab` file. This is a part of Storage Management.

### Command

```bash

sudo blkid

```

### Description

The `blkid` command is used for Storage Management. It shows me the UUID, the type of filesystem and the labels of the Storage Devices. This is useful for Storage Management because it gives me the information I need to work with the Storage Devices.

### Screenshot

![Alt text](screenshots/blkid.png)

---

## 4. Display Mounted Filesystems

### Scenario

I need to see which filesystems are currently being used. This is important for Storage Management because I need to know what is going on with the Storage Devices.

### Command

```bash

findmnt

```

### Description

The `findmnt` command is used for Storage Management. It shows me all the mounted filesystems in a tree structure. This is useful for Storage Management because it gives me a picture of how the Storage Devices are being used.

### Screenshot

![Alt text](screenshots/findmnt.png)

---

## 5. Display Disk Usage by Filesystem Type

### Scenario

I want to see how much space is available on the disks and what type of filesystem is being used. This is a part of Storage Management.

### Command

```bash

df -Th

```

### Description

The `df -Th` command is used for Storage Management. It shows me how much space is being used by the disks and what type of filesystem is being used. This is useful for Storage Management because it gives me the information I need to manage the Storage Devices.

### Screenshot

![Alt text](screenshots/df-th.png)

---

## 6. Display File and Directory Sizes

### Scenario

One of the directories is using much space and I need to find out which files are the biggest. This is a part of Storage Management.

### Command

```bash

du -ah

```

### Description

The `du -ah` command is used for Storage Management. It shows me the size of all the files and directories. This is useful for Storage Management because it helps me identify which files are using the space.

### Screenshot

![Alt text](screenshots/du-ah.png)

---

## 7. Display Mounted Devices

### Scenario

Before I remove a USB drive I need to make sure it is not being used. This is a part of Storage Management.

### Command

```bash

mount

```

### Description

The `mount` command is used for Storage Management. It shows me all the mounted filesystems and where they are mounted. This is useful for Storage Management because it helps me avoid removing a device that is still being used.

### Screenshot

![Alt text](screenshots/mount.png)

---

## 8. Display Partition Table

### Scenario

Before I create or modify partitions I need to see how the disks are currently set up. This is a part of Storage Management.

### Command

```bash

sudo fdisk -l

```

### Description

The `fdisk -l` command is used for Storage Management. It shows me all the available disks and their partition tables. This is useful for Storage Management because it gives me the information I need to work with the partitions.

### Screenshot

![Alt text](screenshots/fdisk-l.png)

---

## 9. Check Filesystem Health (Read-

### Scenario

Before I do any maintenance I need to check the filesystem to make sure it is okay. This is a part of Storage Management.

### Command

```bash

sudo fsck -N /dev/sda1

```

### Description

The `fsck -N` command is used for Storage Management. It shows me what would happen if I checked the filesystem without actually doing anything. This is useful, for Storage Management because it helps me avoid making any mistakes.

### Screenshot

![Alt text](screenshots/fsck-n.png)

---

#

In this part I learned how to use the following Storage Management commands:

- `lsblk` to view block devices.

- `lsblk -f` to display information.

- `blkid` to view partition UUIDs.

- `findmnt` to display mounted filesystems.

- `df -Th` to check disk usage.

- `du -ah` to analyze file and directory sizes.

- `mount` to view mounted devices.

- `fdisk -l` to inspect partition tables.

- `fsck -N` to preview filesystem checks. I learned about all these Storage Management commands. Storage Management is very important. I will use these Storage Management commands to manage the Storage Devices.
