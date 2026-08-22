# GSC 手动请求索引 · 每日队列

> 53 个 URL 按优先级拆成 5 天，每天 10-11 个，适配 GSC 每日请求索引配额。  
> 使用方法：每天复制当天分组 → 打开 GSC → URL Inspection → 逐个粘贴 → 点 "Request Indexing"。  
> 每个 URL 约 10 秒，一天一组约 2 分钟。

---

## ⚠️ 前提：先完成 www 统一

确保以下已生效（否则提交的是错误版本）：

- [ ] `sitemap.xml` 已改为 `https://www.gongdaa.com/`
- [ ] `robots.txt` 已改为 `https://www.gongdaa.com/sitemap.xml`
- [ ] 所有 HTML 的 canonical / og:url 已改为 www 版本
- [ ] 已 commit + push，GitHub Pages 部署完成

---

## 📅 Day 1 — 核心页面（🔴 + 前 6 个 🟡）

```
https://www.gongdaa.com/
https://www.gongdaa.com/products.html
https://www.gongdaa.com/products/decorative-pvc-film.html
https://www.gongdaa.com/products/pvc-edge-banding.html
https://www.gongdaa.com/products/wood-grain-pvc-film.html
https://www.gongdaa.com/products/marble-metallic-pvc-film.html
https://www.gongdaa.com/products/pvc-self-adhesive-film.html
https://www.gongdaa.com/products/pvc-membrane-foil.html
https://www.gongdaa.com/products/soft-touch-matt-pvc-film.html
https://www.gongdaa.com/applications.html
```

## 📅 Day 2 — 高价值页面（🟡 剩余 + 应用页）

```
https://www.gongdaa.com/contact.html
https://www.gongdaa.com/blog.html
https://www.gongdaa.com/blog/decorative-surface-trends-2026.html
https://www.gongdaa.com/zh/index.html
https://www.gongdaa.com/zh/products.html
https://www.gongdaa.com/applications/kitchen-cabinets.html
https://www.gongdaa.com/applications/wardrobes-closets.html
https://www.gongdaa.com/applications/doors-panels.html
https://www.gongdaa.com/applications/wall-panels.html
https://www.gongdaa.com/applications/office-furniture.html
```

## 📅 Day 3 — 英文博客与支持页（🟢）

```
https://www.gongdaa.com/applications/retail-hospitality.html
https://www.gongdaa.com/about.html
https://www.gongdaa.com/certifications.html
https://www.gongdaa.com/faq.html
https://www.gongdaa.com/blog/wood-grain-vs-marble-pvc-film.html
https://www.gongdaa.com/blog/pvc-edge-banding-thickness-guide.html
https://www.gongdaa.com/blog/water-based-vs-oil-based-pvc-ink.html
https://www.gongdaa.com/blog/how-to-apply-pvc-film-vacuum-pressing.html
https://www.gongdaa.com/blog/pvc-edge-banding-vs-abs.html
https://www.gongdaa.com/blog/what-is-soft-touch-pvc-film.html
https://www.gongdaa.com/blog/soft-touch-vs-glossy-vs-matte-pvc-film.html
```

## 📅 Day 4 — 英文博客（🟢 续）

```
https://www.gongdaa.com/blog/soft-touch-pvc-film-applications.html
https://www.gongdaa.com/blog/how-soft-touch-pvc-film-is-made.html
https://www.gongdaa.com/blog/soft-touch-pvc-film-durability-maintenance.html
https://www.gongdaa.com/blog/pvc-film-kitchen-cabinets-guide.html
https://www.gongdaa.com/blog/pvc-film-vs-veneer-vs-laminate.html
https://www.gongdaa.com/blog/customizing-pvc-decorative-film.html
https://www.gongdaa.com/zh/products/decorative-pvc-film.html
https://www.gongdaa.com/zh/products/soft-touch-matt-pvc-film.html
https://www.gongdaa.com/zh/products/pvc-edge-banding.html
https://www.gongdaa.com/zh/products/wood-grain-pvc-film.html
https://www.gongdaa.com/zh/products/marble-metallic-pvc-film.html
```

## 📅 Day 5 — 中文页面（🟢 续，收尾）

```
https://www.gongdaa.com/zh/products/pvc-membrane-foil.html
https://www.gongdaa.com/zh/products/pvc-self-adhesive-film.html
https://www.gongdaa.com/zh/applications.html
https://www.gongdaa.com/zh/applications/kitchen-cabinets.html
https://www.gongdaa.com/zh/applications/wardrobes-closets.html
https://www.gongdaa.com/zh/applications/doors-panels.html
https://www.gongdaa.com/zh/applications/wall-panels.html
https://www.gongdaa.com/zh/applications/office-furniture.html
https://www.gongdaa.com/zh/applications/retail-hospitality.html
https://www.gongdaa.com/zh/about.html
https://www.gongdaa.com/zh/contact.html
```

---

## 重要说明

1. **Request Indexing ≠ 保证收录** — 它只是"请 Google 重新来抓一次"，Google 会按自己的算法决定是否收录。请求一次即可，**不要反复请求**，过度请求可能被降权。
2. **配额** — GSC 每个站点每天有请求索引配额（通常 10-20 个）。如果某天提示超限，等第二天再继续，不要硬试。
3. **更省力的替代** — 重新提交 `sitemap.xml`（见《Sitemap提交清单.md》第二步）后，Google 会自动发现并抓取全部 53 个 URL，效果一样甚至更好。手动请求索引只建议用于 🔴🟡 的高价值页面，🟢 页面完全可以只靠 sitemap。
4. **结果检查** — 提交后 1-2 天，到 GSC → 效果 → 网页 里看收录数和点击量变化。
