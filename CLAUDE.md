# Fuwalief HP

## プロジェクト概要
Fuwalief（法人登記準備中）のコーポレートサイト。GitHub Pagesで公開する静的サイト。

## 技術スタック
- HTML + Tailwind CSS (CDN)
- Google Fonts (Plus Jakarta Sans, Noto Sans JP, Material Symbols)
- ホスティング: GitHub Pages
- お問い合わせフォーム: Google Apps Script → contact@fuwalief.com

## サイト構成
- `index.html` - ホームページ（Hero / Mission / Values / Company Profile / Contact）
- `products.html` - プロダクトページ（Fuwari / Kokoro Band / Mindful Salon）
- `privacy.html` - プライバシーポリシー
- `terms.html` - 利用規約
- `assets/logo.png` - ファビコン用アイコン（四つ葉のクローバー）
- `assets/full-logo.png` - ヘッダー・フッター用ロゴ（アイコン＋文字）

## リポジトリ
- GitHub: https://github.com/nekopath-dev/fuwalief-hp
- ブランチ: main
- 公開URL: https://fuwalief.com
- カスタムドメイン: fuwalief.com（お名前.com管理、DNS設定済み）
- Google Workspace: 同ドメインでGWS利用中（DNS共存）

## 会社情報
- 会社名: 株式会社 Fuwalief（法人登記準備中）
- 代表: 田中 陽祐
- 事業内容: アプリケーション開発・運営

## ルール
- ページ内リンクは `./` 形式を使用（`index.html` は使わない）
- ヘッダー・フッターは全ページ統一（ナビ: ホーム / ミッション / プロダクト / 会社概要 / お問い合わせ）
- お問い合わせボタンは `<a>` タグで統一（`<button>` ではない）

## ステータス

### 完了済み
- [x] index.html / products.html 作成
- [x] GitHub Pages有効化・カスタムドメイン設定
- [x] ロゴ・ファビコン設置
- [x] ヘッダー・フッター全ページ統一（日本語メニュー）
- [x] 会社情報を実データに更新
- [x] お問い合わせフォーム（GAS連携）
- [x] プライバシーポリシー・利用規約ページ作成
- [x] モバイルハンバーガーメニューの追加
- [x] 全ページ総点検（リンク形式統一、head統一、Tailwind設定統一、button→a変換、タグ色統一）

### 要対応
- [ ] OGPメタタグの追加（OGP画像の用意後）
- [ ] フォーム送信テスト・動作確認
