# User Management

### Connect to a Server
```bash
ssh -i <private_key> user@host  # Key authentication
ssh user@host                   # Password, if configured
```

### List Users
```bash
cat /etc/passwd             # All account entries
cut -d: -f1 /etc/passwd     # Usernames only
```
- `-d:` — Use `:` as delimiter.
- `-f1` — Extract field 1.

### Create and Inspect a User
```bash
sudo useradd kirsty   # Create user
id kirsty             # Show UID, GID and groups
```

### Modify a User
```bash
sudo usermod -u 1220 kirsty              # Change UID
sudo usermod -d /var/www/kirsty kirsty   # Change home path
sudo usermod -d /var/www/kirsty -m kirsty # Change path and move files
```

**Remember:** `-u` = UID; `-d` = home directory; `-m` = move existing home contents.

**Important:** Changing a UID can leave existing files owned by the old UID. Changing the home path without `-m` does not move files.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
