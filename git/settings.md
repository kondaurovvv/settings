# Установка и настройка Git

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

## Установка Git

```bash
apt install git
```

Выходим из под **root**.

Добовляем глобальное имя.

```bash
git config --global user.name "name"
```

Добавляем глобально почту.

```bash
git config --global user.email example@email.com
```

Проверяем имя и почту.

```bash
git config --list --show-origin
```
