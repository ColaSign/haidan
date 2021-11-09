# 海胆之家签到器

[![GitHub issues](https://img.shields.io/github/issues/ColaSign/haidan?style=flat-square)](https://github.com/ColaSign/haidan/issues)
[![GitHub forks](https://img.shields.io/github/forks/ColaSign/haidan?style=flat-square)](https://github.com/ColaSign/haidan/network)

最新版本：![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/ColaSign/haidan?style=flat-square)

当前版本：![GitHub tag](https://img.shields.io/badge/tag-v0.0.6-orange)

## 更新说明

默认关闭GitHub自动定时签到功能，加入GitLab签到功能，GitLab需要自行设定签到任务。

## 使用说明

- 【已取消】UTC 18,2,8 会进行一次签到，换算成国内时间每天凌晨2点、上午10点和晚上4点执行一次
- 需要填写下方`使用方法`中的`Secrets`（GitLab在`Settings`→`CI/CD`→`Variables`中设置环境变量）

## 使用方法

- **Fork** 本项目
- 登录[海胆之家](https://www.haidan.video/)后，获得Cookies
  - `c_secure_uid`
  - `c_secure_pass`
  - `*c_secure_login`(可选/非必要)
  - `*c_secure_ssl`(可选/非必要)
  - `*c_secure_tracker_ssl`(可选/非必要)
- 设置`Secrets`
  - `HAIDAN_UID`：获取的`c_secure_uid`
  - `HAIDAN_PASS`：获取的`c_secure_pass`
  - `*HAIDAN_LOGIN`：获取的`c_secure_login`(可选/非必要)
  - `*HAIDAN_SSL`：获取的`c_secure_ssl`(可选/非必要)
  - `*HAIDAN_TRACKER_SSL`：获取的`c_secure_tracker_ssl`(可选/非必要)
- 任意修改`README.md`以启动`Action`


## Secrets 说明

|Key|Value|默认值|必须|说明|
|:-:|:-:|:-:|:-:|:-|
|`HAIDAN_UID`|`c_secure_uid`|无默认值|√|无|
|`HAIDAN_PASS`|`c_secure_pass`|无默认值|√|无|
|`HAIDAN_LOGIN`|`c_secure_login`|bm9wZQ%3D%3D|√|无|
|`HAIDAN_SSL`|`c_secure_ssl`|eWVhaA%3D%3D|√|无|
|`HAIDAN_TRACKER_SSL`|`c_secure_tracker_ssl`|eWVhaA%3D%3D|√|无|
|`HAIDAN_MULTI`|*多任务设置*|无默认值|×|多账户支持，详见下方`多账户支持`|
|`HAIDAN_PRIVACY`|`隐私等级`|1|×|`1`：隐藏用户名首尾 `2`：隐藏用户名 `3`：显示用户名|


## 多账户支持

多账户支持用于使用一个`Action`为多个账户进行签到，此设置将 **覆盖`HAIDAN_UID`、`HAIDAN_PASS`** 的设置，替代其的`Secrets`为`HAIDAN_MULTI`。

`HAIDAN_MULTI`的设置需要遵循以下格式：

```txt
UID_1@PASS_1, UID_2@PASS_2
```

总结来说，使用`@`将`UID`与`PASS`隔开，使用 **英文逗号** `,`分隔多个账户。

## LICENSE

请勿用作任何商业用途

[Apache License 2.0](LICENSE)
