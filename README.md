# Fuwalief HP

> The corporate website of Fuwalief — gentle technology that eases anxiety.

株式会社 Fuwalief（法人登記準備中）のコーポレートサイトです。

**サイト:** https://fuwalief.com

## 概要

Fuwalief のミッションは「**優しいテクノロジーで不安を取り除く**」です。トップページでは次のように紹介しています。

> Fuwaliefは、デジタルウェルビーイングを通じて、あなたの日常に安らぎをお届けします。

このサイトには、会社の紹介（ミッション・価値観・会社概要）、自社アプリの紹介、各アプリのプライバシーポリシーや利用規約などの法的文書、お問い合わせフォームを載せています。

| 項目 | 内容 |
| --- | --- |
| 会社名 | 株式会社 Fuwalief（法人登記準備中） |
| 代表 | 田中 陽祐 |
| 事業内容 | アプリケーション開発・運営 |

### プロダクト

| アプリ | 内容（サイト掲載の文言より） | 状態 |
| --- | --- | --- |
| **Irodori** | AIが彩る、あなただけの壁紙。テキストやテンプレートからAIがスマートフォン用の壁紙を自動生成するアプリ（Android） | クローズドベータテスト実施中 |
| **Madobe** | スマホの中に、キャラクターが住んでいる。AIがキャラクターの日常を描き、壁紙として届けるアプリ（Android） | — |

## 作った理由

- 自社アプリ（Irodori、Madobe）を公開するには、プライバシーポリシー・利用規約・アカウント削除の案内などを載せる場所が必要だったため。
- 事業としての信頼性を示す「会社の顔」をつくるため。

## ページ一覧

| ファイル | ページ |
| --- | --- |
| `index.html` | トップ（Hero / Mission / Values / Products / Company Profile / Contact） |
| `products.html` | プロダクト一覧 |
| `privacy.html` | プライバシーポリシー（会社全体） |
| `terms.html` | 利用規約（会社全体） |
| `irodori.html` | Irodori 紹介 |
| `irodori-beta.html` | Irodori クローズドベータテスト参加方法 |
| `irodori-privacy.html` | Irodori プライバシーポリシー |
| `irodori-terms.html` | Irodori 利用規約 |
| `irodori-ai-ethics.html` | Irodori AI倫理ポリシー |
| `irodori-commerce.html` | Irodori 特定商取引法に基づく表記 |
| `irodori-delete-account.html` | Irodori アカウント削除 |
| `irodori-dashboard.html` | Irodori ダッシュボード（運営用。管理者アカウントでのGoogleログインが必要。サイト内からはリンクしていません） |
| `madobe.html` | Madobe 紹介 |
| `madobe-privacy.html` | Madobe プライバシーポリシー |
| `madobe-terms.html` | Madobe 利用規約 |
| `madobe-ai-ethics.html` | Madobe AI倫理ポリシー |
| `madobe-delete-account.html` | Madobe アカウント削除 |

## 技術・ホスティング

- **構成**: ビルド工程のない静的サイト（HTML / CSS / JavaScript）
- **スタイル**: Tailwind CSS（CDN読み込み）、Google Fonts（Plus Jakarta Sans、Noto Sans JP、Material Symbols）
- **動き**: スクロールアニメーションは CSS `@keyframes` と Intersection Observer で実装（外部ライブラリ不使用）。モバイル用ハンバーガーメニューは vanilla JS
- **お問い合わせフォーム**: `index.html` のフォームから Google Apps Script のWebアプリへ `fetch` でPOSTし、contact@fuwalief.com に届く仕組み
- **ダッシュボード**（`irodori-dashboard.html`）: Firebase（Authentication / Firestore / Functions）と Chart.js を使用
- **ホスティング**: GitHub Pages（`main` ブランチ）
- **独自ドメイン**: `fuwalief.com`（`CNAME` で設定）
- **app-ads.txt**: アプリ広告の販売者情報を記載

## 開発の進め方

1. **Google Stitch** でデザイン案を作成
2. **Claude Code** と **Antigravity** で実装

制作期間は 2026年2月〜3月です（最初のコミット 2026-02-05、最新のコミット 2026-03-11）。作業ルールや進捗は `CLAUDE.md` にまとめています。

## ディレクトリ構成

```
fuwalief-hp/
├── index.html                  # トップ
├── products.html               # プロダクト一覧
├── privacy.html / terms.html   # 会社全体のプライバシーポリシー・利用規約
├── irodori*.html               # Irodori 関連ページ（紹介・ベータ・各種規約・ダッシュボード）
├── madobe*.html                # Madobe 関連ページ（紹介・各種規約）
├── assets/
│   ├── logo.png                # ファビコン用アイコン
│   ├── full-logo.png           # ヘッダー・フッター用ロゴ
│   ├── irodori-icon.png        # Irodori アプリアイコン
│   ├── madobe-icon.png         # Madobe アプリアイコン
│   └── beta/                   # ベータテスト参加手順のスクリーンショット
├── CNAME                       # 独自ドメイン設定（fuwalief.com）
├── app-ads.txt
└── CLAUDE.md                   # 開発メモ（構成・ルール・ステータス）
```

## ローカルでの確認

ビルドは不要です。HTMLファイルをブラウザで直接開くか、簡易サーバを立てて確認します（Tailwind CSS と Google Fonts をCDNから読むため、ネット接続が必要です）。

```bash
git clone https://github.com/nekopath-dev/fuwalief-hp.git
cd fuwalief-hp
python3 -m http.server 8000
# http://localhost:8000 を開く
```

## 作者

田中 陽祐（[@nekopath-dev](https://github.com/nekopath-dev)）

## ライセンス

LICENSE ファイルはありません。サイト内の表記に従い All rights reserved です。
