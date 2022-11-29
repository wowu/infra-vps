[← Powrót](README.md)

## Setup

### Terminal

Zaloguj się do serwera za pomocą SSH i podaj hasło.

```
ssh ubuntu@<adres-ip>
```

### VSCode

* Instalacja VSCode: https://code.visualstudio.com/download
* Instalacja rozszerzenia "Remote - SSH": https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh
* Jak połączyć się z serwerem za pomocą VSCode: https://share.cleanshot.com/hHYuVk

### (opcjonalnie) dodaj swój klucz SSH na serwer

Jeśli chcesz mieć dostęp do serwera bez podawania hasła, możesz dodać swój klucz SSH.

```
ssh-copy-id ubuntu@<adres-ip>
```

Jeśli nie masz klucza SSH, możesz go wygenerować za pomocą komendy:

```
ssh-keygen
```
