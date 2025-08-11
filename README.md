# Error-Postgres-Socket

## Fixing PostgreSQL socket connection error on Unix socket

### Problem

You may encounter an error when your application tries to connect to PostgreSQL via Unix socket:

### Solution: Change PostgreSQL socket directory to `/tmp`

1. Open the PostgreSQL configuration file (`postgresql.conf`). The location may vary for example:

```bash
sudo nano /etc/postgresql/{postgres_version}/main/postgresql.conf
```
2. Find and Update in Postgres Config
```bash
unix_socket_directories = '/tmp'
```
3. Then Restart Postgres
```bash
sudo systemctl restart postgresql
```
