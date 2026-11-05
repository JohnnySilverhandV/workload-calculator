# workload-calculator · 工作量计算器

一个**单文件、零依赖**的工作量换算小工具。输入要求工作量和总工期，算清每小时该做多少；输入已干多久，看此刻应该做到哪儿；输入已完成量，反推该花多长时间。

> 🎮 **在线直接用（国内直连）**：<https://workload-calculator.app.workbuddy.host/?sharecode=2IAAPF72JG>
>
> 🌐 **GitHub Pages**：<https://johnnysilverhandv.github.io/workload-calculator/>
>
> 📦 **离线版下载**：[GitHub Releases](https://github.com/JohnnySilverhandV/workload-calculator/releases) ｜ [码云 Releases](https://gitee.com/johnny-silver-hand123/workload-calculator/releases)

## 源码仓库

| 平台 | 地址 |
|---|---|
| GitHub | https://github.com/JohnnySilverhandV/workload-calculator |
| Gitee（国内直连） | https://gitee.com/johnny-silver-hand123/workload-calculator |

---

## 🆕 更新日志

### v1.0.0 — 首版（2026-11-05）

- 双模式：按时间算「此刻应完成多少」，按进度算「这些量该花多久」
- 单位自定义：工作量单位任意改名，时间单位小时 / 分钟 / 自定义换算
- 设置存本机浏览器 localStorage（key `workloadCalc`），刷新不丢
- 毛玻璃 UI + 三层彩色光斑流动背景 + 数字滚动动画，电脑 / 手机自适应

---

## ✨ 功能

### ⏱ 按时间算

| 输入 | 输出 |
|---|---|
| 要求工作量 + 总工作时长（默认 8 小时） | 每小时应做量 |
| 再加上已干时长（如 3 小时） | 此刻应完成量 + 进度条 |

进度超时或正好完成会有提示，进度条带流光效果。

### 📊 按进度算

| 输入 | 输出 |
|---|---|
| 要求工作量 + 已完成量 | 这个量应花费的时间、剩余量、预计还需时间 |

### ⚙️ 设置

| 项 | 默认 | 可改 |
|---|---|---|
| 总工作时长 | 8 小时 | 任意数值 |
| 时间单位 | 小时 | 小时 / 分钟 / 自定义（1 个单位 = N 小时） |
| 工作量单位 | 条 | 条、件、单、页……任意文字 |

切换单位时数值自动换算，内部统一按小时计算。

## 🚀 使用

线上版点开即用；本地跑，克隆后直接用浏览器打开 `index.html`，或：

```bash
python3 -m http.server 8080
# 打开 http://localhost:8080
```

## 🛠 技术要点

- 单文件 HTML，无框架、无构建、无外部请求，所有计算在本机完成
- 数字滚动用 requestAnimationFrame 三次缓动，不是 CSS transition 硬切
- 毛玻璃效果靠 `backdrop-filter` + 三层彩色光斑打底，纯色背景上做 blur 等于没做
- 布局用 `clamp()` 与 `auto-fit` 网格自适应，触控目标 ≥44px
- 通过页面质量检查（QUALITY_OK 无告警）

## 📄 License

MIT © 2026 JohnnySilverhandV
