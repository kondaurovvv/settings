# Установка и настройка SQL

## Заходим под root

Ctr+Alt+F1 или Terminal.

```bash
login:root
password:*************
```

## Обновление Debian

```bash
apt update && apt full-upgrade && apt autoclean && apt autoremove
```

**Загрузите пакет deb с веб-сайта и установите:**
- [DBeaver](https://dbeaver.io/download/)
- [PostgreSQL](https://www.postgresql.org/download/linux/debian/)
- [MySQL](https://dev.mysql.com/downloads/mysql/)


## Установка программ

```bash
apt install ./name_package
```

## Проверка версий

**DBeaver**

```bash
dbeaver --version
```


**Psotgres**

```bash
pg_config --version
```

или

```bash
/usr/lib/postgresql/15/bin/postgres --version
```

**MySQL**

```bash
mysqld --version
```
