# Paste Lite account site

[简体中文](./README.zh-CN.md)

The host-level landing page at <https://wygkzqa.github.io/> provides the Paste Lite favicon and links to the [Chinese](https://wygkzqa.github.io/paste-lite/) and [English](https://wygkzqa.github.io/paste-lite/en/) product websites. The product website remains in the [paste-lite repository](https://github.com/wygkzqa/paste-lite).

This site uses static HTML with no build dependencies. GitHub Pages publishes from the root of `main`. `.nojekyll` disables Jekyll processing.

## Local preview

```sh
python3 -m http.server 4174 --bind 127.0.0.1
```

Open <http://127.0.0.1:4174/>. Product links under `/paste-lite/` resolve on the published host, not in this standalone preview.

## Search appearance

`index.html` declares the stable `/favicon.png` URL, using the existing 256 × 256 Paste Lite icon. Keep the home page and icon publicly accessible. Google uses one favicon per hostname; it does not support a separate search favicon for a subdirectory. After deployment, request indexing of the host home page in Google Search Console when ownership is verified. Recrawling may take days to weeks, and display is not guaranteed. See [Google's favicon guidance](https://developers.google.com/search/docs/appearance/favicon-in-search).

`robots.txt` allows crawling and lists the host and product sitemaps. It applies to the entire host, including project sites. The `WebSite` structured data identifies the preferred site name as Paste Lite; Google determines the final search appearance.

Submit changes through a feature branch and pull request. Keep this README and its Chinese version synchronized. The site and reused Paste Lite icon are covered by the [MIT license](./LICENSE).
