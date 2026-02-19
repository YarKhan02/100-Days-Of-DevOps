# Temporary User

Create a temporary user in App Server 3 with a expiry date.

### SSH into App Server 3

<img width="647" height="240" alt="image" src="https://github.com/user-attachments/assets/90d301c2-a952-4576-a973-fd8d7ed36f49" />

Syntax
```
sudo useradd -e YYYY-MM-DD username
```

<img width="647" height="252" alt="image" src="https://github.com/user-attachments/assets/938c9b9a-8a5c-4e16-a6e5-65ccaff76ad8" />

To check if the user is successfully created with a expiry date

Syntax
```
sudo chage -l username
```

<img width="671" height="181" alt="image" src="https://github.com/user-attachments/assets/0237576c-c92f-4749-ab66-6aa94e2d440c" />
