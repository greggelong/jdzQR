# Museum Collection Game – README

## English

### Overview

This is a QR‑code driven scavenger hunt where players restore a damaged museum artifact by finding its missing pieces. The page is bilingual — **Chinese primary, English secondary** — and works on any modern mobile browser.

### How it works

- One image is split into a **3 × 5 grid** (15 pieces).
- The **5 rows** correspond to **5 parts** of the hunt (e.g., Jinshang Bowl, Carpentry, Sound, Maps, Untitled).
- Each piece has a unique stage code: `1a`, `1b`, `1c`, `2a`, … `5c`.
- Scanning a QR code with `?stage=1a` marks that piece as collected and saves progress in `localStorage`.
- Players can scan in any order.
- A **Reset** button clears all progress.

### ⚠️ Current image is a placeholder

The image currently used is **`img15.jpg`**, a placeholder that ships with the project.  
**The design team will provide the final artwork.**  
To replace it:

1. Put your new image in the same folder as the HTML file.
2. Open the HTML file and find:
   ```js
   const ARTWORK_URL = "img15.jpg";
   ```
3. Change it to your filename, e.g.:
   ```js
   const ARTWORK_URL = "museum-artifact.jpg";
   ```
4. Save and upload.

Any aspect ratio works, but a square image gives the best result.

### Creating QR codes

Each QR code must contain the **full URL** of the page plus `?stage=CODE`.  
Your game is hosted at:  
**`https://greggelong.github.io/jdzQR/`**

The 15 full URLs are:

| Part | Code | Full URL                                       |
| ---- | ---- | ---------------------------------------------- |
| I    | 1a   | `https://greggelong.github.io/jdzQR/?stage=1a` |
| I    | 1b   | `https://greggelong.github.io/jdzQR/?stage=1b` |
| I    | 1c   | `https://greggelong.github.io/jdzQR/?stage=1c` |
| II   | 2a   | `https://greggelong.github.io/jdzQR/?stage=2a` |
| II   | 2b   | `https://greggelong.github.io/jdzQR/?stage=2b` |
| II   | 2c   | `https://greggelong.github.io/jdzQR/?stage=2c` |
| III  | 3a   | `https://greggelong.github.io/jdzQR/?stage=3a` |
| III  | 3b   | `https://greggelong.github.io/jdzQR/?stage=3b` |
| III  | 3c   | `https://greggelong.github.io/jdzQR/?stage=3c` |
| IV   | 4a   | `https://greggelong.github.io/jdzQR/?stage=4a` |
| IV   | 4b   | `https://greggelong.github.io/jdzQR/?stage=4b` |
| IV   | 4c   | `https://greggelong.github.io/jdzQR/?stage=4c` |
| V    | 5a   | `https://greggelong.github.io/jdzQR/?stage=5a` |
| V    | 5b   | `https://greggelong.github.io/jdzQR/?stage=5b` |
| V    | 5c   | `https://greggelong.github.io/jdzQR/?stage=5c` |

Generate QR codes with any free tool (e.g., QR Code Generator, NFC Tools, Canva).  
**Test one on your phone before printing.**

### Deployment

The game is already hosted on **GitHub Pages** at `https://greggelong.github.io/jdzQR/`.  
To update the files, commit and push to the repository. No further setup is needed.

For reference, the general steps for GitHub Pages are:

1. Create a repository.
2. Upload `index.html` and your image.
3. Go to **Settings → Pages**, choose the branch (usually `main`) and root folder.
4. Your site will be live at `https://username.github.io/repo-name/`.

### Customization

- **Part names**: Edit the `PARTS` array in the script. Change `nameCN` and `nameEN`.
- **Number of pieces**: Change `PIECES_PER_PART`, `TILE_POSITIONS`, and the CSS grid (advanced).
- **Storage key**: Change `STORAGE_KEY` if you run multiple hunts on the same domain.

### Resetting progress

Click the **重置进度** button on the page, or clear the site’s `localStorage` manually.

### Notes

- No personal data is collected.
- Works offline after first load if the image is cached.
- Chinese is the primary language; English is secondary.

---

## 中文

### 概述

这是一个由二维码驱动的寻宝游戏，玩家通过寻找散落的碎片来修复一件损坏的博物馆藏品。页面为**中英双语**，以**中文为主，英文为辅**，适用于任何现代手机浏览器。

### 玩法说明

- 一张图片被分割成 **3 列 × 5 行** 的网格（共 15 块碎片）。
- **5 行**对应寻宝的 **5 个部分**（例如：金缮碗、木工、声音、地图、待定）。
- 每个碎片都有唯一的关卡代码：`1a`、`1b`、`1c`、`2a` … `5c`。
- 扫描带有 `?stage=1a` 的二维码会将该碎片标记为已收集，并将进度保存在浏览器的 `localStorage` 中。
- 玩家可以按任意顺序扫描。
- 页面底部的 **重置** 按钮可清除所有进度。

### ⚠️ 当前图片为占位图

目前使用的图片是 **`img15.jpg`**，这是随项目提供的占位图。  
**设计团队将提供最终的美术图片。**  
替换方法：

1. 将新图片放入与 HTML 文件相同的文件夹。
2. 打开 HTML 文件，找到：
   ```js
   const ARTWORK_URL = "img15.jpg";
   ```
3. 改为你的文件名，例如：
   ```js
   const ARTWORK_URL = "museum-artifact.jpg";
   ```
4. 保存并上传。

任何宽高比均可，但正方形图片效果最佳。

### 生成二维码

每个二维码必须包含页面的**完整 URL** 加上 `?stage=代码`。  
你的游戏托管在：  
**`https://greggelong.github.io/jdzQR/`**

15 个完整网址如下：

| 部分   | 代码 | 完整网址                                       |
| ------ | ---- | ---------------------------------------------- |
| 第一组 | 1a   | `https://greggelong.github.io/jdzQR/?stage=1a` |
| 第一组 | 1b   | `https://greggelong.github.io/jdzQR/?stage=1b` |
| 第一组 | 1c   | `https://greggelong.github.io/jdzQR/?stage=1c` |
| 第二组 | 2a   | `https://greggelong.github.io/jdzQR/?stage=2a` |
| 第二组 | 2b   | `https://greggelong.github.io/jdzQR/?stage=2b` |
| 第二组 | 2c   | `https://greggelong.github.io/jdzQR/?stage=2c` |
| 第三组 | 3a   | `https://greggelong.github.io/jdzQR/?stage=3a` |
| 第三组 | 3b   | `https://greggelong.github.io/jdzQR/?stage=3b` |
| 第三组 | 3c   | `https://greggelong.github.io/jdzQR/?stage=3c` |
| 第四组 | 4a   | `https://greggelong.github.io/jdzQR/?stage=4a` |
| 第四组 | 4b   | `https://greggelong.github.io/jdzQR/?stage=4b` |
| 第四组 | 4c   | `https://greggelong.github.io/jdzQR/?stage=4c` |
| 第五组 | 5a   | `https://greggelong.github.io/jdzQR/?stage=5a` |
| 第五组 | 5b   | `https://greggelong.github.io/jdzQR/?stage=5b` |
| 第五组 | 5c   | `https://greggelong.github.io/jdzQR/?stage=5c` |

可使用任意免费工具生成二维码（如 QR Code Generator、NFC Tools、Canva）。  
**打印前请先用手机测试。**

### 部署

游戏已托管在 **GitHub Pages** 上：`https://greggelong.github.io/jdzQR/`。  
要更新文件，只需提交并推送到仓库即可，无需其他设置。

以下是 GitHub Pages 的通用步骤（供参考）：

1. 创建一个仓库。
2. 上传 `index.html` 和你的图片。
3. 进入 **Settings → Pages**，选择分支（通常是 `main`）和根目录。
4. 网站将上线于 `https://username.github.io/repo-name/`。

### 自定义

- **部分名称**：编辑脚本中的 `PARTS` 数组，修改 `nameCN` 和 `nameEN`。
- **碎片数量**：修改 `PIECES_PER_PART`、`TILE_POSITIONS` 和 CSS 网格（进阶）。
- **存储键**：如果在同一域名下运行多个寻宝活动，请修改 `STORAGE_KEY`。

### 重置进度

点击页面上的 **重置进度** 按钮，或手动清除该网站的 `localStorage`。

### 说明

- 不收集任何个人数据。
- 首次加载后，若图片已缓存，可离线工作。
- 中文为主，英文为辅。
