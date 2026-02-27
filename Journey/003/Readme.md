# Disable Direct SSH root Login

Direct root SSH login: Logging into a server over SSH using the root account (username root).

**Why restrict it:**
- Direct root access is risky because if the password is compromised, the attacker has full control.
- Best practice is to log in as a regular user and use sudo for administrative tasks.

Task: Disable root login for SSH on all application servers.

To disable direct root ssh login. First we get inside the app server

<img width="771" height="159" alt="image" src="https://github.com/user-attachments/assets/74e33540-1d4a-4b4d-9ed1-fd10c7c83838" />

```sudo vi /etc/ssh/sshd_config```

<img width="771" height="22" alt="image" src="https://github.com/user-attachments/assets/edb47832-aa87-4827-8706-68e185c1d2bd" />

**Find the line:**
```PermitRootLogin yes```

**Change it to:**
```PermitRootLogin no```

<img width="771" height="106" alt="image" src="https://github.com/user-attachments/assets/1f1cf5ca-adc9-4bfe-9556-7b78ec35da72" />

**Restart SSH service**
```sudo systemctl restart sshd```

**Verify**
```sudo grep PermitRootLogin /etc/ssh/sshd_config```

<img width="771" height="95" alt="image" src="https://github.com/user-attachments/assets/fe414ae8-3178-4104-b4f6-445c33d5eb53" />

Repeat the same for other two App Servers
