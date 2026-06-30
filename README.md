# Event Content Proposal

体験型イベントコンテンツ提案書（プレミアム版）の静的Webサイトです。

## 概要

- 単一ファイルの静的サイト（`index.html`）
- 画像はすべてHTML内にBase64で埋め込み済み（外部画像ファイル不要）
- フォントは Google Fonts を利用
- A4・全13ページのプレミアムデザインをそのまま再現
- レスポンシブ対応（PC・タブレット・スマホ）— 画面幅に応じてページ全体を等倍縮小し、デザイン・余白・文字サイズ・配色の比率は変更しません

## ローカルで表示する

```bash
# 任意の静的サーバで配信
python3 -m http.server 8000
# → http://localhost:8000/ をブラウザで開く
```

または `index.html` をブラウザで直接開くだけでも表示できます。

## 公開（デプロイ）

### GitHub Pages
1. リポジトリの **Settings → Pages** を開く
2. **Source** を `Deploy from a branch` にする
3. ブランチとフォルダ（`/ (root)`）を選択して保存
4. 数分後に公開URLで `index.html` が表示されます（`.nojekyll` により静的ファイルをそのまま配信）

### Vercel
1. Vercel でこのリポジトリを **Import**
2. Framework Preset は **Other**（ビルド不要の静的サイト）
3. そのまま **Deploy** すると `index.html` が公開されます（設定は `vercel.json` 同梱）

## ファイル構成

```
.
├── index.html      # サイト本体（画像埋め込み済み・全ページ）
├── vercel.json     # Vercel 用静的配信設定
├── .nojekyll       # GitHub Pages で Jekyll 処理を無効化
└── README.md
```
