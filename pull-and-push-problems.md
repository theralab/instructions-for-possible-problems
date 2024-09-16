# Como fazer commit em redes privadas!

## Primeiro passo
Abra seu terminal e ponha o comando

Para **Linux**
```
ssh-keygen -m PEM -t rsa -P "" -f ~/.ssh/github_key
```

Para **Windows**  ( **PRECISA** ser no cmd)
```
ssh-keygen -m PEM -t rsa -P "" -f %USERPROFILE%\.ssh\github_key
```

## Segundo passo
Caso você use Windows, entre no Git Bash e execute. Se você usar Linux, é só seguir normalmente no terminal

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
    IdentityFile ~/.ssh/github_key
    IdentitiesOnly yes
```
## Terceiro Passo
Após esses passos execute os comandos
```
ssh -T git@github.com
```

Se der tudo certo você vai ver uma mensgem
```
Hi [username]! You've successfully authenticated, but GitHub does not provide shell access.
```
 
 E Logo em seguida
```
cat github_key.pub
```

Copie o texto que aparecer e adicione ao github e tchanam!  Agora você pode fazer seus commits em uma rede que bloqueia as portas do github.
