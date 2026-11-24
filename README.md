# 住所読み取り郵便番号検索 (Camera OCR)

スマホのカメラで地名を読み取り、郵便番号を表示するWebアプリ。
OCRエンジン(Tesseract.js)・日本語モデル・郵便番号データ(日本郵便 2026-10-30更新分)をすべて1つのHTMLに内蔵し、**オフラインで動作**。

## 構成

```
.
├── index.html   ← アプリ本体(単一ファイル・これだけ公開すればOK)
└── README.md
```

## 公開手順(GitHub Pages)

1. GitHubで新規リポジトリを作成(例: `zipcode-ocr` / Public推奨)
2. `index.html` をリポジトリのルートに置く(ブラウザの「Add file → Upload files」でも可)
3. Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / Folder: `/ (root)` → Save
4. 1〜2分後、 `https://<ユーザー名>.github.io/zipcode-ocr/` をiPhone Safariで開く
5. 初回アクセス時に「カメラへのアクセスを許可」を選択

## 更新方法

`index.html` を差し替えてcommit/pushするだけ(Pagesが自動で再デプロイ)。

## 動作要件

- iOS Safari 16.4以上 / Android Chrome
- カメラAPIの仕様上、HTTPS配信が必須(GitHub Pagesは対応済み)
- 手動検索機能のみ、ローカルファイル直開きでも使用可
