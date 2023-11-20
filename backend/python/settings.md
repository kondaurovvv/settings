# Установка и настройка Python

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

## Установка Python А ЛУЧШЕ ИСПОЛЬЗОВАТЬ [PYENV](https://github.com/pyenv/pyenv)

Проверка версии **Python** (может уже установлена по умолчанию).

```bash
python3 --version
```

Проверка места нахождения **Python** -> (Должно быть /usr/bin/pythonX.X.X).

```bash
which python3
```

Скачиваем необходимые зависимости.

```bash
apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev
```

Скачиваем [**Python**](https://www.python.org/)

```bash
wget "ссылка на нужную версию"
```

Разархивировать архив.

```bash
tar -xf PythonX.X.X.tar.xz
```

Периходим в каталог **PythonX.X.X**.

```bash
cd PythonX.X.X
```

Запустить конфигурацию.

```bash
./configure --prefix=/usr --enable-optimizations
```

Запустить установку **Python**.

```bash
make altinstall
```

Проверка версии **Python**.

```bash
python3 --version
```

Проверка места нахождения **Python** -> (Должно быть /usr/bin/pythonX.X.X).

```bash
which python3
```

**Проверка переменой среды**

```bash
echo $PATH
```

## Переключения между версиями Python

Проверка всех установленых версии.

```bash
ls /usr/bin/python\*
```

Проверка всех добавленых уже версии.

```bash
update-alternatives --list python3
```

Добавления версии **Python** которых нет.

```bash
update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.X.X 1 <- приоритет
update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.X.X 2 <- приоритет
```

Переключение между версиями.

```bash
update-alternatives --config python3
```

## Удаления Python

```bash
rm -rf /usr/bin/2to3-${VER}
rm -rf /usr/bin/idle${VER}
rm -rf /usr/bin/pip${VER}
rm -rf /usr/bin/pydoc${VER}
rm -rf /usr/bin/python${VER}
rm -rf /usr/bin/python${VER}-config
rm -rf /usr/lib/libpython${VER}.a
rm -rf /usr/lib/python${VER}
rm -rf /usr/lib/python${VER}-embed.pc
rm -rf /usr/lib/python${VER}.pc
rm -rf /usr/lib/pythonX.X
```
