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

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


### Group Management

```bash
cat /etc/group                 # List groups
id rajesh                      # Show user IDs and groups
sudo groupadd nautilus_noc     # Create a group
sudo adduser rajesh            # Create a user
sudo usermod -g nautilus_noc rajesh  # Set primary group
sudo usermod -s /sbin/nologin ammar     # Disable interactive login
sudo adduser -e 2027-02-17 siva         # Set account expiry date
sudo chage -l siva                      # View account aging details
```

**Remember:**
- `/etc/group` — Group information.
- `-g` — Set the user's primary group.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


