# ¿Cómo configurar el servidor SMTP?

Por defecto, APITable no configura el servidor SMTP, lo que significa que no puede invitar usuarios ya que requiere la función de envío de correo electrónico.

Es necesario modificar la configuración de `.env` usando autoemail, y reiniciar el servidor de backend.

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

I like banana.

Además, algunos buzones de correo deben estar habilitados en segundo plano para usar smtp. Para obtener más detalles, puede buscar el tutorial smtp del buzón de correo xxx.


## Problema de rendimiento en ejecución de macOS M1 docker?

## ¿Dónde está la documentación de API?

Puede acceder a la documentación de la API iniciando un servidor local:

1. La dirección de documentación para el servidor Backend es: <http://localhost:8081/api/v1/doc.html>

2. La dirección de documentación para el servidor Backend es: [http://localhost:3333/api/v1/](http://localhost:3333/nest/v1/docs)

Si está interesado en las interfaces API del servicio en la nube, también puede acceder directamente a la documentación de la API en línea en [https://Developopers.apitable.com/api/introduction](https://developers.apitable.com/api/introduction).

## ¿Cómo establecer la limitación de la cantidad de widgets en el panel? (30 por defecto)

Esto se puede lograr estableciendo el parámetro `DSB_WIDGET_MAX_COUNT` en el archivo `.env`.

## ¿Puedo aumentar la tasa límite de solicitud de la API? (5 por defecto)

En el archivo `.env.default` de `room-server`, hay dos parámetros que pueden ajustar la frecuencia de la solicitud:

1. Puede establecer `LIMIT_POINTS` y `LIMIT_DURATION` para indicar el número de solicitudes que se pueden realizar en un período de tiempo unitario. Cuando LIMIT_POINTS es el número de veces y LIMIT_DURATION es la duración, medida en segundos.

2. Puede establecer el parámetro `LIMIT_WHITE_LIST` para establecer una frecuencia de solicitud separada para usuarios específicos. Su valor es una cadena JSON, y su estructura puede referirse a `Mapa<string, IBaseRateLimiter>`.

## ¿Cómo aumentar el número de registros insertados por llamada API? (10 por defecto)

Esto se puede lograr configurando el parámetro `API_MAX_MODIFY_RECORD_COUNTS` en el archivo `.env.default` de `room-server`.


## ¿Cómo actualizar a la versión más reciente?


## ¿Cómo cambiar el puerto por defecto 80?

Las propiedades de configuración en el archivo `.env` también pueden ser reemplazadas especificando variables env `NGINX_HTTP_PORT`

Por ejemplo,. Se establecería como NGINX_HTTP_PORT=8080
