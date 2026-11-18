# 发布为独立 GitHub 仓库

当前环境无法代替你在 GitHub 上「新建仓库」，本地已初始化 git 历史（`main` 分支）。你只需在 GitHub 网页上新建空仓库后推送即可。

## 步骤

1. 打开 <https://github.com/new>
2. **Repository name**：`ao3-hongdeng-wuhai`
3. **Public**，**不要**勾选 “Add a README”（保持空仓库）
4. 创建后在本机执行（路径按你的克隆位置调整）：

```bash
cd ao3-hongdeng-wuhai
git remote add origin https://github.com/HSDCT1230/ao3-hongdeng-wuhai.git
git push -u origin main
```

推送成功后，AO3 皮肤里的背景图链接已指向：

`https://raw.githubusercontent.com/HSDCT1230/ao3-hongdeng-wuhai/main/assets/les-eclaireurs-bg.jpg`

## 从 monorepo 复制

若你只有 `hsdct` 仓库，也可把其中的 `ao3-hongdeng-wuhai/` 目录整夹复制到新仓库根目录后 `git init` 再推送。