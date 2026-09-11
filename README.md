# bailixisu Agent Skills

可在多个 AI 编程 Agent 中复用的个人工作流，遵循开放的 [Agent Skills](https://agentskills.io) 格式。

## Skills

### blog-workflow

将主题或 Markdown 材料整理成 Learn Everything 博客草稿，并通过“草稿 → 评审 → 预览 → 明确确认 → 发布”的安全流程管理内容。

## 安装

使用 [skills CLI](https://github.com/vercel-labs/skills) 安装到支持的 Agent：

```bash
npx skills add bailixisu/agent-skills --skill blog-workflow
```

全局安装到多个 Agent：

```bash
npx skills add bailixisu/agent-skills \
  --skill blog-workflow \
  --global \
  --agent pi \
  --agent claude-code \
  --agent codex \
  --agent cursor
```

安装后请重新启动对应 Agent。

Pi 可以明确调用：

```text
/skill:blog-workflow draft 写一篇关于 Transformer 的文章
```

其他 Agent 可以通过自然语言触发：

```text
请使用 blog-workflow，把这份材料整理成博客草稿，不要发布。
```

## 更新

```bash
npx skills update blog-workflow
```

## 安全说明

Skill 可能引导 Agent 读写文件、执行命令和推送代码。安装第三方 Skill 前，应先检查 `SKILL.md` 和它附带的脚本。本仓库不会保存密钥、Token 或私人笔记。
