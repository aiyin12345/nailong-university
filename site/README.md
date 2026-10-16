# 站点源文件

本目录为 **<https://奶龙大学.work>** 的完整静态源码，可直接部署（纯静态，无后端）。

## 文件

| 文件 | 说明 |
|---|---|
| `index.html` | 首页 |
| `school.html` / `idea.html` / `campus.html` / `news.html` / `faq.html` / `about.html` | 6 个子页面 |
| `robots.txt` | 爬虫规则（Allow: / + Sitemap 指向） |
| `sitemap.xml` | 站点地图（7 个 URL） |
| `a9384e2c87895bf99d4059522dd5760e.txt` | IndexNow 密钥文件（放在根目录用于验证推送） |

## 图片资源

`assets/` 目录共 9 张图片（JPEG/WebP，合计约 2.1 MB）**未包含在本仓库中**，
可直接从线上站点取回：

```
https://xn--psszg58cj45k.work/assets/logo.webp
https://xn--psszg58cj45k.work/assets/nailong_arms.webp
https://xn--psszg58cj45k.work/assets/nailong_laugh.webp
https://xn--psszg58cj45k.work/assets/nailong_side.webp
https://xn--psszg58cj45k.work/assets/hero_gate_night.jpg
https://xn--psszg58cj45k.work/assets/minglun_gate.jpg
https://xn--psszg58cj45k.work/assets/longzihu.jpg
https://xn--psszg58cj45k.work/assets/auditorium.jpg
https://xn--psszg58cj45k.work/assets/gate_4x.jpg
```

下载后放入 `assets/` 即可完整还原站点：

```powershell
$base = 'https://xn--psszg58cj45k.work/assets'
$names = 'logo.webp','nailong_arms.webp','nailong_laugh.webp','nailong_side.webp','hero_gate_night.jpg','minglun_gate.jpg','longzihu.jpg','auditorium.jpg','gate_4x.jpg'
New-Item -ItemType Directory -Force assets | Out-Null
$names | ForEach-Object { curl.exe -s -o "assets/$_" "$base/$_" }
```

## 部署方式

见 [`../docs/02-技术架构与部署.md`](../docs/02-技术架构与部署.md)。
简要：用 Python 打 zip（正斜杠路径）→ Cloudflare 控制台上传 → 绑定自定义域名。
