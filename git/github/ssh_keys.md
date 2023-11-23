# Создаем ключ SSH

В корневом каталоге **'~'** создаем ключ.

```bash
ssh-keygen -t ed25519 -C "example@email.com"
```

Введите имя файла, в котором следует сохранить ключ (/home/name/.ssh/id_ed25519).

```bash
/home/name/.ssh/id_ed25519_github_имя_аккаунта
```

Вводим пароль два раза.

Заходим в деректорию **.ssh**.

```bash
cd .ssh/
```

Читаем **id_ed25519\_\*\*\*\*\_\_\*\*.pub**.

```bash
cat id_ed25519_*******_****.pub
```

Скопируйте ключ из консоли.
В **GitHub** перейдите в **«Edit profile»**.
Перейдите в раздел **«SSH Keys»** и вставьте ключ в поле **«Add new key»**.
Нажмите **«Add key»**.

Переходим к созданию **[config](https://github.com/kondaurovvv/settings/blob/main/git/github/config.md)** файла.

## Тестируем подключение

```bash
ssh -T git@github.имя_аккаунта.com
```

## Клонирование проекта

После того, как мы создали проект на GitLab, клонируем его по SSH.

```bash
git clone git@github.com:имя_аккаунта/имя_проекта.git
```

Это стандартная команда но поскольку у нас несколько SSH,\
нам нужно прописать имя аккаунта между\
git@github."ЗДЕСЬ ПИШЕМ ИМЯ АККАУНТА".com:account_name/project_name.git\

```bash
git clone git@github.имя_аккаунта.com:имя_аккаунта/имя_проекта.git
```
