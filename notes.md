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

![Alt text](screenshots/chage.png)

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
