# Grant Executable Permissions

ssh into App Server 1

<img width="646" height="233" alt="image" src="https://github.com/user-attachments/assets/25321b2b-1c9e-458d-8765-e7a3594191b6" />

the current script has no permissions

<img width="510" height="70" alt="image" src="https://github.com/user-attachments/assets/06c2f620-c806-4e15-9fa4-3bd5b213713a" />

---------- → no permissions at all

- No read (r)
- No write (w)
- No execute (x)
- For owner, group, and others

root root → owned by user root and group root

Granted executable permissions to all users
```
sudo chmod 755 xfusioncorp.sh
```

Why this works
- Owner → read, write, execute
- Group → read, execute
- Others → read, execute
- All users can execute (requirement satisfied)
- Also readable → avoids validation failure
