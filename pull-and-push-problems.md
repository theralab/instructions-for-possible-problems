# Como fazer commit em redes privadas!

## 1º Passo
Instale e execute o Git Bash e digite:
```
ssh-keygen -m PEM -t rsa -P "" -f ~/.ssh/github_key
```

## 2º passo
Digite esse comando para criar um arquivo de configuração:
```
touch config
```

E em seguida esse comando para acessar o arquivo criado:
```
vim config
```

Aperte a tecla I e cole o seguinte comando com `Ctrl+Shift+Ins`
```
Host github.com
    HostName ssh.github.com
    User git
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/github_key
    IdentitiesOnly yes
    Port 443
```
Para sair aperte ESC e digite `:wq`

## 3º Passo
Agora, ainda no Git Bash digite:
```
cat github_key.pub
```
Copie o texto que aparecer e adicione ao Github.
## 4º Passo
Voltando ao terminal, copie e cole o seguinte comando:
```
ssh -T git@github.com
```
Se der tudo certo você vai ver uma mensgem
```
Hi [username]! You've successfully authenticated, but GitHub does not provide shell access.
```
Agora você pode usar o Github! (Até a UEMA descobrir e barrar também)
