# Auto-SSL-Cert

## 注意

> 不要 fork 此项目，请新建私有仓库！

## Usage

- 申请证书相关参数推荐查看原仓库：https://github.com/danbao/auto-ssl/tree/main 或者原 [README.md](ORIGIN_README.md)
- 本仓库为结合申请证书，增加部署到云平台，如：腾讯云、阿里云等

## 配置 GitHub 仓库的 Secrets

在您的 GitHub 仓库中，依次访问 `Settings -> Security -> Secrets and variables -> Actions`，添加以下三个变量：
- `EMAIL`：申请SSL需要的邮箱地址。

### 使用 腾讯

> 申请 token https://console.dnspod.cn/account/token/token （DNS API，CA 验证 DNS 时需要）

- `DP_ID`：DNSpod id
- `DP_KEY`：DNSpod token

> 申请主账号 密钥 https://console.cloud.tencent.com/cam/capi (不推荐)

> 申请子账号 密钥 [申请证书](https://ksh7.com/posts/ssl-cert-auto-deploy/#申请证书) 

- `SECRETID`
- `SECRETKEY`

![](https://image.baidu.com/search/down?url=https://gzw.sinaimg.cn/mw2000/0085UwQ9ly1hts5v8jyhsj31880jyjvc.jpg)

### 使用 阿里云

根据流程所需字段，按需配置

> [阿里云部署流程](https://ksh7.com/posts/ssl-cert-auto-deploy/#阿里云-CDN)

### 使用 Cloudflare

- `CF_TOKEN`：Cloudflare API Token。
- `CF_ACCOUNT_ID`：Cloudflare Account ID。

<img width="1177" alt="image" src="https://github.com/danbao/auto-ssl/assets/4090783/e3ea47d8-7b3e-4605-94ee-689e6bb6ca45">

## 设置 GitHub Actions 权限

在 GitHub 仓库中，依次访问 `Settings -> Code and automation -> Actions -> General -> Workflow permissions`，勾选 `Read and write permissions` 权限。

<img width="827" alt="image" src="https://github.com/danbao/auto-ssl/assets/4090783/abb42eb0-fd78-4417-bf07-9cf090ee7a2c">

## 修改 repo 中的 xxx_domains_list.txt

- 把里面的域名改为你自己的域名，可以填多个域名每行一个
- 支持多个申请证书，部署至云平台未支持多个

## 手动触发 GitHub Actions

手动 run 指定 actions

# 使用示例

> https://ksh7.com/posts/ssl-cert-auto-deploy/
