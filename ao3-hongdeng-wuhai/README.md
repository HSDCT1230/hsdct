# 红灯雾海 · AO3 站点皮肤

北欧深蓝与灯塔海图氛围的 [Archive of Our Own](https://archiveofourown.org/) **站点皮肤**（Site Skin）。背景为火地岛 Les Éclaireurs 灯塔竖图，主内容区半透明叠层，正文使用适合中/英/韩阅读的宋体系衬线字体。

## 快速使用

1. 打开 AO3：[Dashboard → Skins → Site Skins → Create Site Skin](https://archiveofourown.org/skins/new)
2. 标题自定（例如 `红灯雾海`）
3. 将下面链接中的 CSS **全文复制**到 AO3 的 CSS 文本框，保存并 **Update**
4. 在站点皮肤列表中选中本皮肤

### 一键复制 CSS（Raw）

<https://raw.githubusercontent.com/HSDCT1230/ao3-hongdeng-wuhai/main/ushuaia-fin-del-mundo.css>

或克隆本仓库后打开根目录的 `ushuaia-fin-del-mundo.css`。

## 仓库结构

```
ao3-hongdeng-wuhai/
├── README.md
├── LICENSE
├── ushuaia-fin-del-mundo.css   # 粘贴到 AO3 的站点皮肤 CSS
├── assets/
│   └── les-eclaireurs-bg.jpg   # 背景图（768×1024）
└── preview/
    └── index.html              # 本地大致预览（非 AO3 官方页面）
```

## 本地预览

在仓库根目录启动静态服务后打开预览页，例如：

```bash
python3 -m http.server 8765 --bind 127.0.0.1
```

浏览器访问：<http://127.0.0.1:8765/preview/index.html>

## 背景图说明

- AO3 皮肤通过 CSS 引用 GitHub `raw` 地址加载 `assets/les-eclaireurs-bg.jpg`，避免部分图床在中国大陆不可用。
- 若你 fork 本仓库并替换图片，请同步修改 `ushuaia-fin-del-mundo.css` 里 `#outer` 的 `background-image` 为你的 raw 链接。
- 竖图采用顶图一张 + `no-repeat` + `100% auto`，避免 `repeat-y` 重复灯塔；下方由深蓝底色 `#1b2e4b` 延伸。

## AO3 限制与注意

- 这是 **站点皮肤**，请勿使用 `#workskin`（作品皮肤专用），正文样式请用 `.userstuff` 等站点皮肤选择器。
- AO3 可能拒绝带注释、`var()` / `:root`、或精度过长的小数（例如 `1.0625em`）；本仓库 CSS 已按经验规避。
- 字体名使用小写以通过 AO3 校验，例如 `source han serif sc`、`songti sc` 等。

## 致谢

灯塔摄影来源于仓库内 `assets/les-eclaireurs-bg.jpg`（火地岛 Les Éclaireurs 主题）。

## 许可

代码与文档见 [LICENSE](LICENSE)。背景图若为你本人上传的作品，版权归原作者所有；使用 AO3 皮肤时请遵守 AO3 与图片版权相关规定。