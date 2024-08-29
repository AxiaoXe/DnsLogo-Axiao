# DnsLogo-Axiao

DNSLog-Axiao 是一款用 Go 语言编写的监控 DNS 解析记录的工具，使用路由 API 进行返回查询。

## 使用说明

- `/getdomain?t=100-999999`: 生成一个 `随机字符串.log.domain.com` 形式的关键域名
- `/getrecords?t=关键域名`: 查询是否存在该关键域名的DNS请求记录
- `/del?pwd=axiaoxe`: 清空所有DNS记录和生成的域名记录

## DNS解析记录
- `A记录 @ ip`: 设置一个A记录解析到你的服务器IP地址
- `ns	log	domain.com`: NS解析log子域名到你的域名地址
- `ns	*.log	domain.com`: NS解析*。log子域名到你的域名地址

## 服务器信息

服务器启动于 :8000

### 配置示例

```yaml
HTTP:
  port: 8000  # 开放端口

Dns:
  domain: domain.com  # 主域名

Pwd:
  Password: axiaoxe
