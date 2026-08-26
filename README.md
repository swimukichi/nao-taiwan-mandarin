# 使いどころ不明の台湾華語 — 紹介ホームページ

note マガジン「使いどころ不明の台湾華語」(https://note.com/swi0801/m/m2c34c479cded) を紹介する静的サイトです。
HTML / CSS / JS のみで作られており、外部ライブラリやビルドツールは使っていません。

構成は姉妹サイト「NAOの小説箱」と同じ仕組みです:

- `index.html` / `style.css` / `script.js` — サイト本体
- `scripts/update_latest.py` — note の RSS を取得して `data/latest.json` を再生成するスクリプト
- `.github/workflows/update-feed.yml` — 6時間ごとに上記スクリプトを自動実行し、変更があれば自動コミット・push するワークフロー
- `robots.txt` / `sitemap.xml` — 検索エンジン向け

## 手元で見る

```bash
python3 -m http.server 8000
```

## 無料で公開する方法

GitHub Pages または Cloudflare Workers(静的アセット)への公開手順は、姉妹サイトの README と同様です。
このリポジトリでは GitHub Pages と Cloudflare の両方を無料プランで運用しています。
