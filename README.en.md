# 公众号封面生成 Skill

[简体中文](./README.md) | English

Turn an article title, topic, or reference image into a WeChat Official Account cover, article hero image, or supporting visual, with space kept for the headline and focused refinement, from inside Claude Code, Codex, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Turn an article title, topic, or reference image into a WeChat Official Account cover, article hero image, post cover, or supporting article visual with headline-safe space and focused refinement. |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Codex, OpenClaw |

| Skill | Entry point | Version |
| --- | --- | --- |
| [`wechat-cover-maker`](skills/wechat-cover-maker) | [SKILL.md](skills/wechat-cover-maker/SKILL.md) | 0.2.2 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/wechat-cover-maker). Report issues there.

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/wechat-article-cover-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/wechat-article-cover-skill wechat-cover-maker
```

Or clone this repository and copy `skills/wechat-cover-maker` into `~/.claude/skills/` for Claude Code,
`~/.agents/skills/` for Codex, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the wechat-cover-maker skill from https://github.com/beatra-ai/wechat-article-cover-skill (folder skills/wechat-cover-maker), then follow its SKILL.md to connect my Beatra account.
```

## What you get

- **One idea, one visual hook** — Reduce the article to a memorable subject, contrast, or metaphor instead of filling the cover with competing concepts.
- **Choose how the title belongs** — Place a short title in the image or reserve a calm, high-contrast area for typography added later.
- **Refine without losing direction** — Improve the focal point, hierarchy, lighting, color, and brand feel while keeping the accepted composition recognizable where possible.

## Use cases

- **Feature article covers** — Give long-form essays, interviews, and opinion pieces a focused hero visual that communicates the subject quickly.
- **Campaign and announcement headers** — Create a branded article header for launches, events, updates, and member communications.
- **Product and service explainers** — Build a cover around one product, benefit, or transformation while keeping the core subject easy to recognize.
- **Recurring editorial series** — Reuse consistent color, composition, and title-area decisions across a recognizable publishing series.

## FAQ

### What do I need to start a WeChat cover?

A title or topic is enough to begin. An article summary, audience, visual tone, target size, brand colors, logo, product, or portrait can help shape a more specific direction.

### Can the article title appear inside the image?

Yes. A short title can be included with a planned placement and contrast, or the cover can remain text-free with a safe area for precise typesetting later.

### Can I use an existing logo, product image, portrait, or brand reference?

Yes. Up to four visual references can guide the composition, style, subject, or brand direction, with the most important details stated clearly.

### How does the cover keep headlines, logos, faces, and crops clear across placements?

It uses safe margins, clear hierarchy, thumbnail review, and placement-aware cropping, then checks typography, logo shape, faces, dimensions, and edge details before finalizing the cover.

## Updates

Each installed skill checks for a new version at most once a day, verifies the
official archive before replacing itself, and leaves your installation untouched
if anything fails. Turn it off at any time — see
`references/automatic-updates-and-safety.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.
