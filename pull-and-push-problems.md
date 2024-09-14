# Como fazer commit em redes privadas!

## Primeiro passo
Abra seu terminal (de preferencia o bash) e ponha o comando

Para *Linux*
```bash
ssh-keygen -m PEM -t rsa -P "" -f ~/.ssh/github_key
```

Para *Windows*
```shell
ssh-keygen -m PEM -t rsa -P "" -f %USERPROFILE%\.ssh\github_key
```
## Segundo passo
Ainda no terminal no diretório /.ssh execute o comando
```
touch config
```

E em seguida
```
vim config
```

Cole o seguinte comando
```
Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/github_Key
    IdentitiesOnly yes
```

## Terceiro Passo
Após esses passos execute o comando 
```
cat github_key.pub
```

E adicione ao github e tchanam!  Agora você pode fazer seus commits em uma rede que bloqueia as portas do github.
