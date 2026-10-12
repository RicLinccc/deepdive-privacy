# 深潜 DeepDive 隐私政策页（待发布）

本目录就是要发布的静态页：`index.html`（生效日期 2026-10-12，联系邮箱 linxiaobai2026@qq.com）。
发布后把得到的 URL 填进 `entry/src/main/ets/common/PrivacySheet.ets` 第 3 行 `PRIVACY_POLICY_URL`，
再运行根目录 `build-release-app.cmd` 出最终包。

## 方案 A：GitHub Pages（约 2 分钟）

1. 登录 GitHub → New repository → 名称 `deepdive-privacy`，Public，不要勾选初始化 README
2. 在本目录执行（把 `<用户名>` 换成你的 GitHub 用户名）：

```bash
git init -b main
git add .
git commit -m "privacy policy"
git remote add origin https://github.com/<用户名>/deepdive-privacy.git
git push -u origin main
```

3. 仓库 Settings → Pages → Source 选 `main` 分支 `/ (root)` → Save
4. 1~2 分钟后生效，URL：`https://<用户名>.github.io/deepdive-privacy/`

注意：AGC 审核在国内网络，github.io 偶发访问不稳；提交审核前先用手机流量访问确认能打开。

## 方案 B：飞牛 NAS（长期最稳）

1. fnOS 上任一静态 Web 目录（自带 Web 服务或 Docker 一个 nginx）放入 `index.html`
2. 配域名 + HTTPS（AGC 不接受裸 IP；无公网 IP 用内网穿透，如 Cloudflare Tunnel/frp）
3. URL 形如 `https://<你的域名>/deepdive/privacy.html`

## 方案 C：对象存储/静态托管（腾讯云 COS、阿里云 OSS 静态网站）

开桶上传 `index.html`，开公有读 + 静态网站托管即可，费用几乎为零。
