# GSC 手动请求索引 · 队列

> **更新：2026-11-04。** 本文件只保留当前有效动作，历史队列已删除。

---

## ⚠️ 操作纪律（09-29 教训）

「站点地图」提交框**只接受 sitemap 文件**（如 `sitemap.xml`），填 HTML 页面地址必然报
「1 项错误」/「无法抓取」。站点地图表格里不允许有以 `.html` 结尾的条目，有就 ⋮ → 移除。

单页索引请求走 **顶部搜索栏（网址检查）→ 请求编入索引**，不走站点地图框。
一个 URL 请求一次即可，**不要反复请求**；每天约 10 个封顶，超了等第二天。

---

## 📅 批次 5 — 2026-11-04（7 个，优先做）

这一批修的是**会被 Google 直接判负的信号**，重抓价值最高：

1. **16 个中文页原本各有 5 个重复的 canonical 标签** → 已去重为 1 个。
   canonical 重复时 Google 会直接忽略该信号，等于这 16 页的规范化声明一直是失效的。
2. **faq.html / products.html 的 FAQPage 结构化数据与页面可见文本不一致**
   （JSON 是简写版，页面上是完整版）→ 已按可见文本重建，48 条问答 100% 一致。
   重抓后才有机会拿到 FAQ 富摘要。

今天先做这 7 个（覆盖 FAQ 与中文站的主要入口）：

```
https://www.gongdaa.com/faq.html
https://www.gongdaa.com/products.html
https://www.gongdaa.com/zh/
https://www.gongdaa.com/zh/products.html
https://www.gongdaa.com/zh/faq.html
https://www.gongdaa.com/zh/contact.html
https://www.gongdaa.com/zh/applications.html
```

**明天（配额恢复后）再做剩余 12 个中文页**（canonical 同样已修，只是不急着抓）：

```
https://www.gongdaa.com/zh/about.html
https://www.gongdaa.com/zh/certifications.html
https://www.gongdaa.com/zh/products/decorative-pvc-film.html
https://www.gongdaa.com/zh/products/wood-grain-pvc-film.html
https://www.gongdaa.com/zh/products/marble-metallic-pvc-film.html
https://www.gongdaa.com/zh/products/soft-touch-matt-pvc-film.html
https://www.gongdaa.com/zh/products/pvc-edge-banding.html
https://www.gongdaa.com/zh/products/pvc-membrane-foil.html
https://www.gongdaa.com/zh/products/pvc-self-adhesive-film.html
https://www.gongdaa.com/zh/applications/kitchen-cabinets.html
https://www.gongdaa.com/zh/applications/wardrobes-closets.html
https://www.gongdaa.com/zh/applications/doors-panels.html
```

---

## ✅ 无需手动请求（自然重抓即可）

- **批次 4（10-16 补厚的 4 页）**：contact / zh/contact / zh/products / zh/applications
  —— 已在批次 5 里覆盖其中 3 个中文页；contact.html 若还没做，可与批次 5 一起提交。
- **53 个英文页**：本轮只改了 `th scope`、`apple-touch-icon`、`mask-icon` 移除、`dateModified`，
  不涉及正文，让 Google 自然重抓即可。

---

## 📌 待观察（下一轮复查时看）

- **FAQ 富摘要**：faq.html 与 products.html 的 FAQ 数据现在与可见文本严格一致，
  抓取后 2–4 周内应能在 GSC「增强功能 → 常见问题」里看到有效条目。
- **中文站规范化**：16 页 canonical 从 5 个降到 1 个后，观察 GSC 里中文页的
  「重复网页，Google 选择的规范网页与用户指定的不同」是否消失。
- **SGS 报告 PDF**：已换成带水印的图片化低清版（不可提取文字）。文件仍在
  `/files/sgs-test-report-2024.pdf`，若日后希望彻底不被访问，需要移出站点目录或加登录保护。
