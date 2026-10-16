# 04 · SEO 与收录状态

> 最后更新：2026-10-16 22:30（上线约 1.1 天）

## 关键词策略

| 层级 | 关键词 | 竞争度 | 现状 |
|---|---|---|---|
| **品牌词** | `国立河南奶龙大学`、`奶龙大学.work` | 极低 | ✅ 已可检索 |
| **核心词** | `河南奶龙大学` | 中 | ✅ **Bing 第 1 页第 7 条** |
| **热搜词** | `奶龙大学` | **极高** | 🟡 未进前 10，需外链 |
| 长尾词 | `国立河南奶龙大学 学校简介` / `…校训` / `…校园` | 低 | 子页被抓取后进入 |
| 辅助词 | `河南大学`、`奶龙`、`铁塔湖`、`明伦校区`、`龙子湖校区` | 高/中 | 已铺在正文 |

**全部关键词**：奶龙大学, 奶龙大学官网, 河南奶龙大学, 国立河南奶龙大学, 河南大学, 奶龙,
铁塔湖, 明伦校区, 龙子湖校区, 二创整活, 河南大学官网入口, HENAN NAILOONG UNIVERSITY

---

## 已完成的 SEO 动作

| 动作 | 状态 |
|---|---|
| 每页 `<title>` 关键词前置 | ✅ |
| 每页 `meta description` / `keywords` | ✅ |
| `<link rel="canonical">`（punycode 形式） | ✅ |
| Open Graph（og:title/description/image/url） | ✅ |
| **JSON-LD**：WebSite + Organization（首页）、FAQPage（首页与 /faq）、AboutPage、CollegeOrUniversity | ✅ |
| `robots.txt`（`Allow: /` + Sitemap 指向） | ✅ |
| `sitemap.xml`（7 个 URL） | ✅ |
| **IndexNow** 推送 7 个 URL（Bing/Yandex） | ✅ 已推送 3 次，返回 200/202 |
| **Bing 站长平台**：验证 + sitemap 提交 + 逐页 Request indexing | ✅ |
| pretty URL（站内链接无 `.html`，避免 307 重定向链） | ✅ |
| 图片压缩（9.17 MB → 2.15 MB） | ✅ |
| 页脚与正文的合规声明（提升信任度） | ✅ |

---

## 收录进度（Bing 官方数据）

| 指标 | 数值 | 说明 |
|---|---|---|
| 首页索引状态 | ✅ `Indexed successfully` — "URL can appear on Bing" | Bing URL Inspection |
| SEO/GEO 问题 | ✅ `No SEO/GEO issues found` | |
| 结构化数据识别 | ✅ `2 Markup types found` | |
| Sitemap | ✅ `Success`（Known sitemaps: 1，错误 0，警告 0，`Total URLs discovered: 7`） | |
| 子页面（/school /faq /about …） | 🟡 `Discovered but not crawled` | 已批量 Request indexing |
| **Backlinks（外链）** | ❌ `No data available`（约 0） | **排名最大瓶颈** |
| Bing 搜索曝光 | 已有（搜「河南奶龙大学」进第 1 页） | ✅ 突破点 |

### 实测搜索结果（2026-10-16 22:30）

**搜「河南奶龙大学」→ 第 1 页第 7 条 = 本项目** ✅

```
7. 奶龙大学.work
   https://奶龙大学.work
   奶龙大学官网 | 国立河南奶龙大学（河南奶龙大学）· HENAN ...
   国立河南奶龙大学（也写作 奶龙大学、河南奶龙大学，英文 HENAN NAILOONG UNIVERSITY）
   是一个由网友制作的 粉…
```

**搜「奶龙大学」→ 前 10 名（本项目未入榜）**：

| 排名 | 站点 | 类型 |
|---|---|---|
| 1 | ihuan.online（南京奶龙大学） | 站点 |
| 2 | 皇家奶龙大学.com | 站点 |
| 3 | nlucn.com（中国奶龙大学） | 站点 |
| 4 | milkdragonuniversity.me | 站点 |
| 5-6 | news.qq.com / news.ifeng.com | **媒体报道（极目新闻）** |
| 7 | 中国奶龙大学.icu | 跳转站 |
| 8 | nailo.ng | 跳转站 |
| 9 | **奶龙教育网.com** | ⭐ **导航站（可申请收录本域名）** |
| 10 | bilibili.com 视频 | 视频 |

---

## 直接竞品分析：`河南奶龙大学.work`

Punycode：`xn--6kr28k0gz4evu0b1z3e.work`

| 项目 | 竞品 | 本项目 |
|---|---|---|
| 托管 | **GitHub Pages**（`Server: GitHub.com`，IP 185.199.108-111.153） | Cloudflare |
| 页面数 | 4（/、/about.html、/colleges.html、/admission.html） | **7** |
| 首页可见文字 | 663 字符 | **4000+ 字符** |
| robots/sitemap | 与本项目格式**完全一致**（同为 AI 生成） | 同 |
| 注册时间 | 2026-10-14 07:32 UTC（比本项目早 1 天） | 2026-10-15 11:25 UTC |
| Bing 文件验证 | ❌ 无 `BingSiteAuth.xml` | ✅ 有 meta 验证 |
| 标题 | `河南奶龙大学 · 欢迎来到奶龙的家` | 见 `05-页面与内容.md` |

**结论**：竞品页面更少、文字更少、也没做验证，唯一优势是 **GitHub Pages 托管**
（github.com 权重极高 + GitHub 页面被抓取频繁）。但其"能被搜到"并非靠推广，
而是靠**免费托管 + 一天时间**。本项目已在 1 天内达到同等可检索性。

---

## 外链现状（关键瓶颈）

| 渠道 | 结果 |
|---|---|
| 百度贴吧（河南大学吧） | 🟡 帖子存在，但**外链被降级为纯文本**（新账号限制） |
| 知乎「想法」 | ❌ **域名被替换成"链接"二字**，未生成外链 |
| 知乎「回答」 | ⬜ 未做（应在此投入，权重高） |
| 微博 | ⬜ 未做（**评论/正文链接可直接点击，优先级最高**） |
| 奶龙教育网.com（导航站） | ⬜ 未申请收录（**高度相关外链机会**） |

**待用高流量页面**（可用于评论/回答引流）：

- 知乎热门问题：<https://www.zhihu.com/question/2093426512183702784>
- 微博：<https://weibo.com/2/detail/5354634533142994> ｜ <https://weibo.com/2/detail/5354661214947042>
- 贴吧热帖：<https://tieba.baidu.com/p/9266467154>
- 媒体（可 @ 争取报道）：新浪财经 / 成都商报 / 楚天都市报 / 腾讯新闻 / 凤凰新闻

---

## 时间预期

| 时间 | 预期 |
|---|---|
| 已完成（1 天） | 收录 + 品牌词可检索 + 「河南奶龙大学」第 1 页 |
| 3~7 天 | 子页面被抓取；长尾词开始有曝光 |
| 2~4 周 | 搜「国立河南奶龙大学」稳定在第 1 页；「奶龙大学」可能进第 2~3 页 |
| 1~3 月 | 有足够外链后，「奶龙大学」有机会进前几页 |
| 百度 | 未提交；提交后通常数周，受 `.work` 后缀 + 海外主机影响偏慢 |

---

## 流量统计方法

Cloudflare GraphQL Analytics（免费版可用字段有限，**必须做字段回退**）：

```graphql
query { viewer { zones(filter: {zoneTag: "ccaa353112d511958e0522534a92d3c9"}) {
  httpRequestsAdaptiveGroups(limit: 400,
    filter: {datetime_geq: "2026-10-16T00:00:00Z"}, orderBy: [count_DESC]) {
    count dimensions { userAgent clientRequestPath clientCountryName } } } } }
```

> ❌ 不可用字段：`referer`、`clientBrowser`（免费版会报 `unknown field`）
> ✅ 可用字段：`userAgent`、`clientRequestPath`、`clientCountryName`、`clientRefererHost`(部分)

**2026-10-16 观测到的爬虫**：bingbot、Googlebot、YandexBot、GPTBot(35 次)、
ClaudeBot(33 次)、AhrefsBot、FossickBot、l9scan(127 次，漏洞扫描)、curl 等。
