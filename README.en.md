# Lieflat Less AI Tone · 自然语气

Clean up Chinese prose using an explicit list of rules. Change only matching text while preserving facts and document structure.

[中文](README.md) · [Skill instructions](SKILL.md) · [Illustrated setup guide in Chinese](docs/personalization.md) · [Release notes](docs/releases/v1.0.0.md)

This is a public maintenance edition of [larashero3-dotcom/lieflat-less-ai-tone](https://github.com/larashero3-dotcom/lieflat-less-ai-tone), packaged by `linhucong814-cyber`. The original author is `shiujan`. The core skill, research documents, and scripts are preserved from the locally installed edition. This release adds Codex interface metadata, installation instructions, and personalization examples with screenshots.

The research and its numerical claims belong to the upstream project and have not been independently reproduced here. Read the preserved [upstream English README](README.upstream.en.md) or [research document](RESEARCH.en.md) for context.

## Install

Clone into an unused user skill directory:

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/linhucong814-cyber/lieflat-less-ai-tone.git ~/.agents/skills/lieflat-less-ai-tone
```

To update that checkout, run `git -C ~/.agents/skills/lieflat-less-ai-tone pull --ff-only`. Avoid duplicate installations. Restart Codex if changes do not appear.

## Use

Invoke `$lieflat-less-ai-tone` with a completed Chinese draft. The skill changes only explicit rule matches and leaves everything else intact. It does not certify authorship or guarantee a result from AI detection tools.

The illustrated Chinese guide shows how to add preferences in Settings → Personalization → Codex instructions. Install both skills before using the combined [personalization example](examples/personalization.txt).

The upstream [MIT license](LICENSE) and copyright notice are retained. New documentation and interface metadata are also MIT licensed. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for local discovery.
