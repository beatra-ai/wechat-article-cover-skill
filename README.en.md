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

<p align="center"><img src="assets/hero.webp" width="800" alt="Two 2.35:1 WeChat Official Account article covers: a flat illustration for a remote-work article with the headline &quot;三个习惯，让远程办公不再焦虑&quot; rendered in the image, and a no-text clay-pot congee food photo with a quiet headline-safe area on the right. AI-generated with Beatra."></p>

*Two 2.35:1 WeChat Official Account article covers: a flat illustration for a remote-work article with the headline "三个习惯，让远程办公不再焦虑" rendered in the image, and a no-text clay-pot congee food photo with a quiet headline-safe area on the right. AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`wechat-cover-maker`](skills/wechat-cover-maker) | [SKILL.md](skills/wechat-cover-maker/SKILL.md) | 0.2.5 |

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

## Examples

<p align="center"><img src="assets/demo-2.webp" width="800" alt="Matching 1:1 share thumbnails for the same two articles: the remote-work headline set on two lines above the desk illustration, and a close-up of the clay-pot congee that stays readable at small size. AI-generated with Beatra."></p>

*Matching 1:1 share thumbnails for the same two articles: the remote-work headline set on two lines above the desk illustration, and a close-up of the clay-pot congee that stays readable at small size. AI-generated with Beatra.*

Prompt:

```text
[1] 微信公众号文章分享缩略图，正方形 1:1 构图，科技与效率主题的扁平插画风格，与同一篇文章的横版封面保持一致。画面下半部分：一张整洁的家中书桌，一台打开的笔记本电脑、一杯冒热气的茶、一盆小绿植，清晨柔和的暖色阳光。画面上半部分是干净的浅米白色背景留白，在其中居中用粗体黑体、深藏青色（#1F2A44）横排写出标题，分两行，文字必须逐字准确：第一行“三个习惯，”，第二行“让远程办公不再焦虑”。标题字大、醒目，四周留足边距，远离画面边缘。配色：米白、深藏青、柔和的珊瑚橙点缀。在很小的尺寸下依然清晰可辨。除这两行标题外，画面中不要出现任何其他文字、字母、数字、标志或水印；电脑屏幕上不显示文字。 ||| [2] Square 1:1 share thumbnail for a WeChat Official Account lifestyle article about cooking a warming autumn clay-pot congee at home, matching the article's wide editorial food photography cover. One focal subject, large and centered slightly low: a dark glazed clay pot of steaming creamy rice congee with shredded ginger, sliced scallions and a few goji berries, a ceramic spoon resting on the rim, gentle steam rising, on a warm oak table with a folded oatmeal linen napkin and two small dried red dates beside it. Soft natural window light from the left, shallow depth of field, warm amber, cream and muted terracotta palette. Clear bold silhouette that stays recognizable at very small thumbnail size; the upper quarter is a calm out-of-focus warm cream wall. Keep the pot fully inside the frame with margin from all edges. No text, no letters, no typography, no logos, no watermark.
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
