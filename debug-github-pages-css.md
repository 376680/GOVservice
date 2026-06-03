# Debug Session: github-pages-css

## Status: [OPEN]

## Symptom
GitHub Pages 部署后页面 CSS 样式丢失，页面显示为无样式的 HTML。本地 `localhost:8080` 正常。

## Hypotheses
1. **路径问题 (H1)**: `index_files/` 相对路径在 GitHub Pages 子目录 (`/GOVservice/`) 下解析错误，导致 CSS 404
2. **大小写问题 (H2)**: GitHub Pages 对文件名大小写敏感，而本地不敏感
3. **MIME 类型问题 (H3)**: GitHub Pages 对某些文件返回错误的 Content-Type
4. **文件缺失 (H4)**: `index_files` 目录未提交到 GitHub
5. **缓存问题 (H5)**: 浏览器或 GitHub Pages CDN 缓存了旧版本

## Evidence

