# 珠海科技学院计算机协会 · 官方网站首页

> 技术驱动未来，代码改变世界 —— 高校计算机协会网站首页，单文件交付，开箱即用。

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/zh-CN/docs/Web/HTML)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS_3-CDN-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![JavaScript](https://img.shields.io/badge/Vanilla_JS-ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript)
[![License](https://img.shields.io/badge/License-MIT-22C55E?style=flat-square)](#-许可证)

---

## 📖 项目简介

本仓库是 **珠海科技学院计算机协会官网首页** 的前端实现。整个页面收敛为 **一个 `index.html`**（约 99 KB / 1645 行），样式与脚本内联，无需 npm、无需构建工具，双击即可在浏览器中打开。

页面包含导航、轮播、数据统计、协会简介、新闻动态、活动预告、技术资源、快速入口、底部信息栏 **9 大模块**，并带有轮播自动播放、数字滚动增长、滚动淡入上滑、悬浮上浮等 **10 类原生 JS 交互**，完整适配 PC / 平板 / 手机三端。

- 🌐 在线访问：<https://github.com/fly2006heaven/techclub>
- 📄 源码文件：[`index.html`](./index.html)
- 🎯 定位：前端静态页面模板，**所有文案与图片均为占位数据**，可直接接入后端

---

## ✨ 功能特性

| 类别 | 能力 |
|---|---|
| 布局 | 顶部导航 + 主体内容 + 底部信息栏；9 大模块按序排布，语义化标签 + 模块级注释 |
| 响应式 | PC（≥1200px）/ 平板（768~1199px）/ 手机（<768px）三端适配 |
| 交互 | 导航滚动变色、Hero 自动轮播、数字滚动增长、活动倒计时、滚动淡入、卡片上浮、弹窗表单 |
| 无障碍 | `aria-*` 语义标注、键盘方向键切换轮播、Esc 关闭弹窗、焦点样式保留、支持 `prefers-reduced-motion` 降级 |
| 健壮性 | 占位图加载失败自动回退内联 SVG 渐变图，断网也不会出现破图 |
| 可维护 | 色板 / 圆角 / 阴影 / 字体统一收口到 Tailwind 配置；表单校验与后端接入点均有注释标注 |

---

## 🛠 技术栈

| 技术 | 版本 / 来源 | 用途 |
|---|---|---|
| HTML5 | 原生语义化标签 | 页面结构 |
| Tailwind CSS | 3.x（[Play CDN](https://cdn.tailwindcss.com)） | 原子化样式；通过 `tailwind.config` 扩展品牌主题 |
| 原生 JavaScript | ES6+（IIFE 封装，无任何框架） | 轮播、滚动动画、计数、倒计时、菜单、弹窗、表单校验 |
| Font Awesome | 6.5.2（CDN） | 全站图标 |
| Google Fonts | Inter / Roboto | 英文字体，中文回退系统黑体 |
| 占位图服务 | `picsum.photos` | 演示图片，失败时回退内联 SVG |

> **关于 Tailwind Play CDN**：它会在浏览器运行时编译样式，适合原型与教学演示。若要上生产环境，建议改为构建产物（PostCSS / Tailwind CLI），可显著提升首屏速度并支持离线访问。

---

## 🚀 快速开始

### 方式一：直接打开（推荐）

```bash
git clone https://github.com/fly2006heaven/techclub.git
cd techclub
# 双击 index.html，或用浏览器打开
```

### 方式二：起一个本地静态服务

```bash
# Python 3
python -m http.server 5500

# 或 Node.js
npx serve -l 5500
```

然后访问 <http://localhost:5500>。

> 首次打开需要联网加载 Tailwind、Font Awesome、Google Fonts 与占位图；断网时页面仍可正常渲染（图片会显示内置渐变兜底图），但样式会缺失。

---

## 📁 目录结构

```
techclub/
├── index.html    # 全部交付内容：结构 + 内联 CSS + 内联 JS（唯一需要关注的产物）
└── README.md     # 本文件
```

`index.html` 内部结构：

| 行号区间 | 内容 |
|---|---|
| 1 – 17 | `<head>` 文档元信息、SEO 描述、favicon（内联 SVG） |
| 18 – 54 | Tailwind CDN 与 `tailwind.config`（品牌色 / 圆角 / 阴影 / 字体 / 动画） |
| 61 – 122 | 内联 `<style>`：滚动淡入、导航下划线、轮播淡入淡出、卡片上浮等自定义规则 |
| 128 – 231 | **模块 1** 顶部导航栏 Navbar |
| 233 – 387 | **模块 2** Hero 轮播 |
| 389 – 442 | **模块 3** 数据概览 Stats Bar |
| 444 – 521 | **模块 4** 协会简介 About |
| 523 – 633 | **模块 5** 最新动态 News |
| 635 – 757 | **模块 6** 活动预告 Events |
| 759 – 863 | **模块 7** 技术资源 Resources |
| 865 – 942 | **模块 8** 快速入口 Quick Entry |
| 944 – 1053 | **模块 9** 底部信息栏 Footer |
| 1055 – 1117 | 通用弹窗（登录 / 注册 + 活动报名表单） |
| 1119 – 1643 | 全部交互脚本（10 个编号段落，见下文） |

> 行号为当前版本实测值；源码内每个模块顶部均有 `<!-- 模块 N：xxx -->` 注释，按注释检索比按行号更稳。

---

## 🧩 页面模块说明

| # | 模块 | 锚点 | 关键实现 |
|---|---|---|---|
| 1 | 顶部导航栏 | `#navbar` | 文字 Logo + 协会名；7 项菜单（当前页高亮 + 悬浮渐变下划线）；搜索框点击展开；登录/注册按钮与已登录头像下拉；滚动 >24px 时背景由透明转白并加阴影；<1024px 折叠为汉堡菜单 |
| 2 | 首屏 Hero 轮播 | `#hero` | 4 张幻灯片（CSS 渐变 + 网格/光斑装饰模拟背景图）；80vh 高；5 秒自动播放；淡入淡出 + 背景缓慢放大；圆点指示器 + 左右箭头 + 触屏滑动 + 键盘方向键；半透明深色遮罩；文案分级渐显 |
| 3 | 数据概览 Stats Bar | `#stats` | 4 张数据卡片（100+ 会员 / 120+ 活动 / 30+ 项目 / 15+ 获奖）；进入视口触发数字滚动增长（`easeOutCubic` 缓动） |
| 4 | 协会简介 About | `#about` | 左图右文；成立年份角标、荣誉标签；约 130 字简介（成立时间 / 宗旨 / 活动方向）；关键词三宫格；「了解更多」按钮 |
| 5 | 最新动态 News | `#news` | 标题栏 + 「查看更多 >」；4 张新闻卡（封面 / 分类标签 / 标题 / 日期 / 摘要）；PC 4 列 → 平板 2 列 → 手机 1 列；悬浮上浮 + 阴影加深 + 封面缩放 |
| 6 | 活动预告 Events | `#events` | 3 场活动（海报 / 名称 / 时间 / 地点 / 报名按钮）；「距开始还有 X 天」按真实时间戳动态计算并跨天自动刷新；点击报名弹出报名表单弹窗 |
| 7 | 技术资源 Resources | `#resources` | 6 个分类入口：学习路线 / 教程文章 / 资源下载 / 开源项目 / 技术博客 / 常见问题；PC 3 列 × 2 行，移动端 2 列 |
| 8 | 快速入口 Quick Entry | `#join` | 4 张渐变卡片：加入我们 / 活动报名 / 资源下载 / 联系我们；悬浮放大 + 轻微旋转 + 光斑扩散 |
| 9 | 底部信息栏 Footer | `#footer` | 深色 4 列：协会信息 + 社交图标 / 快速链接 / 联系方式 / 友情链接 + 二维码；分隔线下方为版权栏（© 2026 + 备案号） |

页面另有 **通用弹窗**（`#modal`）：承载登录注册与活动报名两套场景，含姓名 / 学号 / 手机号校验、成功态回执，并在提交后切换为"已登录"演示态。

---

## 🎨 设计规范

### 色板

| 用途 | 名称 | 色值 | Tailwind 类名 |
|---|---|---|---|
| 主色 · 深 | 科技蓝 | `#1E3A8A` | `bg-brand-deep` / `text-brand-deep` |
| 主色 · 亮 | 科技蓝 | `#2563EB` | `bg-brand-600` / `text-brand-600` |
| 主色 · 浅 | 科技蓝 | `#DBEAFE` | `bg-brand-100` |
| 深色区块 | 墨蓝 | `#0F172A` | `bg-brand-ink` |
| 辅助色 | 亮青 | `#06B6D4` | `text-cyanx` / `bg-cyanx` |
| 辅助色 | 荧光绿 | `#22C55E` | `text-neon` / `bg-neon` |
| 中性色 | 白 / 浅灰 | `#FFFFFF` / `#F8FAFC` | `bg-white` / `bg-slate-50` |

### 其他规范

| 项目 | 规范 |
|---|---|
| 圆角 | 卡片 `12px`（`rounded-card`）、按钮 `8px`（`rounded-btn`）、大图 `16px`（`rounded-2xl`） |
| 阴影 | 常态轻量（`shadow-card`：`0 4px 14px rgba(15,23,42,.06)`）；悬浮加深（`hover:shadow-card-hover`） |
| 字体 | 英文 Inter / Roboto；中文 `PingFang SC` → `Hiragino Sans GB` → `Microsoft YaHei` 逐级回退 |
| 动效时长 | 悬浮反馈 `0.25~0.35s`；滚动淡入 `0.75s`；轮播淡入淡出 `1s`；背景缩放 `7s` |

### 响应式断点

| 断点 | 布局调整 |
|---|---|
| ≥ 1200px | 完整多列布局（导航展开、新闻 4 列、资源 3 列、入口 4 列） |
| 768 ~ 1199px | 网格列数减少（新闻 2 列 / 资源 2 列 / 入口 2 列），导航仍展开 |
| < 768px | 单列堆叠，导航折叠为汉堡菜单，Hero 字号缩小，箭头常显 |

> 注：导航在 `< 1024px` 即折叠为汉堡菜单（对应规格中「<768px 导航折叠」的加强处理），其余模块严格遵循上表。

---

## ⚙️ 交互实现索引

交互脚本集中在 `index.html` 第 1126–1643 行，按编号可快速定位：

| 编号 | 功能 | 源码位置（注释标题） |
|---|---|---|
| 1 | 占位图加载失败回退内联 SVG | `1) 占位图加载失败兜底` |
| 2 | 导航栏滚动主题切换 + 当前页高亮 + 头像下拉 + 登录态切换 | `2) 导航栏：滚动时背景...` |
| 3 | 移动端汉堡菜单（含 resize 自动收起） | `3) 移动端汉堡菜单` |
| 4 | Hero 轮播：自动播放 / 箭头 / 圆点 / 触屏 / 键盘 / 悬浮暂停 / 标签页隐藏暂停 | `4) Hero 轮播：自动播放（5s）...` |
| 5 | 搜索框展开与占位提交 | `5) 搜索框：点击图标展开 / 收起` |
| 6 | 数字滚动增长（`IntersectionObserver` 触发） | `6) 数字滚动增长（进入视口触发...）` |
| 7 | 活动倒计时与日期渲染（跨天自动刷新） | `7) 活动倒计时：根据「距今 N 天」...` |
| 8 | 模块 / 卡片滚动淡入上滑（35 个 `data-reveal`，支持 `data-delay` 错峰） | `8) 模块 / 卡片滚动淡入` |
| 9 | 弹窗与表单校验（登录 / 报名双场景） | `9) 弹窗：登录 / 注册 + 活动报名表单` |
| 10 | 回到顶部按钮（滚动 >600px 显示） | `10) 回到顶部按钮` |

### 用到的 HTML 数据钩子

| 属性 | 数量 | 作用 |
|---|---|---|
| `data-reveal` / `data-delay` | 35 | 标记参与滚动淡入的元素及其延迟（毫秒） |
| `data-slide` | 4 | 轮播幻灯片 |
| `data-navlink` | 16 | 导航链接（桌面端 + 移动端），用于滚动高亮 |
| `data-theme-ink` | 12 | 随导航深浅色主题切换文字颜色的元素 |
| `data-img` | 11 | 绑定加载失败兜底逻辑的图片 |
| `data-open-modal` | 9 | 打开弹窗（`login` / `signup`），可带 `data-event-name` |
| `data-start-in-days` | 4 | 活动"距今 N 天"，用于换算开始时间与倒计时 |
| `.counter` | 4 | 数字滚动增长的数值节点（`data-target` / `data-duration`） |

---

## 🔌 接入后端指引

页面预留了清晰的后端对接位置，按以下清单替换即可：

**1. 表单提交接口** — `index.html` 第 1598 行 `/* ====== 接入后端的位置 ====== */`

```js
// 现有占位实现：直接展示成功态
// 替换为真实请求：
const res = await fetch('/api/signup', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    name: $('#fName').value,
    sid:  $('#fSid').value,
    phone:$('#fPhone').value,
    direction: $('#fDir').value,
    event: currentEventName   // 报名场景下的活动名
  })
});
```

**2. 替换占位数据**

| 内容 | 查找方式 |
|---|---|
| 协会名称 | 全局检索 `珠海科技学院计算机协会`，替换为你校真实名称 |
| 导航菜单 | 检索 `data-navlink`，补充真实页面 URL（当前均为 `#锚点`） |
| 新闻列表 | 模块 5 中 4 个 `<article>`，建议后续由列表接口渲染 |
| 活动列表 | 模块 6 中 3 个 `<article>`；`data-start-in-days` 改为接口返回的开始时间戳 |
| 统计数字 | 模块 3 中 `.counter` 的 `data-target` 属性 |
| 联系方式 | 模块 9 中的邮箱、QQ 群、地址、备案号 |

**3. 图片资源** — 全部图片带 `data-img` 属性并走 `img[data-img]` 兜底逻辑。替换为真实图片后，可保留该属性以继续获得破图保护：

```html
<img src="/static/news/1.jpg" data-img alt="新闻封面" loading="lazy" />
```

**4. 搜索功能** — 第 5 段脚本中两处 `alert('搜索（占位）：' + ...)` 为占位逻辑，替换为跳转搜索结果页即可。

**5. 登录态** — `setLoggedIn(bool)` 控制"登录/注册按钮"与"头像下拉菜单"的切换，接真实鉴权后改由接口返回的会话状态驱动。

---

## 🌐 浏览器兼容

| 浏览器 | 版本要求 | 说明 |
|---|---|---|
| Chrome / Edge | 88+ | 推荐，体验最佳 |
| Firefox | 78+ | 完全支持 |
| Safari | 14+ | 完全支持（含 `backdrop-filter`） |
| 移动端浏览器 | iOS Safari 14+ / Chrome Android | 支持触屏滑动切换轮播 |

依赖的现代 Web API：`IntersectionObserver`、`requestAnimationFrame`、CSS `custom properties`、`backdrop-filter`、`scroll-behavior: smooth`。其中 `IntersectionObserver` 已在 JS 中做了**降级处理**（不支持时直接显示内容，不做动画）。

---

## ❓ 常见问题

<details>
<summary><b>打开后样式全丢 / 图标变方块？</b></summary>

页面依赖 Tailwind CDN、Font Awesome CDN 与 Google Fonts，请确认网络可达。若处于内网环境，可将三者下载至本地并改为相对路径引用。
</details>

<details>
<summary><b>图片显示为蓝紫渐变块？</b></summary>

这是占位图加载失败后的**兜底 SVG**，说明 `picsum.photos` 不可达。替换为自己的图片路径即可消除。
</details>

<details>
<summary><b>倒计时数字是怎么算的？</b></summary>

活动卡片上的 `data-start-in-days="8"` 表示"距今 8 天"，脚本以此换算出当天 19:00 的真实时间戳，再据此渲染日期文案与剩余天数，并每 10 分钟自动刷新（跨天无需手动改）。
</details>

<details>
<summary><b>想改主题色怎么办？</b></summary>

只需修改 `index.html` 第 19–54 行 `tailwind.config` 中的色值，全站颜色会同步更新（品牌色均已收口为 `brand` / `cyanx` / `neon` 三个语义色板）。
</details>

---

## 🗺 后续规划

- [ ] 拆分多页：协会介绍、新闻列表/详情、活动列表/详情、资源中心
- [ ] 引入 Tailwind 构建流程，产出压缩 CSS 并支持离线
- [ ] 新闻与活动改由接口驱动，支持分页与筛选
- [ ] 接入真实登录鉴权与个人中心
- [ ] 增加深色模式与多语言（中 / 英）支持
- [ ] 补充 Lighthouse 优化：图片懒加载尺寸声明、字体 `display=swap`

---

## 📄 许可证

本项目采用 **MIT License**，可自由用于学习、二次开发与社团官网搭建。

页面内所有文案、数据、图片均为**占位内容**，不代表任何真实机构；正式上线前请替换为贵校协会的真实信息，并确保图片素材版权合规。

---

## 🙌 贡献与反馈

欢迎提交 Issue 或 Pull Request 改进页面。

1. Fork 本仓库
2. 新建分支：`git checkout -b feature/your-feature`
3. 提交改动：`git commit -m "feat: 你的改动说明"`
4. 推送分支：`git push origin feature/your-feature`
5. 发起 Pull Request

---

<div align="center">

**珠海科技学院计算机协会** · 技术驱动未来，代码改变世界

© 2026 珠海科技学院计算机协会 版权所有 | 备案号：京ICP备00000000号-1（占位）

</div>
