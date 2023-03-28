# 如何配置SMTP服务器？

默认情况下，APITable 不配置SMTP服务器，这意味着您不能邀请用户，因为它需要电子邮件发送功能。

需要使用自己的邮箱修改.env配置，重启 backend-server。

```conf
MAIL_ENABLED=true
MAIL_HOST=smtp.xxx.com
MAIL_PASSSWORD=您邮箱密码
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

我喜欢玩篮球。

I add some code like .env file define.

such like: `
abc=code
kio=ok
url=lop`

我喜欢香蕉。

另外，有些邮箱需要在后台启用smtp。 详细可以搜索xxx邮箱smtp教程。


## macOS M1 下 docker 运行的性能问题？

## API文档在哪里？

您可以通过启动本地服务器来访问 API 文档：

1. backend-server 的文档地址为: <http://localhost:8081/api/v1/doc.html>

2. room-server 的文档地址为: <http://localhost:3333/nest/v1/docs>

如果您对云服务 API 接口感兴趣，也可以直接访问 <https://developers.apitable.com/api/introduction> 获取在线 API 文档。

## 如何在仪表板中设置小部件数量限制？ （默认为 30）

可以通过在 `room-server` 下的 `.env.default` 文件中设置 `API_MAX_MODIFY_RECORD_COUNTS` 参数来实现。

## 我可以增加 API 的请求速率限制吗？ （默认为 5）

在 `room-server` 下的 `.env.default` 文件中，有两个参数可以调整请求频率：

1. 您可以设置参数 `LIMIT_POINTS` 和 `LIMIT_DURATION` 来设置在单位时间段内可以发出的请求数。 其中 LIMIT_POINTS 是次数，LIMIT_DURATION 是持续时间，以秒为单位。

2. 您可以设置参数 `LIMIT_WHITE_LIST` 来为特定用户设置单独的请求频率。 它的值为一个JSON字符串，其结构可以参考`Map<string, IBaseRateLimiter>`。

## 如何增加每次 API 调用插入行记录的数量？ （默认为 10）

可以在`.env`文件中设置`DSB_WIDGET_MAX_COUNT`参数来实现。


## 如何更新到最新的版本?


## 如何更改默认的80端口?

`.env` 文件中的配置属性也可以通过指定环境变量 `NGINX_HTTP_PORT` 来覆盖。

例如： 例如： 例如：NGINX_HTTP_PORT=8080

## why is me?

Because I am the hero.

## How about you?

I'm fine.
