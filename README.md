# 交互看板部署包

本目录只有一个 `index.html`（自包含，无外部依赖）与空文件 `.nojekyll`。

## 方式一：GitHub Pages（网页上传，最省事）

1. 登录 github.com，点右上角 **+ → New repository**，仓库名随意（如 `ai-opportunity`），选 **Public**，创建。
2. 在仓库页点 **Add file → Upload files**，把本目录的 `index.html` 与 `.nojekyll` 拖进去，点 **Commit changes**。
3. 进入 **Settings → Pages**，**Source** 选 `Deploy from a branch`，分支选 `main`、目录选 `/ (root)`，点 **Save**。
4. 等 1–2 分钟，页面顶部出现网址：`https://<用户名>.github.io/<仓库名>/`。

## 方式二：Vercel

把本目录拖到 vercel.com 的新项目上传区，框架选 **Other**，部署后同样得到网址。

## 拿到网址后

把网址发我，或在本机执行：

```bash
python tools/set_link_url.py https://<用户名>.github.io/<仓库名>/
```

脚本会把摘要中的「交互版」超链接改到该网址，并重新生成 docx、PDF 与支撑材料。
