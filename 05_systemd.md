# Działanie usługi po restarcie systemu

## Systemd unit

Utwórz plik `bit.service` w katalogu `/etc/systemd/system`.

```
sudo nano /etc/systemd/system/bit.service
```

```
[Unit]
Description=BIT Infra

[Service]
User=ubuntu
WorkingDirectory=/home/ubuntu/realworld
ExecStart=/usr/bin/python3 manage.py runserver localhost:8080
Restart=on-failure

[Install]
WantedBy=multi-user.target
```

Załaduj konfigurację.

```
sudo systemctl daemon-reload
```

Dodaj usługę do autostartu.

```
sudo systemctl enable bit
```

Uruchom usługę.

```
sudo systemctl start bit
```

Sprawdź status usługi.

```
sudo systemctl status bit
```

Wyświetl logi.

```
sudo journalctl -u bit
```
