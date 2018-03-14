## Mysql

Change default charset & collation

```
SET NAMES utf8mb4
SET NAMES utf8mb4 COLLATE utf8mb4_unicode_ci
```

and make `~/.my.cnf` with the following:

```
[client]
default-character-set = utf8mb4

[mysql]
default-character-set = utf8mb4

[mysqld]
character-set-client-handshake = FALSE
character-set-server = utf8mb4
collation-server = utf8mb4_unicode_ci
```
