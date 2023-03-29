# 如何配置SMTP服务器？

默认情况下，APITable 不配置SMTP服务器，这意味着您不能邀请用户，因为它需要电子邮件发送功能。

需要使用自己的邮箱修改.env配置，重启 backend-server。

```conf
MAIL_ENABLED=true
MAIL_HOST=smtp.xxx.com
MAIL_PASSWORD=your_email_password
MAIL_PORT=465
MAIL_SSL_ENABLE=true
MAIL_TYPE=smtp
MAIL_USERNAME=your_email
```

我添加一些东西：

```
xxa=xsd
kdsfds=lok
```

I like play basketball.

I add some code like .env file define.

such like: `
abc=code
kio=ok
url=lop`

I like banana.

In addition, some mailboxes need to be enabled in the background to use smtp. For details, you can search for xxx mailbox smtp tutorial.


## Performance problem under macOS M1 docker run?

## Where is the API documentation?

You can access the API documentation by starting a local server:

1. The documentation address for the Backend server is: <http://localhost:8081/api/v1/doc.html>

2. The documentation address for the Room server is: <http://localhost:3333/nest/v1/docs>

If you are interested in cloud service API interfaces, you can also directly access the online API documentation at <https://developers.apitable.com/api/introduction>.

## How to set the limitation of widget quantity in dashboard? (30 by default)

This can be achieved by setting the `DSB_WIDGET_MAX_COUNT` parameter in the `.env` file.

## Can I increase request rate limit of the API? (5 by default)

In the `.env.default` file of `room-server`, there are two parameters that can adjust request frequency:

1. You can set `LIMIT_POINTS` and `LIMIT_DURATION` to indicate the number of requests that can be made in a unit time period. Where LIMIT_POINTS is the number of times and LIMIT_DURATION is the duration, measured in seconds.

2. You can set the parameter `LIMIT_WHITE_LIST` to set a separate request frequency for specific users. Its value is a JSON string, and its structure can refer to `Map<string, IBaseRateLimiter>`.

## How to increase the number of records inserted per API call? (10 by default)

This can be achieved by setting the `API_MAX_MODIFY_RECORD_COUNTS` parameter in the `.env.default` file of `room-server`.


## How to upgrade to the newest release version?


## How to change the default 80 port?

Configuration properties in  the `.env` file can also be overridden  by specifying them env vars `NGINX_HTTP_PORT`

For example. It would be set as NGINX_HTTP_PORT=8080

## why is me?

Because I am the hero.

## How about you?

I'm fine.
