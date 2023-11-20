# Установка и настройка Nodejs

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

## Устанавливаем [Nodejs](https://nodejs.org)

Создаем каталог **nodejs**.

```bash
mkdir -p /usr/local/lib/nodejs
```

Распаковываем архив (архив должен быть "имя.tar.xz").

```bash
tar -xJvf node-$VERSION-$DISTRO.tar.xz -C /usr/local/lib/nodejs
```

Выходим с **root**.

```bash
exit
```

Записываем даные в файл **.bashrc**.

```bash
nano ~/.bashrc
```

```bash
# Nodejs

VERSION=v18.16.0 <- пишим версию nodejs
DISTRO=linux-x64 <- пишем версию системы
export PATH=/usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin:$PATH
```

После записи данных перезагружаем файл **.bashrc**.

```bash
. ~/.bashrc
```

Проверяем версию **nodejs**.

```bash
node --version
npm --version
npx --version
```
