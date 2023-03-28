# Wie konfiguriere ich den SMTP-Server?

Standardmäßig konfiguriert APITable den SMTP-Server nicht, was bedeutet, dass Sie keine Benutzer einladen können, da dies die E-Mail-Versand-Funktion erfordert.

Es wird benötigt um die Konfiguration von `.env` mittels Selbst-E-Mail zu ändern und den Backend-Server neu zu starten.

```conf
MAIL_ENABLED=true
MAIL_HOST=smtp.xxx.com
MAIL_PASSWORD=your_email_password
MAIL_PORT=465
MAIL_SSL_ENABLE=true
MAIL_TYPE=smtp
MAIL_USERNAME=your_email
```

I add some thing:

```
xxa=xsd
kdsfds=lok
```

I like play basketball.

I like banana.

Zusätzlich müssen einige Postfächer im Hintergrund aktiviert werden, um smtp nutzen zu können. Für Details, können Sie nach xxx Postfach smtp Tutorial suchen.


## Leistungsproblem unter macOS M1 Docker ausführen?

## Wo ist die API-Dokumentation?

Sie können auf die API-Dokumentation zugreifen, indem Sie einen lokalen Server starten:

1. Die Dokumentationsadresse für den Backend Server ist: <http://localhost:8081/api/v1/doc.html>

2. Die Dokumentationsadresse für den Backend Server ist: [http://localhost:3333/api/v1/](http://localhost:3333/nest/v1/docs)

Wenn Sie an Cloud-API-Schnittstellen interessiert sind, können Sie auch direkt auf die Online-API-Dokumentation unter <https://developers.apitable.com/api/introduction> zugreifen.

## Wie kann ich die Anzahl der Widgets im Dashboard begrenzen? (30 Standard)

Dies kann durch das Setzen des `DSB_WIDGET_MAX_COUNT` in der Datei `.env` erreicht werden.

## Kann ich das Anfragelimit der API erhöhen? (5 Standard)

In der `.env.default` Datei von `Raum-Server`gibt es zwei Parameter, die die Zugriffsfrequenz anpassen können:

1. Sie können `LIMIT_POINTS` und `LIMIT_DURATION` einstellen, um die Anzahl der Anfragen anzugeben, die innerhalb eines Zeitraums der Einheit gestellt werden können. Wo LIMIT_POINTS die Anzahl der Male, und LIMIT_DURATION ist die Dauer, gemessen in Sekunden.

2. Sie können den Parameter `LIMIT_WHITE_LIST` so einstellen, dass eine separate Abfragefrequenz für bestimmte Benutzer festgelegt wird. Sein Wert ist ein JSON-String und seine Struktur kann sich auf `Karte<string, IBaseRateLimiter>` beziehen.

## Wie erhöht man die Anzahl der Datensätze, die pro API-Aufruf eingefügt werden? (10 Standard)

Dies kann durch das Setzen des `API_MAX_MODIFY_RECORD_COUNTS` im `.env.default` Datei von `Raum-Server` erreicht werden.


## Wie kann ich auf die neueste Release-Version aktualisieren?


## Wie ändere ich den Standard-80-Port?

Konfigurationseigenschaften in der Datei `.env` können auch überschrieben werden, indem sie env vars angeben `NGINX_HTTP_PORT`

Zum Beispiel. Es würde als NGINX_HTTP_PORT=8080 gesetzt werden
