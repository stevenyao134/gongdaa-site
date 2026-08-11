# Vercel 上线指南（图文版 · 小白专用）

> 适用对象：你已经有了 `decopvc-site-deploy.zip`（或解压后的网站文件夹），域名是 `gongdaa.com`，Cloudflare 添加域名时被限制，改用 Vercel 上线。
>
> Vercel 特点：**免费、不用备案、海外打开快、自动 HTTPS、拖文件夹就能上线**。

---

## 一、整体流程（先看这张图心里有数）

```
注册 Vercel 账号
   ↓
新建 Project → 选 "Upload" 上传文件夹
   ↓
把 decopvc-site-deploy 解压后的文件夹拖进去
   ↓
点 Deploy（约 30 秒）
   ↓
得到 xxx.vercel.app 临时地址 → 打开验证网站正常
   ↓
绑定自己的域名 gongdaa.com（Domains 设置）
   ↓
去域名注册商后台改 Nameserver / DNS 指向 Vercel
   ↓
等 10 分钟~几小时生效 → 用 gongdaa.com 访问正式站
```

---

## 二、第 1 步：注册 Vercel 账号

1. 打开 **https://vercel.com**
2. 右上角点 **"Sign Up"**（注册）
3. 推荐用 **GitHub / Google / 邮箱** 任一方式登录（邮箱最省事，不用另开账号）
4. 填邮箱 → 收验证邮件 → 点链接激活

> 全程免费，选 **Hobby（个人免费）** 套餐即可，别被 "Pro" 误导。

---

## 三、第 2 步：上传网站文件夹

1. 登录后，进入控制台首页，点右上角 **"Add New..." → "Project"**
2. 在跳转页，找到并点击 **"Upload"** 这一项（如果是第一次用，可能要先安装一个本地小工具，按提示点 "Install" 即可，或选 "Direct Upload"）

   > ⚠️ 注意：不要点 "Import Git Repository"（那是给有 GitHub 代码仓库的人用的），你要的是 **Upload（上传本地文件夹）**。

3. 把之前解压好的 **`decopvc-site-deploy`** 文件夹直接**拖到上传框**，或点框内"Browse"选择该文件夹
   - 确认文件夹里有 `index.html`、`css/`、`products/`、`zh/`、`sitemap.xml`、`robots.txt`
   - ⚠️ 确保 `index.html` 在文件夹**根层**，不要多套一层

---

## 四、第 3 步：一键部署

1. 上传完，Vercel 会显示项目名（可改成 `decopvc` 之类）
2. 直接点 **"Deploy"**（部署）按钮
3. 等待约 30 秒~1 分钟，进度条走完出现 ✅ **"Congratulations!"**

此时 Vercel 会给你一个免费临时域名，类似：
```
https://decopvc-xxx.vercel.app
```
点这个地址，**打开看看网站是否正常显示**（深色高端双语站、中英文切换能用）。

> 这一步哪怕还没绑定自己域名，网站已经上线可访问了。

---

## 五、第 4 步：绑定自己的域名 gongdaa.com

1. 部署成功后，进项目控制台，左侧点 **"Settings" → "Domains"**
2. 在输入框填 `gongdaa.com`（主域名）和 `www.gongdaa.com`，点 **"Add"**
3. Vercel 会给你显示需要配置的 **DNS 记录**（通常是两条 A 记录，或两条 Nameserver）

Vercel 给的 DNS 信息大致长这样（以实际页面为准）：
```
类型 A    @      →  76.76.21.21
类型 A    www    →  76.76.21.21
```
或 CNAME：
```
www  →  cname.vercel-dns.com
```

---

## 六、第 5 步：去域名注册商后台改 DNS（关键）

拿到 Vercel 给的 DNS 记录后，去你**买 `gongdaa.com` 的那个网站**后台改：

### 情况 A：你是在 Namecheap / GoDaddy / 阿里云等买的域名
1. 登录你买域名的注册商后台
2. 找到 **"DNS / 域名解析 / Nameserver"** 设置
3. 按 Vercel 给的记录添加：
   - 如果用 **A 记录**方式：添加两条 A 记录（`@` 和 `www` 都指向 `76.76.21.21`）
   - 如果 Vercel 要求 Nameserver 方式：把原来的 Nameserver 换成 Vercel 给的

### 情况 B：你已经在 Cloudflare 注册了账号但被限制
- 暂时**不要用 Cloudflare 管 DNS**，直接在你买域名的注册商那里改 A 记录指向 Vercel 即可（见情况 A）。
- 等以后 Cloudflare 解封了再考虑切过去。

---

## 七、第 6 步：等待生效 + 验证

1. 改完 DNS 后，回到 Vercel 的 Domains 页面
2. 状态会从 "Invalid Configuration" 变成 **"Valid Configuration" / 绿色对勾**
3. 等待时间：**快则 10 分钟，慢则 24 小时内**（取决于注册商）
4. 生效后，浏览器打开 **https://gongdaa.com** —— 你的正式网站就上线了 🎉
5. 确认地址栏有 🔒 锁标（Vercel 自动配好 HTTPS）

---

## 八、上线前必做：替换占位内容

网站能打开只是第一步，下面这些**必须改**，否则显得不专业/联系不上你：

| 要替换的占位 | 改成什么 | 在哪里改 |
|---|---|---|
| `gongdaa.com` | `gongdaa.com` | 所有 `.html` 文件的 `<head>` 里（canonical / OG / hreflang） |
| `GONGDA` | 你的真实品牌名 | 全站 Logo、页脚版权、标题 |
| 邮箱 `steven@sundecor.cn` | 你的真实邮箱 | `contact.html`、页脚 |
| 电话 / WhatsApp 号码 | 你的真实号码 | 页脚、联系页 |
| 产品图（占位色块） | 真实产品照片 | 各产品页 `<div class="thumb">` 换成 `<img>` |

> 💡 如果你把真实品牌名、邮箱、电话、WhatsApp 发我，我可以**帮你全局替换好再重新打包**，你直接上传就是开箱即用版。

---

## 九、常见问题

**Q1：Vercel 免费版能用多久？要钱吗？**
免费版永久免费，适合个人/小公司官网。流量大的话才会到付费门槛，初期完全够用。

**Q2：以后网站内容要改，怎么办？**
重新上传文件夹覆盖即可（Vercel 每次上传都会生成新版本，旧的还在，可回滚）。

**Q3：SEO 的 sitemap.xml 还用提交吗？**
要。在 **Google Search Console** 里提交 `https://gongdaa.com/sitemap.xml`，加速收录。

**Q4：Cloudflare 那个限制以后能解吗？**
能。按之前提示发邮件到 `abusereply@cloudflare.com` 申诉，或等几天再试。解封后要不要迁移过去看你，Vercel 本身已经满足需求。

**Q5：中文版 / 英文版切换为什么有的页跳回首页？**
那是我在建双语时，部分中文页（blog/certifications/faq 等）还没补，暂时回退到中文首页避免 404。需要的话我可以补齐。

---

## 十、下一步我可以帮你做的

1. **全局替换占位** → 你给我品牌名 / 邮箱 / 电话 / WhatsApp，我改好重新打包。
2. **补齐剩余中文页**（blog、certifications、faq 及 4 个产品中文页）。
3. **加西语 / 俄语版**（针对南美、东欧客户），复制 `/zh/` 结构加 `/es/`、`/ru/`。
4. 如果你愿意，我也可以出一份 **Cloudflare 解封申诉邮件模板**。

把品牌信息发我，我们先把"开箱即用版"做出来。
