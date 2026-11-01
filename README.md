# strategy-CN · 中国企业出海整合管理（中文版入口）

线上地址：<https://yan-shipeng.github.io/strategy-CN/>

## 固定约定（不要改）

> **这个链接永远是「中文战略执行」版。**
> `https://yan-shipeng.github.io/strategy-CN/` → 中文版 Global Integration Challenge，
> 排行榜只读 `esg.db` 的 `en_sessions`（courseKey = `strategy-cn`）。
> 不要把它指向 ESG 版，也不要把其他课程的成绩混进这个标签。

三个入口各管各的榜，互不搬运：

| 入口 | 版本 | 路径 | 课程标签 |
|---|---|---|---|
| `go-overseas` | 战略执行（英文） | `/en` | `strategy` |
| `esg-simulation` | ESG 转型（英文） | `/esg/en` | `esg` |
| `strategy-CN`（本仓库） | 战略执行（中文） | `/cn` | `strategy-cn` |

## 这个仓库做什么

它只做一件事：提供一个中文入口页，把中文版模拟游戏用一层 iframe 嵌进来。

```
https://yan-shipeng.github.io/strategy-CN/            ← 本仓库（薄壳）
  └─ iframe → https://<deployment>/cn                 ← 中文版游戏（当前地址见 current.json）
https://yan-shipeng.github.io/strategy-CN/leaderboard ← 跳转到 /cn/leaderboard
```

## 部署

纯静态，无需构建：把内容推到 `gh-pages` 分支，GitHub Pages 自动发布。

> ⚠️ WorkBuddy Sites 每次重新发布会生成**新的域名**，届时运行
> `sites/update-live-url.sh <新域名>` 一次，三个入口的 `current.json` 会一起更新。
