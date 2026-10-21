# personal-site

一个最简单的静态个人主页。纯 HTML + CSS，无依赖、无构建步骤。

## 本地查看

直接双击 `index.html`，或在目录里运行：

```bash
python -m http.server 8000
```

然后打开 http://localhost:8000

## 要改的地方

全部内容都在 `index.html` 里，改这几处即可：

| 位置 | 内容 |
| --- | --- |
| `<title>` | 浏览器标签页标题 |
| `<h1>` | 你的名字 |
| `.tagline` | 一句话简介 |
| 「关于」段落 | 自我介绍 |
| 「在做的事」 | 项目列表，改标题、链接、年份 |
| 「联系」 | GitHub / Email 地址 |
| `<footer>` | 版权年份与名字 |

配色在文件顶部 `:root` 里，改 `--accent` 就能换主题色；深色模式在 `prefers-color-scheme: dark` 里。

## 发布到 GitHub Pages

1. 在 GitHub 新建仓库，命名 `你的用户名.github.io`（这样网址最短），或任意名字。
2. 推送代码：

```bash
git init
git add -A
git commit -m "init: personal site"
git branch -M main
git remote add origin https://github.com/<用户名>/<仓库名>.git
git push -u origin main
```

3. 仓库 Settings → Pages → Source 选 `Deploy from a branch`，Branch 选 `main` / `root`，保存。
4. 等 1–2 分钟，访问 `https://<用户名>.github.io/`（若仓库非 `用户名.github.io`，则网址为 `https://<用户名>.github.io/<仓库名>/`）。
