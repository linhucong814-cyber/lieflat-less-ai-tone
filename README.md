# 自然语气 · Lieflat Less AI Tone

按明确规则清理中文成稿中的 AI 表达。只修改命中的文字，保留原文信息和文章框架。

[MIT](LICENSE) · [技能规则](SKILL.md) · [图文设置教程](docs/personalization.md) · [发布公告](docs/releases/v1.0.0.md) · [English](README.en.md)

本仓库是 [larashero3-dotcom/lieflat-less-ai-tone](https://github.com/larashero3-dotcom/lieflat-less-ai-tone) 的公开维护版本，由 `linhucong814-cyber` 整理发布。核心 `SKILL.md`、研究材料和分析脚本保留自本地已安装版本，本次增加 Codex 界面说明、安装教程和个性化设置示例。

原作者为 `shiujan`，原许可证为 MIT。原始项目介绍保存在 [中文说明](README.upstream.zh-CN.md) 和 [英文说明](README.upstream.en.md)；研究数据和方法说明来自上游，本仓库未重新采集语料或验证研究结论。

## 适合什么情况

文章已经写好，想清理“说白了”等起手式，或检查规则中列出的重复句法、标点和翻译腔。

技能按 11 条规则检查，只改明确命中的部分。没有命中的句子逐字保留，不增删事实，不改标题层级与段落顺序。已有写作风格参考时，先遵循目标作者的实际风格。

它适合成稿清理。研究脚本用于比较语料特征，不提供单篇文章是否由 AI 生成的可靠鉴定，也不承诺通过检测工具。

## 安装

在终端运行以下命令，将技能克隆到当前官方文档列出的用户技能目录。目标目录需为空或不存在。

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/linhucong814-cyber/lieflat-less-ai-tone.git ~/.agents/skills/lieflat-less-ai-tone
```

更新通过上述方式安装的技能：

```bash
git -C ~/.agents/skills/lieflat-less-ai-tone pull --ff-only
```

已有 `~/.codex/skills/lieflat-less-ai-tone` 安装的用户，先确认自己的 Codex 能发现该目录，再选择保留或迁移；避免重复安装同名技能。更新后若未显示，重启 Codex。

## 直接调用

```text
$lieflat-less-ai-tone 请检查下面这篇中文成稿，只修改命中技能规则的表达，保留原文信息和文章框架。

[粘贴成稿]
```

也可以在技能选择器中选择“自然语气”。先写内容，再检查表达；没有命中规则时保留原文。

## 使用技巧：添加到“个性化”

安装后进入 **设置 → 个性化 → 自定义指令 → Codex 指令**。

![在个性化中打开 Codex 指令](docs/images/codex-personalization-entry.png)

![填写两个技能的使用习惯](docs/images/codex-custom-instructions.png)

截图由维护者提供，具体界面随版本变化。推荐指令和操作说明见 [完整教程](docs/personalization.md)，也可直接复制 [个性化指令示例](examples/personalization.txt)。该示例同时使用 [Goal Prompt Template](https://github.com/linhucong814-cyber/goal-prompt-template-skill)，需要另行安装。

## 规则与研究

- [SKILL.md](SKILL.md)：完整改写规则和验收清单。
- [RESEARCH.md](RESEARCH.md) / [English](RESEARCH.en.md)：上游研究说明。
- [scripts/](scripts/)：原有语料统计脚本，不含研究语料。
- [README.upstream.zh-CN.md](README.upstream.zh-CN.md)：保留的上游项目介绍。

## 来源与许可

原项目：[larashero3-dotcom/lieflat-less-ai-tone](https://github.com/larashero3-dotcom/lieflat-less-ai-tone)。部分规则参考 [KKKKhazix/human-writing](https://github.com/KKKKhazix/human-writing)，详见原技能说明。

本维护版保留 [MIT 许可证和原作者版权声明](LICENSE)。新增文档、截图教程和界面说明同样按 MIT 发布。技能目录与指令机制参考 [OpenAI 官方技能文档](https://learn.chatgpt.com/docs/build-skills)。
