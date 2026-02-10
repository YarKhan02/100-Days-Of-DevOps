# Creating a user

Creating a user in App Server 1 with non interactive shell.

<img width="752" height="215" alt="image" src="https://github.com/user-attachments/assets/7853a809-4cf7-4b69-9965-882dfecd90de" />

To Create a user

<img width="752" height="195" alt="image" src="https://github.com/user-attachments/assets/ca116e36-cd44-44fe-9048-46f0b7190379" />

To Verify that it actually created with no non-interactive shell

<img width="752" height="195" alt="image" src="https://github.com/user-attachments/assets/63acb678-b2d5-4b72-9c56-750614b11495" />

## What is Non-Interactive User

Creating a user with a non-interactive shell (like /usr/sbin/nologin or /bin/false) is mainly done to stop that user from logging into the server normally.

## Purpose (why it’s used)

### Security

If the account is only meant for a service (not a real human), you don’t want anyone to SSH into it.

Example:

```
nginx
www-data
postgres
redis
```

These users exist just so services can run with limited permissions.

### For Example

We create a directory and put some files in it and dont want any other user to access them or write in that directory. we will create a non interactive user and gives directory ownership to that user. Now this directory belongs only to this user and no other user can access. And this user dont have any way to get a shell. So this directory cant be accessed. 

### Format of /etc/passwd is like this:
```
username:x:UID:GID:comment:home_directory:login_shell
```
So in your case:
```
ravi:x:100x:100x::/home/ravi:/usr/sbin/nologin
```
