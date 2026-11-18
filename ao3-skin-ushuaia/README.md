# AO3 站点皮肤 · 南极灯塔 · 极简文艺

**半透明画幅 + 浅色字**：主区约 48% 深蓝叠底，海图透出来。中英正文 **无衬线、行距 1.8、段距 1.8em**。顶栏与主区仍为一列衔接。可调 `--ushuaia-sheet` 透明度与 `--ushuaia-ink` 明暗。

## 文件

| 文件 | 说明 |
|------|------|
| `ushuaia-fin-del-mundo.css` | 粘贴到 AO3「创建站点皮肤」的完整 CSS |
| `preview/index.html` | 本地预览（模拟 AO3 结构，非官方页面） |

## 为什么预览像「啥都没了」？

AO3 保存皮肤时会**删掉所有 CSS 注释**，有时连注释旁边的规则一起删；`--变量` / `var()` 若未通过校验，**整段配色也会失效**，页面上就只剩默认红白站 + 零星几条（例如搜索框发黑）。  
本仓库里的 `ushuaia-fin-del-mundo.css` 已做成 **无注释、颜色全部写成具体色值** 的版本，请**整份重新粘贴**后 Update，再 **重新打开编辑页** 对照：保存后的 CSS 应仍有大量 `{` 规则（约 80 段），并能看到 `background-image: url("https://i.imgur.com/ARshGKAh.jpg")`。

## 如何设置（AO3）

1. 登录 [AO3](https://archiveofourown.org/)，点击顶栏 **Hi, [用户名]!** → **My Dashboard**（我的仪表盘）。
2. 侧栏或菜单进入 **Skins**（皮肤）。
3. 选择 **Create Site Skin**（创建站点皮肤）。
4. **Title**：填一个**全站唯一**的名称，建议带上你的用户名，例如：`Ushuaia-CN-你的用户名`。
5. 在 **Write Custom CSS** 大文本框中，打开本仓库的 `ushuaia-fin-del-mundo.css`，**全选复制**后粘贴进去。
6. 页面底部 **Submit** 保存。
7. 回到 **My Site Skins**，在刚创建的皮肤下点 **Use** 启用；想先试效果可点 **Preview**。
8. 也可在 **My Preferences** → **Your site skin** 下拉里选该皮肤，底部 **Update**。

### 换回默认皮肤

- 任意页脚 **Customize** → **Default**；或  
- **Skins** 页 **Revert to Default Skin**。

## 背景图（已内置你的灯塔照片）

**AO3 能用的外链**（经验证较稳）：`upload.wikimedia.org`、Imgur 直链（`i.imgur.com/xxxx.jpg`）、部分图床。  
**常被拒绝**：`raw.githubusercontent.com`、`cdn.jsdelivr.net`（含 `@分支` 的地址）。

默认 CSS 已使用你上传的灯塔照片直链：  
`https://i.imgur.com/ARshGKAh.jpg`（相册页 [hfz9rOI](https://imgur.com/a/hfz9rOI) 不能写在 CSS 里，必须用 `i.imgur.com/…jpg`）。

若以后换图：

1. 上传到 [Imgur](https://imgur.com/)，在单张图页 **复制图片地址**（形如 `https://i.imgur.com/xxxxxxxx.jpg`）。
2. 只改 **`body` / `body.logged-in`** 里的  
   `background-image: url("…");`  
   **不要**写在 `:root` 里，**不要**再给 `#header` 加 `background-image`。
3. **Update** 后在编辑器搜索 `background-image`，确认 AO3 没有删掉该行。

备用（维基）：`https://upload.wikimedia.org/wikipedia/commons/3/3e/Faro_Les_Eclaireurs_Ushuaia.jpg`

## 配色说明（与照片一致）

| 用途 | 色值 | 对应画面 |
|------|------|----------|
| 浪 / 顶栏 | `#1B2E4B` | 深海蓝 |
| 版心底 | `#F0F4F7` | 冰云灰白 |
| 正文 | `#35404A` | 礁石深灰 |
| 边框 | `#B8CAD9` | 远山冷蓝 |
| 强调 | `#A64B3F` | 灯塔赤陶红 |

## 中文版式

- 界面：黑体栈 16px，行高 1.75  
- 正文：宋体系 1.125em，行高 **1.875**，字距 0.04em，段后 0.85em  
- 版心：最大约 36em 正文栏；作品区左右内边距约 1.75em（手机流式收缩）

若背景过亮，可将 `--ushuaia-panel-light` 末尾透明度改为 `0.99`。

## 许可

CSS 可自由复制、修改、再发布；背景图请遵循各图源的版权与署名要求。