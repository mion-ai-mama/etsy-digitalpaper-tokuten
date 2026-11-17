# みおん式AI副業ノート デジタルペーパー編（v2テンプレート複製）

> 設計の共通原則は `~/.claude/CLAUDE.md` に従う。デザイン基準は `docs/requirements.md`（この特典の要件。共通デザインは v2 テンプレートの仕様書）。

## プロジェクト設定

技術スタック: HTML5 / CSS3 / Vanilla JavaScript（ビルドなし）、GitHub Pages。backend・database・環境変数なし（`.env` 系は作らない）。

## 運用ルール

- 元のテンプレート `instagram-tokuten-template-v2` は編集しない。この特典の変更は `js/content.js` が中心
- 文章・画像・LINEリンクの単一の源は `js/content.js`。色・フォント・余白の単一の源は `css/style.css` の `:root`。特典ごとにCSSを足さない
- 旧テンプレート（`instagram-tokuten-template`・ピンク系）と既存特典は、明示指示がない限り変更しない
- 操作画面は実キャプチャのみ。ChatGPT・Canva・Etsyの画面は未掲載（提供待ち）。Etsyのルール・手数料は公式ページで確認し、日付つきで書く
- 人物はバナーの本人イラスト（`インスタ関連/指を掲げる笑顔の女性ポートレート.png`・背景を切り抜いたもの）のみ。バナーはCodexの画像生成で作成。作例のデジタルペーパー12枚はAI生成の作例で、本人の過去の成果や販売実績とは書かない
- CTA: 冒頭と最後の2か所。LINE誘導はテンプレートの標準構成（`js/line-cta.js` の共通文章＋`content.js` の `lineIntro`）。目次画像は使わない。OGP画像は指定がなければ設定しない

## 命名・品質

- ファイル kebab-case / 変数 camelCase / 関数100行・ファイル700行・複雑度10・行長120以下
- ローカル確認: `python3 -m http.server <port>` を1つだけ起動

## ドキュメント管理

許可: `docs/requirements.md` / `docs/SCOPE_PROGRESS.md` / `README.md` / `LICENSE.md`。他は要許諾。

## 品質ゲート

- 第一防壁: ローカル git hook（pre-commit: 秘密情報拒否＋JS構文）
- 最終防壁: GitHub Actions `verify`（JS構文・必須ファイル・index.htmlのリンク切れ）。main保護
- ブランチ: `main`＝公開 / `develop`＝編集

## この特典の追加仕様

- 収入・売上・「稼げる」を約束しない。売上と手元に残る金額は違うことを書く
- AIを使ったら商品説明で開示すること、プロンプト集は売れないこと（Etsy公式）を必ず入れる
- プロンプトの書き換え箇所は「（ここに…）」で示す（script.js が目立たせる）
- 読者向け文章に「確認していません」と書かない。未確認事項は `docs/SCOPE_PROGRESS.md` に記録
