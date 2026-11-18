# AO3 站点皮肤 · 南极灯塔 · 极简文艺

**南极灯塔**远景为底，**冷酷**灰蓝与近白版心；红色只留在导航下划线、链接与当前态。界面去阴影、去粗边框；正文 **宋体系 + 宽行距**，偏诗集版式。针对中文阅读优化，桌面与手机通用（AO3 皮肤内无 `@media`）。

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

## 自定义背景图

在 CSS 文件顶部的「可配置区」修改 `--ushuaia-bg-image` 的 `url(...)`：

- 图片须为 **HTTPS**，扩展名 **.jpg / .jpeg / .png / .gif**（避免带复杂查询参数的链接，AO3 可能拒绝）。
- 可上传到自己的图床或 [AO3 允许的外链图床](https://archiveofourown.org/faq/skins-and-archive-interface)，把直链贴进 `url("...")`。

若背景过亮导致字不清，可把同文件中的 `--ushuaia-panel-bg` 调得不透明一些（例如把最后的 `0.92` 改成 `0.96`）。

## 许可

CSS 可自由复制、修改、再发布；背景图请遵循各图源的版权与署名要求。