# Paste Lite 账号站点

[English](./README.md)

域名根首页 <https://wygkzqa.github.io/> 提供 Paste Lite 网站图标，以及[中文](https://wygkzqa.github.io/paste-lite/)和[英文](https://wygkzqa.github.io/paste-lite/en/)官网入口。产品官网仍由 [paste-lite 仓库](https://github.com/wygkzqa/paste-lite)维护。

本站使用静态 HTML，无构建依赖。GitHub Pages 从 `main` 分支根目录发布；`.nojekyll` 禁用 Jekyll 处理。

## 本地预览

```sh
python3 -m http.server 4174 --bind 127.0.0.1
```

打开 <http://127.0.0.1:4174/>。`/paste-lite/` 下的产品链接在正式域名上可用，单独预览本站时不提供这些页面。

## 搜索展示

`index.html` 声明固定的 `/favicon.png` 地址，沿用 256 × 256 的 Paste Lite 图标。首页与图标必须允许公开访问。Google 按主机名统一使用一个 favicon，不支持子目录单独设置搜索图标。发布后，在完成所有权验证的 Google Search Console 中对域名根首页请求编入索引。重新抓取可能需要几天至几周，并不保证展示。详见 [Google favicon 说明](https://developers.google.com/search/docs/appearance/favicon-in-search)。

`robots.txt` 允许抓取，并列出根站点和产品官网的网站地图；规则对整个主机名生效，包括项目站点。`WebSite` 结构化数据将首选站点名称设为 Paste Lite，最终搜索展示由 Google 决定。

修改通过独立分支与 PR 提交。保持本说明及英文版本同步。本站及复用的 Paste Lite 图标采用 [MIT 许可证](./LICENSE)。
