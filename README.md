# 我的 Hugo + OINK 博客

这是一个使用 [Hugo](https://gohugo.io/) 和 [OINK](https://oink.pgsty.com/) 的博客，推送到 GitHub 后会自动部署到 GitHub Pages。

## 本地预览

需要 Hugo ≥ 0.169 与 Go（OINK 以 Hugo Module 方式引入，首次构建时自动下载）：

```bash
brew install hugo go
hugo server -D
```

浏览器打开 <http://localhost:1313/>。

## 发布

推送到 `main` 后，`.github/workflows/hugo.yml` 会自动构建并部署到 GitHub Pages：
<https://elias-zhao.github.io/eliaszhao.com/>

## 从这里开始修改

- 站点标题、语言、主题选项：`hugo.yaml`
- 首页内容（Hero、卡片）：`data/home/zh.yaml`、`data/home/en.yaml`
- 菜单：在页面 front matter 的 `menus.main` 中设置
- 新文章：`content/posts/`，或执行 `hugo new content posts/文章标题.md`
- 升级主题：`hugo mod get github.com/pgsty/oink@latest`，并提交 `go.mod` / `go.sum`

主题文档：<https://oink.pgsty.com/docs/>。需要深度定制时，在本站目录新增 `layouts/`、`assets/` 等覆盖文件即可。
