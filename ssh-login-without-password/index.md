# Ssh Login Without Password



# Ssh Login Without Password

## SSH login linux/unix without password

## General your key

```
ssh-keygen-t rsa
```

## copy your rsa.pub to server which you want to login without password.

``` bash
ssh-copy-id -i ~/.ssh/id_rsa.pub user1@$server-hosts
```

## Test login

```bash
ssh user1@$server-hosts
```

