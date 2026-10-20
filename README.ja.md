# 公众号封面生成 Skill

[简体中文](./README.md) | [English](./README.en.md) | 日本語

> 👉 こちらもどうぞ [小红书封面制作 Skill](https://github.com/beatra-ai/xiaohongshu-cover-maker-skill)

記事タイトル、テーマ、参考画像から、見出し用のスペースを確保した WeChat 公式アカウントのカバー、記事のヒーロー画像、補助ビジュアルを作成し、必要な箇所だけ手直し。Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw のどれからでもそのまま使えます。

> [!IMPORTANT]
> 生成には [Beatra](https://beatra.ai) アカウントが必要で、クレジットを消費します。スキル自体のインストールは無料です。

| 項目 | 内容 |
| --- | --- |
| **できること** | 記事タイトル、テーマ、参考画像からWeChat公式アカウント向けのカバー画像、記事アイキャッチ、見出し画像を作成し、見出し用の安全領域やブランド感まで整えます。 |
| **モデル** | Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、MiniMax Image 01 Live |
| **動作要件** | Python 3.10 以上と、`SKILL.md` を読み込めるエージェント |
| **費用** | インストールは無料。生成のたびに Beatra アカウントのクレジットを消費しますが、課金されるのは、その生成を明示的に依頼したとき、または確認カードを承認したときだけです。 |
| **対応エージェント** | Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="2.35:1 の WeChat 公式アカウント記事カバー 2 枚：リモートワーク記事向けに見出し「三个习惯，让远程办公不再焦虑」を画像内に描いたフラットイラストと、右側に見出し用の静かな余白を残した文字なしの土鍋粥の料理写真。Beatra AI で生成。"></p>

*2.35:1 の WeChat 公式アカウント記事カバー 2 枚：リモートワーク記事向けに見出し「三个习惯，让远程办公不再焦虑」を画像内に描いたフラットイラストと、右側に見出し用の静かな余白を残した文字なしの土鍋粥の料理写真。Beatra AI で生成。*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`wechat-cover-maker`](skills/wechat-cover-maker) | [SKILL.md](skills/wechat-cover-maker/SKILL.md) | 0.3.0 |

このリポジトリは [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/wechat-cover-maker) から自動的に公開されています。問題の報告はそちらへお願いします。

## インストール

[`skills`](https://skills.sh) CLI を使う場合：

```bash
npx skills add beatra-ai/wechat-article-cover-skill
```

GitHub CLI を使う場合：

```bash
gh skill install beatra-ai/wechat-article-cover-skill wechat-cover-maker
```

または、このリポジトリをクローンして `skills/wechat-cover-maker` を次の場所にコピーします：Claude Code は `~/.claude/skills/`、Cursor は `~/.cursor/skills/`、Codex は `~/.agents/skills/`、Windsurf は `~/.codeium/windsurf/skills/`、Cline は `~/.cline/skills/`、OpenClaw は `~/.openclaw/skills/`。

または、次の文をエージェントに貼り付けてください：

```text
https://github.com/beatra-ai/wechat-article-cover-skill から wechat-cover-maker スキル（フォルダ skills/wechat-cover-maker）をインストールし、その SKILL.md に従って私の Beatra アカウントに接続してください。
```

## 作例

<p align="center"><img src="assets/demo-2.webp" width="800" alt="同じ 2 本の記事に合わせた 1:1 のシェア用サムネイル：机のイラストの上に 2 行で置いたリモートワークの見出しと、小さく表示しても読みやすい土鍋粥のクローズアップ。Beatra AI で生成。"></p>

*同じ 2 本の記事に合わせた 1:1 のシェア用サムネイル：机のイラストの上に 2 行で置いたリモートワークの見出しと、小さく表示しても読みやすい土鍋粥のクローズアップ。Beatra AI で生成。*

エージェントへの依頼例：

```text
この 2 本の記事に合わせた 1:1 のシェア用サムネイルを作って：リモートワークの記事は見出し「三个习惯，让远程办公不再焦虑」を机のイラストの上に 2 行で置き、土鍋粥の記事は小さく表示しても読めるクローズアップで。
```

プロンプト：

```text
[1] 微信公众号文章分享缩略图，正方形 1:1 构图，科技与效率主题的扁平插画风格，与同一篇文章的横版封面保持一致。画面下半部分：一张整洁的家中书桌，一台打开的笔记本电脑、一杯冒热气的茶、一盆小绿植，清晨柔和的暖色阳光。画面上半部分是干净的浅米白色背景留白，在其中居中用粗体黑体、深藏青色（#1F2A44）横排写出标题，分两行，文字必须逐字准确：第一行“三个习惯，”，第二行“让远程办公不再焦虑”。标题字大、醒目，四周留足边距，远离画面边缘。配色：米白、深藏青、柔和的珊瑚橙点缀。在很小的尺寸下依然清晰可辨。除这两行标题外，画面中不要出现任何其他文字、字母、数字、标志或水印；电脑屏幕上不显示文字。 ||| [2] Square 1:1 share thumbnail for a WeChat Official Account lifestyle article about cooking a warming autumn clay-pot congee at home, matching the article's wide editorial food photography cover. One focal subject, large and centered slightly low: a dark glazed clay pot of steaming creamy rice congee with shredded ginger, sliced scallions and a few goji berries, a ceramic spoon resting on the rim, gentle steam rising, on a warm oak table with a folded oatmeal linen napkin and two small dried red dates beside it. Soft natural window light from the left, shallow depth of field, warm amber, cream and muted terracotta palette. Clear bold silhouette that stays recognizable at very small thumbnail size; the upper quarter is a calm out-of-focus warm cream wall. Keep the pot fully inside the frame with margin from all edges. No text, no letters, no typography, no logos, no watermark.
```

## 技術仕様と出力上限

2026-10-18 時点。最新の一覧：https://docs.beatra.ai/ja/docs/models

- **アップロード** — 1 ファイルあたり最大 100 MB。下記の各モデルの入力制限も適用されます
- **テキストから画像** — 10 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、MiniMax Image 01 Live）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 16.8 MP
  - 16.8 MP（4K ティア）：Wan Image 2.7 Pro（1 リクエストあたり最大 4 枚）／GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2（1 リクエストにつき 1 枚）
- **画像から画像** — 10 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、MiniMax Image 01 Live）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 16.8 MP
  - 16.8 MP（4K ティア）：GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2（1 リクエストにつき 1 枚）
  - 入力画像：1 リクエストあたり最大 4 枚、各 10〜20 MB／BMP、GIF、JPEG、PNG、TIFF、WEBP
- **画像編集** — 6 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 4.2 MP
  - 4.2 MP（2K ティア）：Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro（1 リクエストあたり最大 4 枚）
  - 入力画像：1 リクエストあたり最大 4 枚、各 10〜20 MB／BMP、GIF、JPEG、PNG、TIFF、WEBP

## 得られるもの

- **一つの記事に一つのフック** — 記事の約束、対比、人物、物、比喩から主役を一つ選び、複数のアイデアが競合する構図を避けます。
- **見出しの置き方を先に決める** — 短い見出しを画像に入れるか、後から正確に組むための静かで見やすい安全領域を残します。
- **方向性を保ったまま調整** — 採用した構図をできるだけ保ちながら、焦点、階層、光、色、ブランドらしさを整えます。

## 活用シーン

- **特集・インタビュー記事** — 長文、インタビュー、解説、意見記事に、テーマが素早く伝わるアイキャッチ画像を用意します。
- **キャンペーン・告知記事** — 新商品、イベント、更新情報、会員向けのお知らせに、ブランド感のある記事ヘッダーを作ります。
- **商品・サービス解説** — 一つの商品、価値、変化を主役にし、記事の要点が伝わるカバー画像を作ります。
- **連載・定期コンテンツ** — 色、構図、見出し領域の考え方をそろえ、継続して見分けやすいシリーズ画像にします。

## よくある質問

### WeChatの記事カバーを作るには何が必要ですか？

記事タイトルまたはテーマがあれば始められます。要約、想定読者、雰囲気、掲載サイズ、ブランドカラー、ロゴ、商品、人物の資料があると方向をより具体的にできます。

### 記事タイトルを画像の中に入れられますか？

はい。短いタイトルを位置とコントラストを決めて含めることも、後から正確に文字を組めるよう安全領域を空けた文字なし背景にすることもできます。

### ロゴ、商品画像、人物写真、ブランド資料を使えますか？

はい。最大四つのビジュアル資料を、主役、スタイル、人物、ブランドの手がかりとして使い、残したい特徴を明確にできます。

### 見出し、ロゴ、人物、トリミングを掲載先で見やすくするには？

安全な余白、明確な階層、サムネイル確認、掲載位置に合わせたトリミングを使い、文字組み、ロゴ形状、人物、寸法、端の要素まで仕上げ前に確認します。

## 更新とセキュリティ

2026 年 10 月のリリース以降、このスキルに自動更新機能はありません。インストールしたファイルだけを実行し、
自動的に置き換えることはありません。更新はインストールに使ったツール（`npx skills update wechat-cover-maker` または
`gh skill update wechat-cover-maker`）で行ってください。詳細はスキル内の `references/updates-and-security.md` を参照してください。

## ライセンス

[MIT-0](LICENSE)：商用を含め、自由に使用・改変・再配布できます。クレジット表記は不要です。ClawHub 上のこれらのスキルと同じ条件です。

## リンク

- ウェブサイト — https://beatra.ai
- ドキュメント — https://docs.beatra.ai
- コンソール — https://console.beatra.ai
- AI エージェント向け — https://beatra.ai/llms.txt（インデックス）· https://beatra.ai/llms-full.txt（全スキルを 1 ファイルに）
