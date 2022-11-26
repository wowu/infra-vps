[← Powrót](README.md)

## Uruchomienie aplikacji

Sklonuj repozytorium z przykładową aplikacją:

```
git clone https://github.com/Wowu/realworld.git
```

Zainstaluj zależności:

```
sudo apt update
sudo apt install python3 python3-pip

cd realworld
pip install -r requirements.txt
```

Stwórz bazę danych i tabele:

```
python3 manage.py migrate
```

Uruchom aplikację:

```
python3 manage.py runserver 0.0.0.0:8080
```

Otwórz stronę `http://<adres-ip>:8080`.

Zadziała również `http://<domena>:8080`.

Zatrzymaj aplikację wciskając <kbd>Ctrl</kbd> + <kbd>C</kbd>.
