---
name: github-cn-guide
description: 陪不读英文界面的用户在 GitHub 网页上建仓库、传文件、改文件。用户说"帮我建个仓库""教我把文件传上去""GitHub 怎么用""这个按钮什么意思"时使用：一次只给一个动作，每个英文按钮配中文对照，每步给核对方法。
---

# github-cn-guide — 陪不会英文界面的人在 GitHub 上干活

## 触发条件

- 用户要建仓库、上传文件、修改或删除仓库里的文件
- 用户看不懂 GitHub 某个页面，要求逐条翻译
- 用户说"卡住了""按钮点不动""传完了但不知道对不对"

## 三条铁律

1. **一次只给一个动作**。不要一口气丢八个步骤，用户会迷失在第二屏。
2. **每个英文原文都配中文**，并说清它在屏幕哪个位置（右上角、页面最底、地址栏左侧）。
3. **不信译名，信原文**。浏览器翻译会把 `main` 翻成"主要内容"、`No license` 翻成"无驾照"、把文件名 `self-improving` 翻成"自我提升"。核对路径和按钮时以英文原文为准。

## 建仓库（最常用）

让用户直接在地址栏输入 `github.com/new`，比在界面上找 `+` 号快。表单只有六处：

| 字段原文 | 中文 | 怎么填 |
|---|---|---|
| `Owner` | 所有者 | 默认是本人，不动 |
| `Repository name` | 仓库名 | 小写加连字符，不要中文和空格 |
| `Description` | 描述 | 选填，不填不影响 |
| `Public` / `Private` | 公开 / 私有 | 默认选 **Private**，除非用户明确要分享 |
| `Start with a template` | 模板 | 选 `No template` |
| `Add a README file` | 添加 README | **勾上**，否则建出来是空仓库 |
| `Add .gitignore` / `Choose a license` | 忽略文件 / 许可证 | 用户自带 LICENSE 时都不勾 |

点最底下绿色 `Create repository`（创建仓库）。

## 网页上传文件

1. 仓库页右上角 `Add file`（添加文件）→ 下拉第二项 `Upload files`（上传文件）
2. 拖文件进去。**只拖内容本身，不要拖外层父文件夹**——拖错会多套一层目录，路径全废
3. 核对清单：每一行路径的前缀必须一致（例如都以 `skills/` 开头）；文件总数要对；没有 `.DS_Store`
4. 滚到底 → `Commit changes`（提交更改）→ 若弹确认框再点一次

提交后回仓库首页核对三层：顶层项目数量和名字对不对；点进主文件夹看子项数量；随便打开一个文件，能看到 `name:` 和 `description:` 就说明内容是完整的。

## 改和删

- 改：点开文件 → 右上角铅笔 `Edit` → 改完 `Commit changes`
- 新增：`Add file` → `Create new file`，文件名带上完整路径
- 删：点开文件 → 右上角垃圾桶 `Delete file` → 提交
- 转换可见性：`Settings` → 拉到最底 `Danger Zone` → `Change visibility`

## 术语对照（用户问就查这里）

`Repository` 仓库 · `Commit` 提交 · `Branch` 分支 · `main` 主分支 · `Add file` 添加文件 · `Upload files` 上传文件 · `Commit changes` 提交更改 · `Create repository` 创建仓库 · `Settings` 设置 · `Visibility` 可见性 · `Danger Zone` 危险操作区 · `Issue` 议题 · `Pull request` 拉取请求 · `Fork` 派生 · `Release` 发布 · `README` 说明文档 · `License` 许可证

## 不要碰的东西

- 首页绿色的 `Create project`：那是 Codespaces，不是仓库
- `Copilot` 里的 `Upgrade`：付费入口
- 任何"GitHub 中文版""GitHub 镜像站"：输入账号密码会被第三方拿走，唯一入口是 `github.com`

## 收尾提醒

传完提一句：私有仓库别人打不开是正常现象，不是出错；建议顺手开两步验证（`Settings → Password and authentication → Enable`）。

## 常见坑

- 用户把上层目录拖进去，路径变成 `01-技能/xxx`，与 README 里的相对链接全部对不上——发现就点"取消"重传。
- 中文版浏览器把路径里的英文单词也翻译了，用户以为文件名错了——让用户看原始英文或用代码视图确认。
- 一次给太多步骤，用户在第二个页面就走丢。宁可多问一句"现在屏幕上看到什么"。
