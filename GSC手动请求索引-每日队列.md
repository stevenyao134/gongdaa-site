# GSC 手动请求索引 · 队列

> **更新：2026-09-30。** 本文件只保留当前有效动作，历史队列已删除。

---

## ⚠️ 先纠正一个操作（09-29 截图发现的问题）

「站点地图」提交框**只接受 sitemap 文件**（如 `sitemap.xml`），填 HTML 页面地址必然报
「1 项错误」/「无法抓取」。如果站点地图表格里还有以 `.html` 结尾的条目：

1. 每条点右侧 **⋮ → 移除站点地图**
2. 同一个框里改填 `sitemap.xml` → 提交 → 状态应显示「成功」、已发现的网页 ≈ 61

单页索引请求走 **顶部搜索栏（网址检查）→ 请求编入索引**，不走站点地图框。

---

## 0. 站点地图（最省力，覆盖全站 61 个 URL）

GSC → 站点地图 → `sitemap.xml` → 提交。

sitemap 与线上已逐字节一致（61 条 URL，全含 lastmod），Google 会按 lastmod 自动发现变更。
这一步不占配额，先做完再考虑手动请求。

---

## 📅 批次 1 — 8 个（2026-09-29 起，未做完就继续做）

每个 URL：顶部搜索栏粘贴 → 回车 → 右上「请求编入索引」→ 等转完 → 下一个。

```
https://www.gongdaa.com/blog/pvc-film-market-outlook-2026-2030.html
https://www.gongdaa.com/blog/how-to-vet-a-pvc-film-supplier.html
https://www.gongdaa.com/blog/pvc-film-sustainability-reach-formaldehyde.html
https://www.gongdaa.com/blog/shipping-pvc-film-from-china-moq-incoterms.html
https://www.gongdaa.com/blog/private-label-pvc-film-distributors.html
https://www.gongdaa.com/certifications.html
https://www.gongdaa.com/blog.html
https://www.gongdaa.com/blog/the-ultimate-pvc-film-buyers-guide.html
```

| URL | 为什么需要 | 内容量 |
|---|---|---|
| 5 篇新博客 | 全新 URL，之前不存在，从未被抓取 | 983–1276 词 |
| `certifications.html` | 新增 Guides & Insights 卡片区，lastmod 09-18 → 09-29 | 合规枢纽页 |
| `blog.html` | 卡片 14 → 20，ItemList numberOfItems 15 → 20，meta 描述重写 | 博客索引 |
| `the-ultimate-pvc-film-buyers-guide.html` | 页面早已存在，但 blog.html 一直没有它的卡片，本轮才补上入口 | 询盘转化主力文 |

**顺序**：5 篇新文 → `certifications.html` → `blog.html` → buyers-guide。

---

## ❌ 明确不需要请求索引的

- **26 个文件**（applications/ 6 + zh/applications/ 6 + blog/ 其余 15）：本轮只改了
  JSON-LD 的 `inLanguage` / `wordCount` / `articleSection` 三个字段，**正文一字未动**。
  schema 是抓取时顺带读的，不是排名信号，强行请求只白占配额。
- `products.html`：上次改动 09-21，早已被处理。

---

## 📌 规则

1. **Request Indexing ≠ 保证收录** — 一个 URL 请求一次即可，**不要反复请求**，过度请求可能被降权。
2. **配额** — 每站点每天约 10–20 个（新站偏低）。批次 1 的 8 个刚好在额度内。超了等第二天。
3. **验证是否已收录** — 请求后 1–3 天，URL Inspection 粘贴 URL 看状态；或搜
   `site:gongdaa.com/具体路径`。
4. **观察指标** — 一周后看 impressions。`sustainability-reach`（REACH/CBAM）对 EU 买家意图最强，重点看它的曝光。
5. **网页索引编制报告**（38 未编入 / 17 已编入，更新于 09-21）— 点开 4 个原因各截一张图，
   我逐个分类。薄内容页实测见 `索引诊断-2026-09-29.md`。
