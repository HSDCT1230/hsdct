# 红灯雾海 1.0

Archive of Our Own 站点皮肤。深蓝底、灯塔海图，正文用宋体系衬线，方便中文、英文和韩文阅读。

这是正式 1.0。皮肤只有这一份：`ushuaia-fin-del-mundo.css`。

## 安装

1. 打开 [新建站点皮肤](https://archiveofourown.org/skins/new)。
2. 类型选 **Site Skin**，标题可写成 `红灯雾海`。
3. 把下面的 CSS 全文贴进文本框，保存并 Update。
4. 在 My Skins 里选用它。

CSS（合并进 `main` 之后）：

<https://raw.githubusercontent.com/HSDCT1230/hsdct/main/ao3-hongdeng-wuhai/ushuaia-fin-del-mundo.css>

背景图写在 CSS 里，指向本仓库里的 `assets/les-eclaireurs-bg.jpg`，不用单独上传。本地预览改用同一张图的相对路径。

## 1.0 包含

- 火地岛 Les Éclaireurs 灯塔做页头背景，下沿渐变进 `#1b2e4b`，不重复铺图。
- 顶栏胶囊（Hi、Post、Log Out、Fandoms、Browse、Search、About）在窄屏里换行，文字不被裁切。
- 这些按钮展开后的菜单与主导航同宽：整块列表、行间分隔，不再缩成按钮那么窄。
- 搜索结果和作品列表里，页面标题大于作品标题，作品标题大于分区、标签和摘要。

## 目录

```
ao3-hongdeng-wuhai/
├── ushuaia-fin-del-mundo.css   # 贴进 AO3 的站点皮肤
├── assets/les-eclaireurs-bg.jpg
├── preview/index.html          # 本地大致预览，不是 AO3 页面
├── LICENSE
└── STANDALONE_SETUP.md         # 可选：拆成单独仓库
```

## 本地预览

在本目录执行：

```bash
python3 -m http.server 8765 --bind 127.0.0.1
```

打开 <http://127.0.0.1:8765/preview/index.html>。预览页改用本地背景图，AO3 上仍使用上面的 raw 地址。

## AO3 约束

- 这是站点皮肤。不要写 `#workskin`。正文用 `.userstuff`。
- 不要使用 `calc()`、`caret-color`、`-webkit-text-fill-color`，也不要留空的 `fieldset` 规则。
- 字体名用小写，例如 `source han serif sc`、`songti sc`。
- `#header` 和 `#inner` 是并列的。顶栏规则要写在 `#outer #header` 上，不要写成 `#outer #inner #header`。

## 许可

代码与文档见 [LICENSE](LICENSE)。灯塔照片版权归原作者。在 AO3 上使用时请遵守 AO3 和图片的使用规定。
