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

## Установка [PYENV](https://github.com/pyenv/pyenv)

Переходим к **Table of Contents** и идем по пунктам:

- install Python build dependencies

Выходим с **root**.

```bash
exit
```

- Basic GitHub Checkout
- Set up your shell environment for Pyenv
  - For bash
- Set up your shell environment for Pyenv
  - Restart your shell

**Проверка версий**

```bash
pyenv -v
```

## Установка Python

```bash
pyenv install 3.X.X
```

Проверить версии **Python**.

```bash
pyenv versions
```

Переключить глобально версию **Python**.

```bash
pyenv global 3.X.X
```

Проверить версию **Python и pip**.

```bash
python3 --version
pip --version
```

Обновить **pip**.

```bash
pip install --upgrade pip
```

Удалить ненужную версию **Python**.

```bash
pyenv uninstall 3.X.X
```

## Удалить PYENV

```bash
rm -rf "$HOME/.pyenv"
```

Из файла **.bashrc** удалить:

- export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
- command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
- eval "$(pyenv init -)"' >> ~/.bashrc
