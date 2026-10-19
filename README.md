# The Moon Remembers · free hosting package

Prepared 18 October 2026. This is a local preparation package, **not an already-published GitHub website**.

## 零费用方案

- 使用 GitHub Free 的公开仓库和 GitHub Pages，先用免费的 `github.io` 地址。
- 不购买域名、不租服务器、不启用付费套餐、Codespaces 或付费运行器。
- 仓库内的网站代码和媒体文件将公开；不包含原工程的 Git 记录、账号凭据、内部笔记、原始 Downloads 或访客的浏览器本地收藏。
- 这个方案不等于保证中国大陆免 VPN 稳定访问；发布成功后，仍需要在大陆移动网络与家庭网络分别实测。如果效果不合适，再讨论其他托管，不自动产生任何购买。

## 你现在需要做的事

1. 到 https://github.com/signup 注册 GitHub **免费账号**，由你自己完成邮箱验证和服务条款确认；不要把密码、验证码或密钥发给助手。
2. 将 GitHub 与当前工作环境授权连接，然后告知已连接。助手可继续建立并上传干净的公开网站仓库。账号尚未授权前，本包不会自行创建仓库或上线。
3. 正式部署时，在目标仓库的 **Settings → Pages → Build and deployment → Source** 选择 **GitHub Actions**。本包已带好发布配置，不需要安装依赖或运行构建。
4. 将本目录的内容提交到仓库的 `main` 分支。保留隐藏目录 `.github`，不要只上传 `site` 文件夹，也不要把 ZIP 文件直接当作网页入口提交。
5. 在 Actions 中确认发布成功，再使用平台实际返回的网址。地址通常是 `https://你的用户名.github.io/仓库名/`；这只是格式说明，账号和仓库尚未创建，不能当作现有网址。

如果手动在浏览器上传，先解压压缩包；整个 ZIP 约 178 MiB，不要把 ZIP 本身上传为单个仓库文件。由已授权的 Git/连接工具提交这个干净目录会更合适。

## Package layout

```text
README.md
.github/workflows/pages.yml
site/
  index.html
  home.html
  lost.html
  assets/
  vendor/
  ...
```

The workflow publishes **only `site/`**, not this README, the workflow directory or the original workspace. It uses GitHub's own Pages actions and the automatic short-lived `GITHUB_TOKEN`; no personal access token or paid service is embedded. It runs only for `main` pushes or an explicit manual dispatch, not untrusted pull requests.

## Continuation and validation

- `site/` is an exact copy of the public runtime from the current version, including the three unique TV videos, four disjoint photo channels and custom bilingual photograph picker. No animation/media quality was reduced for hosting.
- English remains the default on a fresh origin. Language/music preferences and added photographs are browser-local; moving to a new domain does not move saved visitor additions automatically. Keep the original website available for any backups.
- The shell uses hash navigation and relative assets, suitable for a project subpath. HTTPS must remain enabled because camera gestures need a secure context and explicit permission.
- Check Home entry/audio, Explore gate, all three gesture rooms and Back, six films, language switch, photo constellation, uploads and TV navigation at the real deployed URL.
- The original editing project remains separate. Later updates should refresh `site/` from its verified `dist/` files before publishing, rather than editing two divergent copies independently.

Official references (checked during preparation):

- Free/public Pages availability and size limits: https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
- GitHub's own static deployment workflow: https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages
