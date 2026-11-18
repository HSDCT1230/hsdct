# AO3 站点皮肤 · 红灯雾海

半透明深蓝栏 + 浅色字；正文字体 `"microsoft yahei", "pingfang sc", "noto sans sc", sans-serif`，行高 2，字距约 0.02em。海图写在 `#outer` 上。

## 文件

| 文件 | 说明 |
|------|------|
| `ushuaia-fin-del-mundo.css` | 粘贴到 AO3 站点皮肤的完整 CSS |
| `preview/index.html` | 本地结构预览（非 AO3 页面） |
| `assets/les-eclaireurs-bg.jpg` | 灯塔背景原图 |

## 设置步骤

1. AO3 → **Skins** → 编辑皮肤 **红灯雾海**（或新建 Site Skin）。
2. CSS 框 **全选删除**，从下面链接复制**整份**新 CSS 粘贴：  
   https://raw.githubusercontent.com/HSDCT1230/hsdct/cursor/ao3-ushuaia-skin-8314/ao3-skin-ushuaia/ushuaia-fin-del-mundo.css  
3. **Update**（成功会回到皮肤列表）→ **Use**。
4. 站点皮肤请用 **`.userstuff`**，不要用 `#workskin`（那是作品皮肤）。`font-family` 里的字体名须**全小写**。

## 背景图

- 写在 `#outer` / `#outer.wrapper` 的 `background-image`。
- 默认：  
  `https://raw.githubusercontent.com/HSDCT1230/hsdct/cursor/ao3-ushuaia-skin-8314/ao3-skin-ushuaia/assets/les-eclaireurs-bg.jpg`
- 想更透、更看清海图：搜 `background-color: rgba(21, 37, 56` 把 alpha 数字调小（例如 `#main` 的 `0.24`）。
- 想图更靠灯塔：改 `#outer` 的 `background-position`（默认 `center 32%`）。

## AO3 保存注意

- 小数点后最多 **3** 位（例：`1.06em` 可以，`1.0625em` 不行）。
- 不要加 CSS 注释；不要用 `var()` / `:root` 变量。

## 许可

CSS 可自由修改；背景图请遵守图源版权。