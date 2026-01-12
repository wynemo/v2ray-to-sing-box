# 代理配置转换工具

## 项目介绍
机场一般都是 v2ray/clash 格式的，
这是一个用于将 v2ray/clash 格式的订阅配置转换为sing-box格式的Web工具。
clash格式为yaml格式
v2ray可以是一行一行的节点信息，也可以是base64过的
(不转换规则等配置，只有节点信息)
支持多种代理协议,能够将配置快速转换为sing-box可用的JSON格式。

代码是复制粘贴和AI写的的，感谢 gui-for-singbox 插件

原作者：https://github.com/GUI-for-Cores/Plugin-Hub/blob/main/plugins/Generic/plugin-node-convert.js

下面也是AI写的，将就看吧

## 使用方法

可以直接下载打开 index.html 使用，也可以访问 https://singbox-to-uri.pages.dev/ 使用
所有转换都是在本地或浏览器进行的，不会上传到服务器 你可以放心使用 也可以检查代码

### 节点转换
1. 在输入框中粘贴需要转换的代理配置(支持Base64、URI链接、Clash YAML格式)
2. 点击"转换"按钮
3. 在输出框中获取转换后的sing-box配置
![效果图](1.png)

### Sing-box 完整配置生成器
新增完整配置生成器页面 (singbox_full_config.html)，支持 sing-box 1.12 版本配置模板，可以生成包含路由规则的完整配置文件。

## 功能特性
- 支持Base64编码输入
- 支持多行配置批量转换
- 支持 Clash YAML 格式配置
- 支持 URI 链接格式
- 输出标准sing-box JSON格式
- 支持生成 sing-box 1.12 版本完整配置
- 纯前端实现,无需后端服务

## 一些支持的协议
- Shadowsocks
- VMess
- Trojan
- VLESS

## 开发说明
本工具使用纯JavaScript实现,主要文件:
- index.html - 主界面
- test.js - 协议解析和转换逻辑

## 注意事项
- 确保输入格式正确
- 转换错误会在控制台输出
- 不支持的协议会自动跳过

## License
MIT

视频讲解：

[![视频讲解](https://img.youtube.com/vi/9CnqlpCn4pw/0.jpg)](https://www.youtube.com/watch?v=9CnqlpCn4pw)
