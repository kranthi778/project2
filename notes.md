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

lastlog

```

### Description

I want to see the login information for all users, including testuser. This command displays the login information for all users.

### Screenshot

![Alt text](screenshots/lastlog.png)

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

