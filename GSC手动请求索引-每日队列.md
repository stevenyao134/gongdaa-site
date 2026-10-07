# GSC 手动请求索引 · 队列

> **更新：2026-10-07。** 本文件只保留当前有效动作，历史队列已删除。

---

## ⚠️ 操作纪律（09-29 教训）

「站点地图」提交框**只接受 sitemap 文件**（如 `sitemap.xml`），填 HTML 页面地址必然报
「1 项错误」/「无法抓取」。站点地图表格里不允许有以 `.html` 结尾的条目，有就 ⋮ → 移除。

单页索引请求走 **顶部搜索栏（网址检查）→ 请求编入索引**，不走站点地图框。
一个 URL 请求一次即可，**不要反复请求**；每天约 10 个封顶，超了等第二天。

---

## 📅 批次 2 — 2026-10-07（12 个，先做前 6 个）

10-07 内容更新（Practical Guide 补厚 + title/h1 对齐 + 承诺统一 10 小时），
sitemap lastmod 已全部改为 2026-10-07。

**前 6 个 = 实质内容新增，优先：**

```
https://www.gongdaa.com/applications.html
https://www.gongdaa.com/products/wood-grain-pvc-film.html
https://www.gongdaa.com/products/marble-metallic-pvc-film.html
https://www.gongdaa.com/products/pvc-self-adhesive-film.html
https://www.gongdaa.com/products/pvc-membrane-foil.html
https://www.gongdaa.com/products/soft-touch-matt-pvc-film.html
```

**后 6 个 = h1/文案对齐（明天做）：**

```
https://www.gongdaa.com/certifications.html
https://www.gongdaa.com/faq.html
https://www.gongdaa.com/products.html
https://www.gongdaa.com/zh/certifications.html
https://www.gongdaa.com/zh/contact.html
https://www.gongdaa.com/blog/customizing-pvc-decorative-film.html
```

| 页面 | 变更 | 词数 |
|---|---|---|
| `applications.html` | 新增「Matching the Film to the Job」选型指引节 | 152 → 352 |
| 5 个产品页 | 各新增「Practical Guide」三小节（真实规格表数据 + 内链） | 259–277 → 456–484 |
| `certifications.html` | h1 → Certifications & SGS Test Reports…（对齐 title） | — |
| `faq.html` / `products.html` / zh 两页 | h1 补 title 关键词 | — |
| `zh/contact.html` | 修复承诺矛盾：title/描述 24 小时 → 10 小时（与全站一致） | — |
| `blog/customizing…` | 引导语 quote within 24h → 10h | — |

---

## 📅 批次 1 — 09-29 的 8 个（做完就不用管）

5 篇新博客 + `certifications.html` + `blog.html` + buyers-guide。已请求过的不要重复。

---

## 📌 规则

1. **Request Indexing ≠ 保证收录**，Google 自行决定；过度请求可能被降权。
2. **验证是否已收录** — 请求后 1–3 天，URL Inspection 粘贴 URL 看状态；或搜 `site:gongdaa.com/路径`。
3. **网页索引编制报告** — 点开未编入索引的各原因截图给我分类。薄内容实测见
   `索引诊断-2026-09-29.md`（本轮已把 7 个 EN 薄页补厚，zh 侧未动）。
4. **观察指标** — `sustainability-reach`（REACH/CBAM）对 EU 买家意图最强，重点看曝光。
