[← Powrót](README.md)

## Hostowanie statycznych plików

Utwórz folder `www`:

```
cd ~
mkdir www
```

Stwórz plik `index.html`:

```
cd www
nano index.html
```

Przykładowa treść:

```
<h1>BIT Infra</h1>
<p>Witaj na moim serwerze!</p>
```

Zapisujemy i wychodzimy wciskając <kbd>Ctrl</kbd> + <kbd>X</kbd>, następnie <kbd>Y</kbd> i <kbd>Enter</kbd>.

Zainstaluj `nginx`.

```
sudo apt install nginx
```

Sprawdzamy co dostaniemy po wejściu na adres `http://<adres-ip>`.

Utwórz plik konfiguracyjny w katalogu `/etc/nginx/conf.d`.

```
sudo nano /etc/nginx/conf.d/bit.conf
```

```
server {
  listen 80;
  server_name <domena>;

  location / {
    root /home/ubuntu/www;
  }
}
```

Sprawdź poprawność konfiguracji:

```
sudo nginx -t
```

Przeładuj konfigurację:

```
sudo systemctl reload nginx
```

Otwórz stronę `http://<domena>`.
