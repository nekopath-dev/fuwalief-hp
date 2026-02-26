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
- `products.html` - プロダクト一覧ページ（Irodori / Madobeカード）
- `irodori.html` - Irodori プロダクト紹介ページ
- `irodori-privacy.html` - Irodori プライバシーポリシー
- `irodori-terms.html` - Irodori 利用規約
- `irodori-delete-account.html` - Irodori アカウント削除案内
- `irodori-beta.html` - Irodori クローズドベータテスト参加方法
- `irodori-ai-ethics.html` - Irodori AI倫理ポリシー
- `irodori-commerce.html` - Irodori 特定商取引法に基づく表記
- `madobe.html` - Madobe プロダクト紹介ページ
- `madobe-privacy.html` - Madobe プライバシーポリシー
- `madobe-terms.html` - Madobe 利用規約
- `madobe-delete-account.html` - Madobe アカウント削除案内
- `madobe-ai-ethics.html` - Madobe AI倫理ポリシー
- `privacy.html` - プライバシーポリシー（会社全体）
- `terms.html` - 利用規約（会社全体）
- `assets/logo.png` - ファビコン用アイコン（四つ葉のクローバー）
- `assets/full-logo.png` - ヘッダー・フッター用ロゴ（アイコン＋文字）
- `assets/irodori-icon.png` - Irodori アプリアイコン
- `assets/madobe-icon.png` - Madobe アプリアイコン
- `assets/beta/` - ベータテスト参加手順のスクリーンショット

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
- モバイルハンバーガーメニュー搭載（md未満で表示、vanilla JS）
- お問い合わせボタンは `<a>` タグで統一（`<button>` ではない）
- フッターの著作権表示に「（法人登記準備中）」を含める
- スクロールアニメーション: CSS @keyframes + Intersection Observer（外部ライブラリ不使用）
  - `data-animate` 属性 + `fade-in-up` / `fade-in` / `scale-in` クラスで適用
  - 対象: index.html, products.html, irodori.html, irodori-beta.html, madobe.html（法的文書ページは対象外）

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
- [x] products.html を「鋭意制作中」ページに変更
- [x] Hero見出しのモバイル改行修正（text-3xl化・sm以上で改行）
- [x] products.html をプロダクト一覧ページに変更（Irodoriカード追加）
- [x] irodori.html（プロダクト紹介ページ）作成
- [x] irodori-privacy.html（Irodoriプライバシーポリシー 全14条）作成
- [x] irodori-terms.html（Irodori利用規約 全17条）作成
- [x] スクロールアニメーション追加（index.html / products.html / irodori.html）
- [x] irodori-delete-account.html（アカウント削除案内ページ）作成
- [x] irodori-beta.html（クローズドベータテスト参加方法ページ）作成
- [x] Irodoriアプリアイコン追加（irodori.html / products.html）
- [x] 不要ファイル削除（ルートのスクショ・txtファイル）
- [x] メールアドレス修正（irodori-privacy.html / irodori-terms.html: fuwalief@gmail.com → contact@fuwalief.com）
- [x] irodori-ai-ethics.html（AI倫理ポリシーページ）作成
- [x] madobe.html（Madobeプロダクト紹介ページ）作成
- [x] products.html にMadobeカード追加
- [x] Madobe関連ページ確認・整備（privacy / terms / delete-account / ai-ethics）
- [x] アプリ詳細.md 削除
- [x] irodori-commerce.html（特定商取引法に基づく表記ページ）作成
- [x] Madobeアプリアイコン追加（madobe.html / products.html）

### 要対応
- [ ] OGPメタタグの追加（OGP画像の用意後）
- [x] フォーム送信テスト・動作確認（GAS経由で送信成功確認済み、迷惑メールフォルダに振り分けられる場合あり）
