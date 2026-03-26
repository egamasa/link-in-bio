# link-in-bio

[![FTP Deploy](https://github.com/egamasa/link-in-bio/actions/workflows/ftp-deploy.yml/badge.svg?branch=main)](https://github.com/egamasa/link-in-bio/actions/workflows/ftp-deploy.yml)

egamasa の Link-in-Bio ページ [R203.org](https://r203.org) のソースコードです。

## 技術スタック

- HTML / CSS
  - [トップ画像のRetinaディスプレイ対応](docs/top_image_retina.md)
- フォント
  - [フォント取得・設定方法](docs/fonts.md)
  - [Inter](https://fonts.google.com/specimen/Inter) （セルフホスト、woff2）
- アイコン
  - [MingCute](https://www.mingcute.com/) （インライン SVG）
- Linter / Formatter
  - Prettier
  - Stylelint

## ディレクトリ構成

```
public/          # デプロイ対象
├── css/
├── fonts/
├── images/
└── index.html
src/             # ソースファイル（デザイン素材等）
├── design/
└── images/
docs/            # ドキュメント
```

## 開発環境

```bash
npm install
```

### Lint

```bash
npx stylelint "public/css/**/*.css"
npx prettier --check .
```

## デプロイ

`main` ブランチへの push 時に GitHub Actions で自動デプロイされます。

1. CSS / HTML の Minify（ [auto-minify](https://github.com/nizarmah/auto-minify) ）
1. サーバーへFTP転送（ [FTP Deploy Action](https://github.com/SamKirkland/FTP-Deploy-Action) ）

## ライセンス

(C) 2026 egamasa | orangeliner.net
