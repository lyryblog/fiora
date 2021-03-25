---
id: config
title: 配置
sidebar_label: 配置
---

服务器配置 `config/server.ts`
客户端配置 `config/client.ts`

在 fiora 根目录创建 `.env` 文件, 在里面填写 `key=value` 键值对(每行一个), 即可修改配置. 比如修改端口号 `Port=8888`

## 服务端配置

| Key                | 类型    | 默认值                             | 描述                                                                   |
| ------------------ | ------- | ---------------------------------- | ---------------------------------------------------------------------|
| Host               | string  | your ip                            | 服务端 host                                                           |
| Port               | number  | 9200                               | 服务端端口号                                                           |
| Database           | string  | mongodb://localhost:27017/fiora    | mongoDB 数据库地址                                                     |
| RedisHost          | string  | localhost                          | redis 地址主机名                                                      |
| RedisPort          | number  | 6379                               | redis 端口                                                           |
| JwtSecret          | string  | jwtSecret (推荐修改它来保证安全性) | jwt token 加密 secret                                                  |
| MaxGroupCount      | number  | 3                                  | 用户最大可以创建的群组个数                                             |
| QiniuAccessKey     | string  | ''                                 | 七牛 CDN access key. 如果为空, 则文件长传到服务端                      |
| QiniuSecretKey     | string  | ''                                 | 七牛 CDN secret key                                                    |
| QiniuBucket        | string  | ''                                 | 七牛 CDN bucket 名                                                     |
| QiniuUrlPrefix     | string  | ''                                 | 七牛 CDN bucket url 前缀, 以 / 结尾, 例如 https://cdn.suisuijiang.com/ |
| AllowOrigin        | string  | null                               | 允许的客户端 origin 列表, null 时允许所有 origin 连接, 多个值逗号分割  |
| tokenExpiresTime   | number  | 2592000000 (30 天)                 | 登陆 token 过期时间                                                    |
| Administrator      | string  | ''                                 | 管理员用户 id 列表, 多个值逗号分割                                     |
| DefaultGroupName   | string  | fiora                              | 默认群组名                                                             |
| DisableRegister    | boolean | false                              | 禁止注册账号                                                           |
| DisableCreateGroup | boolean | false                              | 禁止创建群组                                                           |

## 客户端配置

| Key                    | 类型    | 默认值          | 描述                                               |
| ---------------------- | ------- | --------------- | -------------------------------------------------- |
| Server                 | string  | /               | 客户端要连接的服务端地址                           |
| MaxImageSize           | number  | 3145728 (3MB)   | 客户端可以上传的最大图片大小                       |
| MaxBackgroundImageSize | number  | 5242880 (5MB)   | 客户端可以上传的最大背景图大小                     |
| MaxAvatarSize          | number  | 1572864 (1.5MB) | 客户端可以上传的最大头像图片大小                   |
| MaxFileSize            | number  | 10485760 (10MB) | 客户端可以上传的最大文件大小                       |
| DefaultTheme           | string  | cool            | 默认主题                                           |
| Sound                  | string  | default         | 默认通知音                                         |
| TagColorMode           | string  | fixedColor      | 默认标签颜色模式                                   |
| FrontendMonitorAppId   | string  | fixedColor      | 岳鹰监控 appId <https://yueying.effirst.com/index> |
| DisableDeleteMessage   | boolean | false           | 禁止用户撤回消息                                   |