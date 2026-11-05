# 工作量计算器（Workload Calculator）

一个零依赖的单文件 HTML 小工具：算清每小时该做多少，进度一目了然。

> 🎮 在线直接用：https://workload-calculator.app.workbuddy.host/?sharecode=2IAAPF72JG

## 是什么

- **按时间算**：输入要求工作量 + 总工作时长（默认 8 小时）→ 算出每小时应做量；再输入已干时长 → 算出该时刻应完成的工作量
- **按进度算**：输入要求工作量 + 已完成量 → 算出这个量应花费的时间，附剩余量与预计还需时间
- **设置**：默认工作时长（默认 8）、时间单位（小时/分钟/自定义+换算）、工作量单位（条/件/页……）均可自定义，存本机浏览器 localStorage

## 怎么用

两种方式任选：

1. **直接用线上版**：点上面的入口链接即可，无需安装
2. **本地跑**：克隆仓库后直接用浏览器打开 `index.html`，或

```bash
python3 -m http.server 8080
# 打开 http://localhost:8080
```

## 特性

- 毛玻璃 UI + 流动渐变光斑背景 + 数字滚动动画
- 电脑 / 手机自适应，触控目标 ≥44px
- 零依赖零构建，单文件交付（约 25 KB）
- 通过页面质量检查（QUALITY_OK 无告警）

## 源码仓库

| 平台 | 地址 |
|---|---|
| GitHub | https://github.com/JohnnySilverhandV/workload-calculator |
| Gitee | https://gitee.com/johnny-silver-hand123/workload-calculator |

## 版本记录

- v1.0.0（2026-11-05）：首版——双模式计算 + 单位自定义 + 毛玻璃动效
