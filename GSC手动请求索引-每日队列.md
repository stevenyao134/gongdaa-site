# GSC 手动请求索引 · 队列

> **更新：2026-10-11。** 本文件只保留当前有效动作，历史队列已删除。

---

## ⚠️ 操作纪律（09-29 教训）

「站点地图」提交框**只接受 sitemap 文件**（如 `sitemap.xml`），填 HTML 页面地址必然报
「1 项错误」/「无法抓取」。站点地图表格里不允许有以 `.html` 结尾的条目，有就 ⋮ → 移除。

单页索引请求走 **顶部搜索栏（网址检查）→ 请求编入索引**，不走站点地图框。
一个 URL 请求一次即可，**不要反复请求**；每天约 10 个封顶，超了等第二天。

---

## 📅 批次 3 — 2026-10-11（7 个）

新增 5 篇行业博客（全新 URL，从未被抓取）+ `blog.html`（卡片 20→25）+
`blog/shipping…`（卷重表修正）。新 5 篇词数 1068–1326。

**今天做前 5 个 = 全新 URL，优先：**

```
https://www.gongdaa.com/blog/pvc-vs-pet-vs-pp-decorative-film.html
https://www.gongdaa.com/blog/pvc-film-thickness-selection-guide.html
https://www.gongdaa.com/blog/pvc-edge-banding-adhesive-guide.html
https://www.gongdaa.com/blog/pvc-film-price-cost-breakdown.html
https://www.gongdaa.com/blog/pvc-film-for-wall-panels-guide.html
```

**明天做后 2 个：**

```
https://www.gongdaa.com/blog.html
https://www.gongdaa.com/blog/shipping-pvc-film-from-china-moq-incoterms.html
```

| 页面 | 选题 | 词数 |
|---|---|---|
| `pvc-vs-pet-vs-pp-decorative-film` | 基材对比（PVC/PET/PP） | 1079 |
| `pvc-film-thickness-selection-guide` | 装饰膜 0.12–0.45mm 厚度选型 | 1088 |
| `pvc-edge-banding-adhesive-guide` | 封边条 EVA/PUR/热风胶种与设备设定 | 1092 |
| `pvc-film-price-cost-breakdown` | 报价五块成本构成 | 1326 |
| `pvc-film-for-wall-panels-guide` | 墙板基材/规格/安装 | 1142 |
| `blog.html` | 卡片 20 → 25 | — |
| `blog/shipping…` | 卷重表修正（64kg 而非 4-6kg） | — |

---

## 📅 批次 2 — 2026-10-07（12 个，做完就不用管）

applications + 5 个产品页（补厚）+ certifications/faq/products/zh×2（h1 对齐）+
customizing（承诺统一）。已请求过的不要重复。

---

## 📅 批次 1 — 09-29 的 8 个（做完就不用管）

5 篇新博客 + `certifications.html` + `blog.html` + buyers-guide。已请求过的不要重复。

---

## 📌 规则

1. **Request Indexing ≠ 保证收录**，Google 自行决定；过度请求可能被降权。
2. **验证是否已收录** — 请求后 1–3 天，URL Inspection 粘贴 URL 看状态；或搜 `site:gongdaa.com/路径`。
3. **网页索引编制报告** — 点开未编入索引的各原因截图给我分类。薄内容实测见
   `索引诊断-2026-09-29.md`（10-07 已把 7 个 EN 薄页补厚，zh 侧未动）。
4. **观察指标** — `sustainability-reach`（REACH/CBAM）对 EU 买家意图最强，重点看曝光；
   本批 `pvc-film-price-cost-breakdown` 商业意图最强，值得盯。
