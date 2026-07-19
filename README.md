# Shoko Sano — Portfolio

公開URL: **https://shokoko-dev.github.io/**

GitHub Pages でホストしている静的サイト。ビルド不要 — ファイルを編集して push するだけで1〜2分後に反映される。

## ファイル構成

```
├── index.html      ← Home/About(写真+bio+Background+Honors+News抜粋+Contact)
├── research.html   ← Research(修論・卒論・研究経験)
├── work.html       ← Work(全プロジェクトのカードグリッド+タグ絞り込み)
├── news.html       ← News(全履歴の時系列テーブル)
├── style.css       ← 全ページ共通の見た目(色は :root の変数だけ)
├── images/         ← 画像置き場(今はプレースホルダーSVG)
└── projects/       ← プロジェクト詳細ページ(sample-project.html が雛形)
```

## よくある更新

| やりたいこと | 手順 |
|---|---|
| **Newsを1件追加** | `news.html` の `<table>` 先頭に `<tr><td class="date">...</td><td>...</td></tr>` を1行追加。直近5件なら `index.html` のNewsも同様に更新 |
| **Workカードを追加** | 画像を `images/` に入れ、`work.html` の `<!-- ▼ カード1枚の雛形 -->` ブロックをコピーして編集。`data-tags` にタグ(research/engineering/design/community/professional)をスペース区切りで |
| **プロフィール写真を入れる** | `images/profile.jpg` を置き、`index.html` の `<div class="hero-photo">SS</div>` を `<img class="hero-photo" src="images/profile.jpg" alt="Shoko Sano">` に差し替え |
| **カードのサムネイル差し替え** | `images/` に写真(横長16:10推奨)を入れ、カードの `src` を書き換え |
| **アクセントカラー変更** | `style.css` の `--accent` |
| **CV PDFを置く** | ルートに `cv.pdf` を置き、`index.html` のContactの該当行を `<a href="cv.pdf">Download PDF</a>` に |

## 変更を公開する

```bash
git add -A
git commit -m "Update site"
git push
```

1〜2分後に https://shokoko-dev.github.io/ に反映される。
