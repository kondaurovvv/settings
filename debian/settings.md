# Настройка Debian после установки

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

## Изменение локализации

```bash
locale -a
```

```bash
dpkg-reconfigure locales
```

**Выбираем:**

- ru_RU.UTF-8 UTF-8
- en_US.UTF-8

```bash
locale -a
```

## Добавляем язык в консоль

```bash
dpkg-reconfigure console-setup
```

**Выбираем:**

- UTF-8
- Combined – Latin; Slavic Cyrillic; Greek
- Fixed

## Добавляем раскладку клавиатуры

```bash
dpkg-reconfigure keyboard-configuration
```

**Выбираем:**

- Generic 105-key PC (intl)
- Other
- Russia
- Russia
- Alt+Shift
- No temporary switch
- The default for the keyboard layout
- No compose Key
- No

```bash
service keyboard-setup restart
```

Открываем файл **profile**.

```bash
nano /etc/profile
```

В конце файла пишем **setupcon --force**.

## Добавить ветки в репозитории Debian

```bash
nano /etc/apt/sources.list
```

В конце каждой строки добавьте **contrib non-free**.

### Обновляем Debian

```bash
apt update && apt full-upgrade && apt autoclean && apt autoremove
```

## Установка видеодрайвера

### Проверьте какая видеокарта установлена

```bash
lspci -nn | egrep -i "3d|display|vga" или lspci -v
```

Если у вас интегрированная графика Intel, то смотрим установлен ли видеодрайвер i915, если установлен, то все супер.

### Установка видеодрайвера NVIDIA

```bash
apt install nvidia-driver
```

Перезагрузитесь после всех установок.

```bash
reboot
```

Проверка установленного видеодрайвера.

```bash
lspci -v
```
Удаление драйверов NVIDIA.

```bash
apt remove nvidia-* --purge
```

## Установка программ

```bash
apt install xclip vlc qbittorrent gimp eog telegram-desktop
```

**Загрузите пакет deb с веб-сайта и установите:**

- [Google chrome](https://www.google.com/intl/ru/chrome/)
- [Yandex](https://browser.yandex.ru/)
- [Opera](https://www.opera.com/ru)
- [Firefox](https://www.mozilla.org/ru/firefox/)
- [MEdge](https://www.microsoft.com/ru-ru/edge/download?form=MA13FJ)
- [VSCode](https://code.visualstudio.com/)
- [DBeaver](https://dbeaver.io/download/)
- [PostgreSQL](https://www.postgresql.org/download/linux/debian/)

```bash
apt install ./package_name.deb
```

## Удалить нижнюю панель

- Settings/Panel <- Panel 2
- Settings/Display/Output <- Primary

Нажмите справа минус.

## Настройки питания

- Settings/Power Manager/General <- выключи все
- Settings/Power Manager/System <- выключи все
- Settings/Power Manager/Display <- выключи все
- Settings/Power Manager/Security <- выключи все

## Настройка тёмной темы

- Settings/Appearance <- Adwaita-dark

## Появление иконок только на главном экране

- Settings/Desktop/Icons <- Show icons on primary display

## Добавления переключателя языка

- Settings/Panel Preferences/items <- Add/Keyboard Layouts

## Создать нового пользователя

```bash
adduser name
```
