# GSC & Bing Sitemap 提交清单

> 网站已从 Vercel 迁移到 GitHub Pages，需要通知搜索引擎重新抓取。
> 生成日期：2026-08-17

---

## ⚠️ 第一步（必做）：修复 www 不一致问题

### 现状
- sitemap.xml 里所有 URL 写的是 `https://gongdaa.com/`（**不带 www**）
- GitHub Pages 自定义域名绑定的是 `www.gongdaa.com`（**带 www**）
- 两个都能访问，但搜索引擎会认为是两个不同网站 → 重复内容惩罚

### 需要统一选择一个版本

**推荐方案：统一用 `https://www.gongdaa.com/`（带 www）**

理由：GitHub Pages 默认绑定的就是 www 版本，DNS CNAME 也指向 www。

#### 修改步骤：
1. 打开 `sitemap.xml`，把所有 `https://gongdaa.com/` 替换为 `https://www.gongdaa.com/`
2. 检查所有 HTML 文件的 `<link rel="canonical">` 标签，确认指向 www 版本
3. 检查 `robots.txt` 里的 sitemap 指令
4. 提交到 git → push → GitHub Pages 自动部署

---

## 第二步：Google Search Console 提交

### 前置条件
- 有 Google 账号
- 已验证 `gongdaa.com` 域名所有权（之前用 TXT 记录验证过）

### 2.1 确认站点属性
登录 https://search.google.com/search-console

检查是否有以下属性：
- ✅ `gongdaa.com`（域名级属性，覆盖 www 和非 www）
- 或者 `https://www.gongdaa.com/`（URL 前缀属性）

如果没有 → 添加新属性 → 选择"域名"→ 输入 `gongdaa.com` → 按 TXT 记录验证

### 2.2 提交 Sitemap
左侧菜单 → **Sitemaps**

| 字段 | 填写内容 |
|------|----------|
| 输入 sitemap URL | `sitemap.xml` |
| 完整 URL | `https://www.gongdaa.com/sitemap.xml` |

点 **Submit** → 等待状态变为 "Success"（通常几分钟到几小时）

### 2.3 手动请求索引（重要页面优先）
左侧菜单 → **URL Inspection** → 逐个输入以下 URL → 点 "Request Indexing"

#### 英文版页面（必须提交）

| # | URL | 优先级 |
|---|-----|--------|
| 1 | `https://www.gongdaa.com/` | 🔴 最高 |
| 2 | `https://www.gongdaa.com/products.html` | 🔴 最高 |
| 3 | `https://www.gongdaa.com/products/decorative-pvc-film.html` | 🔴 最高 |
| 4 | `https://www.gongdaa.com/products/pvc-edge-banding.html` | 🔴 最高 |
| 5 | `https://www.gongdaa.com/products/wood-grain-pvc-film.html` | 🟡 高 |
| 6 | `https://www.gongdaa.com/products/marble-metallic-pvc-film.html` | 🟡 高 |
| 7 | `https://www.gongdaa.com/products/pvc-self-adhesive-film.html` | 🟡 高 |
| 8 | `https://www.gongdaa.com/products/pvc-membrane-foil.html` | 🟡 高 |
| 9 | `https://www.gongdaa.com/products/soft-touch-matt-pvc-film.html` | 🟡 高 |
| 10 | `https://www.gongdaa.com/applications.html` | 🟡 高 |
| 11 | `https://www.gongdaa.com/applications/kitchen-cabinets.html` | 🟢 中 |
| 12 | `https://www.gongdaa.com/applications/wardrobes-closets.html` | 🟢 中 |
| 13 | `https://www.gongdaa.com/applications/doors-panels.html` | 🟢 中 |
| 14 | `https://www.gongdaa.com/applications/wall-panels.html` | 🟢 中 |
| 15 | `https://www.gongdaa.com/applications/office-furniture.html` | 🟢 中 |
| 16 | `https://www.gongdaa.com/applications/retail-hospitality.html` | 🟢 中 |
| 17 | `https://www.gongdaa.com/about.html` | 🟢 中 |
| 18 | `https://www.gongdaa.com/certifications.html` | 🟢 中 |
| 19 | `https://www.gongdaa.com/contact.html` | 🟡 高 |
| 20 | `https://www.gongdaa.com/faq.html` | 🟢 中 |
| 21 | `https://www.gongdaa.com/blog.html` | 🟡 高 |

#### 英文版博客文章

| # | URL | 优先级 |
|---|-----|--------|
| 22 | `https://www.gongdaa.com/blog/decorative-surface-trends-2026.html` | 🟡 高 |
| 23 | `https://www.gongdaa.com/blog/wood-grain-vs-marble-pvc-film.html` | 🟢 中 |
| 24 | `https://www.gongdaa.com/blog/pvc-edge-banding-thickness-guide.html` | 🟢 中 |
| 25 | `https://www.gongdaa.com/blog/water-based-vs-oil-based-pvc-ink.html` | 🟢 中 |
| 26 | `https://www.gongdaa.com/blog/how-to-apply-pvc-film-vacuum-pressing.html` | 🟢 中 |
| 27 | `https://www.gongdaa.com/blog/pvc-edge-banding-vs-abs.html` | 🟢 中 |
| 28 | `https://www.gongdaa.com/blog/what-is-soft-touch-pvc-film.html` | 🟢 中 |
| 29 | `https://www.gongdaa.com/blog/soft-touch-vs-glossy-vs-matte-pvc-film.html` | 🟢 中 |
| 30 | `https://www.gongdaa.com/blog/soft-touch-pvc-film-applications.html` | 🟢 中 |
| 31 | `https://www.gongdaa.com/blog/how-soft-touch-pvc-film-is-made.html` | 🟢 中 |
| 32 | `https://www.gongdaa.com/blog/soft-touch-pvc-film-durability-maintenance.html` | 🟢 中 |
| 33 | `https://www.gongdaa.com/blog/pvc-film-kitchen-cabinets-guide.html` | 🟢 中 |
| 34 | `https://www.gongdaa.com/blog/pvc-film-vs-veneer-vs-laminate.html` | 🟢 中 |
| 35 | `https://www.gongdaa.com/blog/customizing-pvc-decorative-film.html` | 🟢 中 |

#### 中文版页面

| # | URL | 优先级 |
|---|-----|--------|
| 36 | `https://www.gongdaa.com/zh/index.html` | 🟡 高 |
| 37 | `https://www.gongdaa.com/zh/products.html` | 🟡 高 |
| 38 | `https://www.gongdaa.com/zh/products/decorative-pvc-film.html` | 🟢 中 |
| 39 | `https://www.gongdaa.com/zh/products/soft-touch-matt-pvc-film.html` | 🟢 中 |
| 40 | `https://www.gongdaa.com/zh/products/pvc-edge-banding.html` | 🟢 中 |
| 41 | `https://www.gongdaa.com/zh/products/wood-grain-pvc-film.html` | 🟢 中 |
| 42 | `https://www.gongdaa.com/zh/products/marble-metallic-pvc-film.html` | 🟢 中 |
| 43 | `https://www.gongdaa.com/zh/products/pvc-membrane-foil.html` | 🟢 中 |
| 44 | `https://www.gongdaa.com/zh/products/pvc-self-adhesive-film.html` | 🟢 中 |
| 45 | `https://www.gongdaa.com/zh/applications.html` | 🟢 中 |
| 46 | `https://www.gongdaa.com/zh/applications/kitchen-cabinets.html` | 🟢 中 |
| 47 | `https://www.gongdaa.com/zh/applications/wardrobes-closets.html` | 🟢 中 |
| 48 | `https://www.gongdaa.com/zh/applications/doors-panels.html` | 🟢 中 |
| 49 | `https://www.gongdaa.com/zh/applications/wall-panels.html` | 🟢 中 |
| 50 | `https://www.gongdaa.com/zh/applications/office-furniture.html` | 🟢 中 |
| 51 | `https://www.gongdaa.com/zh/applications/retail-hospitality.html` | 🟢 中 |
| 52 | `https://www.gongdaa.com/zh/about.html` | 🟢 中 |
| 53 | `https://www.gongdaa.com/zh/contact.html` | 🟢 中 |

**总计：53 个 URL**

> ⚠️ GSC 每天有请求索引配额（通常 10-20 个/天），优先提交红色和黄色标记的页面。

---

## 第三步：Bing Webmaster Tools 提交

登录 https://www.bing.com/webmasters

### 3.1 添加站点
- 如果已有 `gongdaa.com` → 直接进入
- 如果没有 → Add Site → 输入 `https://www.gongdaa.com/` → 验证所有权

### 3.2 提交 Sitemap
左侧 → **Configure My Site** → **Sitemaps**

输入：`https://www.gongdaa.com/sitemap.xml`

点 **Submit**

### 3.3 批量提交 URL（Bing 支持批量）
左侧 → **Configure My Site** → **Submit URLs**

一次性粘贴以下所有 URL（Bing 允许一次最多 10000 个）：

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
https://www.gongdaa.com/applications/kitchen-cabinets.html
https://www.gongdaa.com/applications/wardrobes-closets.html
https://www.gongdaa.com/applications/doors-panels.html
https://www.gongdaa.com/applications/wall-panels.html
https://www.gongdaa.com/applications/office-furniture.html
https://www.gongdaa.com/applications/retail-hospitality.html
https://www.gongdaa.com/about.html
https://www.gongdaa.com/certifications.html
https://www.gongdaa.com/contact.html
https://www.gongdaa.com/faq.html
https://www.gongdaa.com/blog.html
https://www.gongdaa.com/blog/decorative-surface-trends-2026.html
https://www.gongdaa.com/blog/wood-grain-vs-marble-pvc-film.html
https://www.gongdaa.com/blog/pvc-edge-banding-thickness-guide.html
https://www.gongdaa.com/blog/water-based-vs-oil-based-pvc-ink.html
https://www.gongdaa.com/blog/how-to-apply-pvc-film-vacuum-pressing.html
https://www.gongdaa.com/blog/pvc-edge-banding-vs-abs.html
https://www.gongdaa.com/blog/what-is-soft-touch-pvc-film.html
https://www.gongdaa.com/blog/soft-touch-vs-glossy-vs-matte-pvc-film.html
https://www.gongdaa.com/blog/soft-touch-pvc-film-applications.html
https://www.gongdaa.com/blog/how-soft-touch-pvc-film-is-made.html
https://www.gongdaa.com/blog/soft-touch-pvc-film-durability-maintenance.html
https://www.gongdaa.com/blog/pvc-film-kitchen-cabinets-guide.html
https://www.gongdaa.com/blog/pvc-film-vs-veneer-vs-laminate.html
https://www.gongdaa.com/blog/customizing-pvc-decorative-film.html
https://www.gongdaa.com/zh/index.html
https://www.gongdaa.com/zh/products.html
https://www.gongdaa.com/zh/products/decorative-pvc-film.html
https://www.gongdaa.com/zh/products/soft-touch-matt-pvc-film.html
https://www.gongdaa.com/zh/products/pvc-edge-banding.html
https://www.gongdaa.com/zh/products/wood-grain-pvc-film.html
https://www.gongdaa.com/zh/products/marble-metallic-pvc-film.html
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

## 第四步：robots.txt 检查

确认 `robots.txt` 里的 sitemap 指令已更新：

```
Sitemap: https://www.gongdaa.com/sitemap.xml
```

---

## 完成后检查清单

- [ ] sitemap.xml 里所有 URL 已改为 `https://www.gongdaa.com/`
- [ ] robots.txt 里 sitemap 指令已更新
- [ ] git commit + push 完成
- [ ] GitHub Pages 部署成功
- [ ] GSC 提交 sitemap → 状态 Success
- [ ] GSC 手动请求索引（至少前 10 个页面）
- [ ] Bing 提交 sitemap
- [ ] Bing 批量提交所有 URL
- [ ] 1-2 周后检查 GSC → Coverage → 确认收录数量正常
- [ ] 确认稳定后取消 Vercel Pro 订阅
