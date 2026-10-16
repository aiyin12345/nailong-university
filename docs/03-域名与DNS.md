# 03 · 域名与 DNS

## 主域名：`奶龙大学.work`

| 项目 | 值 |
|---|---|
| Unicode 形式 | `奶龙大学.work` |
| **Punycode 形式** | `xn--psszg58cj45k.work` |
| 注册商 | Alibaba Cloud Computing Ltd. d/b/a HiChina（阿里云 / 万网） |
| 注册时间 | **2026-10-15 11:25:29 UTC**（北京时间 19:25） |
| 到期时间 | 2027-10-15 |
| 阿里云 saleId | `S2026801HXV70911` |
| 注册局状态 | `serverTransferProhibited` + `addPeriod`（新增期，正常） |
| DNS 服务商 | **Cloudflare**（免费版） |

### Cloudflare 信息

| 项目 | 值 |
|---|---|
| 账号 | `efef234@163.com` |
| Account ID | `636f5fdf74b046d1bc1c68d8ed0e2443` |
| **Zone ID** | `ccaa353112d511958e0522534a92d3c9` |
| 分配 NS | `christina.ns.cloudflare.com`<br>`clark.ns.cloudflare.com` |
| 原 NS（阿里云） | `dns21.hichina.com` / `dns22.hichina.com` |
| 计划 | Free Website |
| 激活时间 | 2026-10-15 12:53 UTC 左右 |
| A 记录（当前） | Cloudflare 边缘 IP，如 `104.21.82.61` / `172.67.197.26` |

### 绑定的自定义域名（Cloudflare Workers Domains）

| hostname | 服务 |
|---|---|
| `xn--psszg58cj45k.work` | Worker（每次部署会变，当前 `tight-sun-4bb8`） |
| `www.xn--psszg58cj45k.work` | 同上 |

---

## 其他域名（同一 Cloudflare 账号）

| 域名 | Punycode | Zone ID | 当前行为 |
|---|---|---|---|
| `国立河南奶龙大学.com` | `xn--6krt8fs3b9iv6ffv5bu2vyj1e.com` | `06e62f71c30a64bbb9094c2e1a4c76ac` | 301 → `https://www.henu.edu.cn/` |
| `河南奶娃大学.com` | `xn--6kr28k0g6tq9cey3c.com` | — | 待处理（可 ¥18 删除退 ¥99，截止 2026-10-18 18:16） |

> 💡 **可选优化**：把 `国立河南奶龙大学.com` 的 301 规则改为指向主站，
> 可获得一个**含完整关键词的中文域名入口**（对 SEO 有正向作用）。
> 操作：Cloudflare → 该 zone → Rules → Redirect Rules → 把 target 改为 `https://xn--psszg58cj45k.work/`。

---

## 改 NS 的标准流程（阿里云 → Cloudflare）

> ⚠️ 这是**唯一必须用户本人参与**的步骤（需要短信验证码）。

1. 阿里云控制台 → 域名 → 找到域名 → **DNS 修改**
   URL 模板：
   ```
   https://dc.console.aliyun.com/#/domain/details/dns-modify?saleId=<saleId>&domain=<urlencode(域名)>
   ```
2. 点「**修改DNS服务器**」
3. 填入两个 Cloudflare NS（按 placeholder 定位输入框：
   第一个 `请输入修改后的域名DNS…`，第二个 `如：dns2.abc.com`）
4. 点「确定」→ 弹出「**请确认该操作 / 手机认证**」
5. 点「**获取验证码**」（短信发至 `197*****986`）
6. **由用户输入 6 位验证码** → 点「确定」
   - 验证码输入框特征：`type=text`、无 placeholder、位于弹窗下部
   - ⚠️ 弹窗里另有一个 `type=radio`（协议勾选，默认已选）—— 别填错
7. 成功后页面「当前DNS服务器」应立即显示 Cloudflare NS

## Cloudflare 激活（关键！）

新加站点后 zone 会停在 `pending`。必须走完向导：

1. 打开 `https://dash.cloudflare.com/<account>/<urlencode(域名)>/select-plan`
2. 点 `Select plan`
3. 进入 `/confirm-scanned-records` → 点 **`Continue to activation`**
4. 进入 `/nameserver-directions` → 点 **`I updated my nameservers`** ← **决定性一步**
5. 约 60 秒后 zone 变为 `active`

> 如果漏了第 4 步，zone 会一直 pending（本项目曾因此卡 50 分钟）。

---

## DNS 记录现状

Cloudflare 会自动为 Worker 自定义域名创建记录。当前域名下共 2 条 DNS 记录
（200 条上限）。`www` 与 apex 均解析到 Cloudflare 边缘。
