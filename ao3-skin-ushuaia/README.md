# AO3 站点皮肤 · 南极灯塔 · 极简文艺

**连贯画幅**：顶栏（照片上缘）+ 主区（纸白下半段）拼成**一整列**；元数据 / 简介 / 正文只用**细分隔线**。列表为**同一张画幅内分行**。侧缘固定海图连续可见。正文 **宋体系 + 行距 1.875**。

## 文件

| 文件 | 说明 |
|------|------|
| `ushuaia-fin-del-mundo.css` | 粘贴到 AO3「创建站点皮肤」的完整 CSS |
| `preview/index.html` | 本地预览（模拟 AO3 结构，非官方页面） |

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

皮肤默认使用仓库内 `assets/les-eclaireurs-bg.jpg`，AO3 中对应：

`https://raw.githubusercontent.com/HSDCT1230/hsdct/cursor/ao3-ushuaia-skin-8314/ao3-skin-ushuaia/assets/les-eclaireurs-bg.jpg`

（合并到 `main` 后可将路径中的分支名改成 `main`。）

若要换图：修改 CSS 里 `--ushuaia-bg-image` 的 `url(...)`，须为 **HTTPS** 且 **.jpg/.png/.gif** 直链。

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