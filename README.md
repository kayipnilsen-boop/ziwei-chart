# 紫微斗数命盘详批

乙酉年五月廿八日寅时（男命）的紫微斗数完整批盘，可直接发布为静态网站。

- **在线看**：`index.html` 是单文件、零依赖的排版页面，双击即可打开，也可以直接挂到 GitHub Pages。
- **文本版**：`命盘详批.md` 是同一份分析的 Markdown 版本，便于在 GitHub 上直接阅读、diff 与迭代。
- **原始数据**：`数据/命盘原始数据.txt` 是文墨天机导出的原始盘（安星码 `C5VUC`），用于复核与重排。

## 文件结构

```
.
├── index.html          # 命盘详批单页（含十二宫盘图、飞化、大限时间轴）
├── 命盘详批.md          # 同一内容的 Markdown 版本
├── README.md
└── 数据/
    └── 命盘原始数据.txt # 原始导出盘，供校验
```

## 十二宫速览

| 宫位 | 干支 | 主星 |
|---|---|---|
| 命宫 | 庚辰 | 武曲（庙）↓权、擎羊（庙） |
| 兄弟 | 己卯 | 天同（平）、禄存（庙） |
| 夫妻 | 戊寅 | 七杀（庙）、陀罗（陷） |
| 子女 | 己丑 | 天梁（旺·生年权）↓科、地劫（陷） |
| 财帛 | 戊子 | 廉贞（平）、天相（庙）、天魁、铃星 |
| 疾厄 | 丁亥 | 巨门（旺）↓忌 ↑禄、天马 |
| 迁移 | 丙戌 | 贪狼（庙） |
| 交友（来因） | 乙酉 | 太阴（旺·生年忌）↓忌、地空 |
| 官禄（身宫） | 甲申 | 紫微（旺·生年科）、天府（得）、文昌、左辅、天钺 |
| 田宅 | 癸未 | 天机（陷·生年禄） |
| 福德 | 壬午 | 破军（庙）、文曲（陷）、右弼（旺）↑科 |
| 父母 | 辛巳 | 太阳（旺）↓权、火星（得） |

## 本地预览

直接双击 `index.html`。或者用任意静态服务器：

```bash
# Python
python -m http.server 8080

# Node
npx serve .
```

然后访问 <http://localhost:8080>。

## 发布到 GitHub Pages

### 方案 A：网页端上传（无需在本机装 git）

1. 在 GitHub 新建一个仓库（Public 才能免费开 Pages；Private 需 Pro）。
2. 点 **Add file → Upload files**，把本目录下 `index.html`、`命盘详批.md`、`README.md` 以及 `数据/` 目录拖进去，提交。
3. 进入 **Settings → Pages**：
   - Source 选 **Deploy from a branch**
   - Branch 选 **main**，目录选 **/ (root)**
   - 保存，等 1–2 分钟
4. 访问 `https://<你的用户名>.github.io/<仓库名>/`。

`index.html` 就是全站唯一入口，无需构建步骤、无需配置 workflow。

### 方案 B：命令行推送

本机当前**未安装 git 与 gh**，需要先补装其一：

```powershell
# 用 winget 装 git（含 GitHub CLI 可选）
winget install --id Git.Git -e
winget install --id GitHub.cli -e
```

装完后（需要重开终端让 PATH 生效）：

```powershell
cd "C:\Users\Administrator\Doubao\chats\2026-11-21\new-chat"

git init
git add .
git commit -m "紫微斗数命盘详批：乙酉年五月廿八日寅时"

# 先在 GitHub 网页端建好空仓库，再执行（替换用户名与仓库名）
git remote add origin https://github.com/<用户名>/<仓库名>.git
git branch -M main
git push -u origin main
```

用 gh 可以省掉建仓库这一步：

```powershell
gh auth login
gh repo create <仓库名> --public --source . --remote origin --push
```

之后到 **Settings → Pages** 按方案 A 的第 3 步设置即可。

## 说明

本批盘依据三合紫微、飞星紫微、钦天四化与河洛数理交叉校验，属传统命理推演，**仅供研究、文化探讨与娱乐参考**，请勿作为婚姻、投资、医疗等重大决策的唯一依据。

真太阳时 04:56 仍属寅时（03:00–05:00），时辰无争议。
