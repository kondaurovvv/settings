# Создаем файл config для GitHub

Переходим в каталог **.ssh**.

```bash
cd .ssh
```

В каталоге **.ssh** создаем файл **config**.

```bash
nano config
```

Записываем дынные в файл.

```bash
# github_имя_ключа

Host github.имя_аккаунта.com
    PreferredAuthentications publickey
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519_github_имя_аккаунта
```

Переходим к **[Тестированию подключения](https://gitlab.com/vladimir_kondaurov/setings/-/blob/main/git/github/ssh_keys.md?ref_type=heads)**.
