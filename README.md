# 拆书博主 · book-block-splitter

把书籍正文拆成「客观提取＋可拍短视频知识块」的 AI Skill。

本仓库保存现有 v1.0 技能的原样导出，`SKILL.md` 保留原作者、规则和老王环境适配注记。

## 能做什么

- 提取本章 3—5 个作者核心观点及对应原文。
- 提炼 2—4 条有出处的独立洞见。
- 推荐 2—4 个适合拍摄的知识块，包含钩子、价值、痛点、解法和关键原文。
- 有明确身份信息时，补充个人映射。

输出是拆书报告及素材推荐。技能中提到的后续成稿与知识入库流程需另行配置。

## 安装

把仓库放入所用 AI 工具的技能目录，确保目录名为 `book-block-splitter`，内部直接包含 `SKILL.md`。以下命令要求已安装 Git；私有仓库需要先获得访问权限并完成 GitHub 认证。

Codex（PowerShell）：

```powershell
git clone https://github.com/wzhmaggie25-rgb/book-block-splitter.git "$env:USERPROFILE/.codex/skills/book-block-splitter"
```

Claude Code（PowerShell）：

```powershell
git clone https://github.com/wzhmaggie25-rgb/book-block-splitter.git "$env:USERPROFILE/.claude/skills/book-block-splitter"
```

Hermes：把本仓库目录放入当前 profile 的 `skills/note-taking/` 下。必要时重新打开会话，让宿主发现新技能。

## 使用

向已加载技能的 AI 发送口令并提供正文：

```text
拆书

以下是我提供的章节正文：
……
```

也可以提供可读取的文件路径或网页链接。只有书名时，需要先补充正文。文件读取、PDF/EPUB 解析和网页提取依赖宿主可用工具；原文中的 Read、WebFetch 等名称应映射到宿主实际能力。

## 文件与关联技能

本技能只有一个运行文件 `SKILL.md`，没有附带脚本、模型或书籍正文。

元数据中的 `knowledge-processing-pipeline` 和 `script-four-rulers` 是原环境的后续关联技能，不包含在仓库内；生成拆书报告不要求同时安装它们。技能末尾的个人映射默认值属于老王环境，其他使用者应按自己的身份处理。

## 来源与许可

- 技能名称：`book-block-splitter`
- 原作者署名：老王投喂 / 溯整理
- 原版本：1.0
- 导出日期：2026-10-21
- 许可：MIT，与原技能元数据一致，见 [LICENSE](LICENSE)。
