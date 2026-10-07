# GoBang5 的博客

网址：https://gobang5.github.io/

使用 Hexo 与 Redefine 主题，通过 GitHub Actions 自动发布到 GitHub Pages。使用平台的免费网址，没有购买域名或付费服务。

## 本地预览

需要 Node.js 22。

```sh
npm ci
npm run server
```

打开 http://localhost:4000 。发布前可以运行 `npm run build` 检查文章和配置是否能正常生成。

## 写博客

文章放在 `source/_posts/`，每篇一个 Markdown 文件。复制已有文章修改，或运行：

```sh
npm run new:post -- "我的文章标题"
```

文件开头的 `---` 中填写标题、日期、分类、标签；第二个 `---` 后面写正文。中文标题可以配一个稳定的英文文件名，文件名会用于文章网址。图片放在 `source/images/`，正文中引用，例如 `![图片说明](/images/example.jpg)`。

## 发碎碎念

编辑 `source/_data/essays.yml`，增加一项：

```yaml
- content: 今天试了一个新工具，先记几句感受。
  date: 2026-10-07 18:00:00
```

多行内容写成：

```yaml
- content: |
    第一段内容。

    第二段内容。
  date: 2026-10-07 18:00:00
```

保持日期格式和缩进。动态按日期排列。

## 修改个人信息和样式

- `_config.yml`：网站名称、简介、作者、网址。
- `_config.redefine.yml`：导航、主题色、封面、侧栏等样式。
- `source/about/index.md`：关于页面。

主题通过 npm 安装，定制写在 `_config.redefine.yml` 中，不直接修改 `node_modules/`。

## 更新网站

修改后提交并推送到 `main`，Actions 会自动构建和发布。也可以直接在 GitHub 网页中编辑文章或碎碎念文件，并提交更改。发布结果在仓库的 Actions 页面查看。

`public/` 和 `node_modules/` 是生成文件，不提交到 GitHub。`source/_drafts/` 中的草稿也不提交，以免尚未发布的文字出现在公开仓库。

欢迎文章和首条动态是搭建时准备的起始文案，可以随时替换或删除。

## 主题来源

- [Hexo](https://hexo.io/)
- [Redefine](https://github.com/EvanNotFound/hexo-theme-redefine)
- [Redefine 使用文档](https://redefine-docs.ohevan.com/)

主题版权与许可证保留在 npm 依赖中，页面保留主题署名。
