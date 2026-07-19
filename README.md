# Shoko Sano — Portfolio

公開URL: **https://shokoko-dev.github.io/portfolio/**

GitHub Pages でホストしている静的サイト。ビルド不要 — ファイルを編集して push するだけで1〜2分後に反映される。

## ファイル構成

```
portfolio/
├── index.html            ← トップページ(自己紹介 + Projectグリッド + Contact)
├── style.css             ← 全ページ共通の見た目(色を変えたい時は :root の変数だけ)
├── images/               ← 画像置き場(写真はここに入れる)
└── projects/
    └── sample-project.html  ← Project個別ページの雛形(これをコピーして増やす)
```

## Projectを1つ追加する手順(3ステップ)

1. **画像を入れる**: 写真を `images/` にコピー(例: `images/my-project.jpg`)
   - 横長(16:10くらい)だとサムネイルがきれいに収まる
2. **個別ページを作る**: `projects/sample-project.html` を複製して
   `projects/my-project.html` にリネーム → 中のテキストと画像パスを書き換える
   - 画像パスは `../images/my-project.jpg` のように `../` を付ける
3. **トップにカードを足す**: `index.html` の `<!-- ▼▼ Projectカード -->` の
   ブロックをコピーして、タイトル・説明・画像・リンク先を書き換える

## 変更を公開する(push)

ターミナルでこのフォルダに移動して:

```bash
git add -A
git commit -m "Add new project"
git push
```

1〜2分後に https://shokoko-dev.github.io/portfolio/ に反映される。

## よくある編集

| やりたいこと | 触るファイル |
|---|---|
| 自己紹介文を直す | `index.html` の `<!-- ABOUT -->` セクション |
| アクセントカラーを変える | `style.css` の `--accent` |
| 顔写真を入れる | `images/` に入れて `index.html` の `.hero-photo` を `<img>` に差し替え |
| CV PDFを置く | ルートに `cv.pdf` を置いて `href="cv.pdf"` にリンク |
