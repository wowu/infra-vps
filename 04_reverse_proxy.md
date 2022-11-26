[← Powrót](README.md)

## Reverse proxy

Dodaj do pliku `bit.conf` nowy blog konfiguracyjny:

```
# Dodaj na końcu pliku:

server {
  listen 80;
  server_name <domena>;

  location / {
    proxy_pass http://localhost:8080;
  }
}
```

Sprawdź poprawność konfiguracji i przeładuj serwer.

Uruchom aplikację na porcie 8080, tym razem bindując serwer do localhosta:

```
cd ~
cd realworld
python3 manage.py runserver localhost:8080
```

Sprawdź czy możesz wejść na stronę `http://<adres-ip>:8080`.

Wejdź na stronę `http://<domena>`.

### Nginx: Location

Dodaj następujący blok `location` do wybranej domeny:

```
server {
  ...

  location /hello {
    add_header Content-Type text/html;
    return 200 "Witam na mojej domenie";
  }

  ...
}
```

Sprawdź poprawność konfiguracji i przeładuj serwer.

