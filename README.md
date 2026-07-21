# 我的 Hugo + Blowfish 博客

这是一个使用 [Hugo](https://gohugo.io/) 和 [Blowfish](https://blowfish.page/) 的博客，推送到 GitHub 后会自动部署到 GitHub Pages。

## 本地预览

```bash
git submodule update --init --recursive
hugo server -D
```

浏览器打开 <http://localhost:1313/>。

## 发布到 GitHub Pages

1. 在 GitHub 新建一个仓库。若要使用 `https://你的用户名.github.io/`，仓库必须命名为 `你的用户名.github.io`。
2. 将本地仓库关联并推送：

   ```bash
   git remote add origin https://github.com/你的用户名/仓库名.git
   git add .
   git commit -m "Initial Hugo blog"
   git push -u origin main
   ```

3. 在 GitHub 仓库的 **Settings → Pages → Build and deployment** 中，将 Source 设为 **GitHub Actions**。
4. 等待 Actions 完成，Pages 链接会显示在部署结果中。

## 从这里开始修改

- 基本资料、头像和社交链接：`config/_default/languages.zh-cn.toml`
- 外观和文章显示选项：`config/_default/params.toml`
- 菜单：`config/_default/menus.zh-cn.toml`
- 新文章：`content/posts/`，或执行 `hugo new content posts/文章标题.md`

请保留 `themes/blowfish` 原样；需要深度定制时，在本站目录新增 `layouts/`、`assets/` 等覆盖文件即可。
