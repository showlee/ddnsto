---
title: 为什么我的APP用不了DDNSTO？
date: 2021-6-24
tag: js
tags: 
  - app
  - 客户端
  - 验证 
---

# 为什么我的APP用不了DDNSTO？

为什么我的RDP客户端无法访问？

为什么我手机上群晖APP无法访问？

为什么有时候能用有时候不能用？

。。。

这些常见的问题，给大家一次性说明白。

## 哪些客户端可以使用？

- 使用http协议（包括websocket、webdav）的客户端基本都能使用

- 非http协议，如rdp、ssh等协议的客户端，目前都不支持使用DDNSTO。

没错，避免拿来做坏事以及控制运营的成本，DDNSTO目前不支持非HTTP协议的TCP、UDP穿透。

请注意，为了保证客户端能正常使用，用户当前IP需经过身份验证。


## 为什么要身份验证？

DDNSTO在保护用户数据安全同时也要避免恶意分享不良内容带来的法律风险，所以我们对用户的域名访问都做了认证判断：服务器会判断用户当前IP是否已经过验证，如果没有就会跳转验证流程。

所以当你的第三方客户端使用DDNSTO时，需要先在浏览器访问一遍对应域名进行身份验证。否则客户端可能会出现连接失败或假死等错误。

## 我有rdp、ssh的需求，怎么办？

可以使用DDNSTO的远程应用，我们也会不断拓展远程应用的能力。