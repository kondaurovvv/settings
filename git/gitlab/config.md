# Создаем файл config для GitLab

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
# gitlab_имя_ключа

Host gitlab.имя_аккаунта.com
    PreferredAuthentications publickey
    HostName gitlab.com
    User git
    IdentityFile ~/.ssh/id_ed25519_gitlab_имя_аккаунта
```

Переходим к **[Тестированию подключения](https://gitlab.com/vladimir_kondaurov/setings/-/blob/main/git/gitlab/ssh_keys.md?ref_type=heads)**.
