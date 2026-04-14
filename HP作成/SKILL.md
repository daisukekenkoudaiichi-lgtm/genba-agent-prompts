---
name: lp-creation
description: クライアント LP / HP の設計・実装・デプロイ時のデザインルールと8ステップ手順（汎用版）
---

# LP 作成スキル

## 概要

[クライアント名]のホームページを  
**「信頼感・権威性・コンバージョン最大化」** を軸に構築するための  
デザイン・実装・デプロイ一気通貫の標準手順書。

- **主要ファイル**: `index.html`（LP 本体）
- **技術スタック**: HTML / CSS（Tailwind のみ）/ JavaScript（フレームワークなし）
- **ホスティング**: Netlify（GitHub push で自動デプロイ）

---

## 参考資料

| 資料 | パス | 用途 |
|---|---|---|
| HP、LP用語、技術仕様書 | `C:\GitHub\mddata\HP、LP用語、技術仕様書.md` | UI用語・構成の定義源 |
| CLAUDE.md | `[プロジェクトルート]\CLAUDE.md` | デザイナーペルソナ・開発方針 |
| CHANGE_LOG.md | `[プロジェクトルート]\CHANGE_LOG.md` | 修正履歴（自動記録） |

> **作業開始時は必ず上記2ファイルを Read してから着手すること。**

---

## ペルソナ（役割定義）

> マーケティング心理学を熟知した、世界トップクラスのWEBデザイナー兼フロントエンドエンジニア。  
> ユーザーの信頼を勝ち取り、コンバージョン（問い合わせ）に繋がる最高品質のLPを構築する。

---

## 作成時のルール（8 ステップ）

### Step 1: ファーストビュー（FV）の構成を決定

**目標**: スクロールせずに見える領域で「この人（サービス）に任せたい」と思わせる。

- **背景**: グラデーション（例：メインカラー → ダーク）+ 半透明オーバーレイ
- **写真**: クライアントの顔写真・サービス画像を右寄せ最大 **600px** で配置（WebP 形式）
- **キャッチコピー**: 大見出し（`font-size: 3rem+`）を左側に縦中央揃え
- **CTA ボタン**: FV 内に最低1つ設置（例：「お問い合わせはこちら」）
- **視線誘導**: Z 型 または F 型レイアウトで自然な読み進め順を設計

```
[ロゴ + グローバルナビ]
─────────────────────────────────────
  キャッチコピー（大）   │  メイン画像 600px
  サブコピー（小）       │
  [CTA ボタン]          │
─────────────────────────────────────
```

---

### Step 2: CSS は Tailwind のみ使用（Bootstrap 混在禁止）

- CDN 読み込み: `<script src="https://cdn.tailwindcss.com"></script>`
- カスタムカラーは `tailwind.config` の `extend` で定義
- Bootstrap・独自 CSS フレームワークは **絶対に混ぜない**
- 独自スタイルが必要な場合のみ `<style>` タグに最小限の CSS を記述

```html
<!-- OK: Tailwind のみ -->
<div class="flex items-center justify-between px-6 py-4 bg-primary-900">

<!-- NG: Bootstrap + Tailwind 混在 -->
<div class="container-fluid flex items-center">
```

---

### Step 3: HTML 構造の設計（Semantic HTML）

セクション構成（上から順）:

| # | セクション | タグ | Tailwind クラス例 | 備考 |
|---|---|---|---|---|
| 1 | ヘッダー / グローバルナビ | `<header>` | `sticky top-0 z-50` | 必須 |
| 2 | ファーストビュー | `<section id="hero">` | `min-h-screen relative` | 必須 |
| 3 | ペインポイント（悩み提示） | `<section id="pain">` | `bg-gray-50 py-20` | 必須 |
| 4 | プロフィール / 会社概要（権威性） | `<section id="profile">` | `py-20` | 必須 |
| 5 | 実績・事例（ソーシャルプルーフ） | `<section id="achievements">` | `bg-white py-20` | 必須 |
| 6 | サービス / 特徴 | `<section id="service">` | `bg-blue-50 py-20` | 必須 |
| 7 | お問い合わせフォーム（CTA） | `<section id="contact">` | `bg-primary-900 py-20` | 必須 |
| 8 | フッター | `<footer>` | `bg-gray-900 text-white` | 必須 |
| ※ | クライアント固有セクション | 任意 | — | 業種・目的に応じて追加 |

- `<main>` タグでコンテンツ全体を囲む
- 見出しは `h1` → `h2` → `h3` の階層を守る（SEO 重要）
- `alt` 属性はすべての `<img>` に設定必須

---

### Step 4: 画像を WebP 形式で最適化

- **形式**: JPEG/PNG → **WebP** に変換（ファイルサイズ 30〜50% 削減）
- **サイズ指定**: 表示サイズの最大 2x（Retina 対応）
- **遅延読み込み**: `loading="lazy"` を FV 以外の全画像に付与
- **フォールバック**: `<picture>` タグで WebP 未対応ブラウザに対応

```html
<picture>
  <source srcset="images/photo.webp" type="image/webp">
  <img src="images/photo.jpg" alt="[クライアント名]の写真" loading="lazy" width="600" height="800">
</picture>
```

---

### Step 5: スマホ対応（レスポンシブ）の確認

- **方針**: モバイルファースト（小画面から設計し、`md:` / `lg:` で拡張）
- **ブレイクポイント**（Tailwind デフォルト）:
  - `sm`: 640px〜（小型スマホ対応）
  - `md`: 768px〜（タブレット）
  - `lg`: 1024px〜（PC）
- **ハンバーガーメニュー**: `md:hidden` でスマホのみ表示、JS でトグル制御
- **FV 写真**: スマホでは非表示 or 上部に移動（`hidden md:block`）
- **フォント**: スマホ `text-2xl` → PC `text-5xl` に段階拡大

確認手順:
1. Chrome DevTools → Toggle Device Toolbar（F12 → Ctrl+Shift+M）
2. iPhone SE（375px）/ iPhone 14（390px）/ iPad（768px）で目視確認
3. 文字・ボタンが指で押せるサイズか（最小 44px × 44px）を確認

---

### Step 6: Lighthouse で品質測定

Chrome DevTools → Lighthouse タブ で以下スコアを目標にする:

| 項目 | 目標スコア | 主な改善手段 |
|---|---|---|
| Performance | **90+** | WebP 化・遅延読み込み・不要 JS 削除 |
| Accessibility | **95+** | alt 属性・aria ラベル・コントラスト比 |
| Best Practices | **95+** | HTTPS・コンソールエラーゼロ |
| SEO | **95+** | meta description・h1 の一意性 |

測定コマンド（Node.js CLI）:
```bash
npx lighthouse https://your-netlify-url.netlify.app --view
```

---

### Step 7: GitHub に push → Netlify で自動デプロイ

**Netlify 設定**（初回のみ）:
- Build command: （なし・空欄）
- Publish directory: `/`（ルートディレクトリ）
- Branch: `main`

**デプロイフロー**:
```
git push origin main
    ↓ （Webhook 自動起動）
Netlify Build（静的ファイルのみなので即時）
    ↓
本番 URL に反映（通常 1〜3 分）
```

**手動デプロイ確認**:
```bash
# Netlify CLI を使う場合
npx netlify deploy --prod --dir .
```

---

### Step 8: watch.js と auto-push.js で自動監視・デプロイ

**起動**（開発中は常時起動しておく）:
```bash
npm run watch
```

**動作フロー**:
```
index.html を保存（VSCode: Ctrl+S）
    ↓ fs.watch が検知
    ↓ 3 秒デバウンス（連続保存をまとめる）
git add . → git commit -m "index.html 修正: [タイムスタンプ]"
    ↓
git push origin main
    ↓
CHANGE_LOG.md に修正内容を自動記録
    ↓
Netlify が自動デプロイ（1〜3 分で本番反映）
```

**手動プッシュ**（メッセージを指定したい場合）:
```bash
npm run push "FV キャッチコピーを修正"
```

---

## カラースキーム（汎用）

> 業種・ブランドイメージに合わせてカスタマイズしてください。

| 役割 | カラー例 | Tailwind クラス例 | 意図 |
|---|---|---|---|
| ベース | `#FFFFFF` | `bg-white` | 清潔感・余白 |
| メイン | クライアントのブランドカラー | `bg-primary-900` | 信頼・ブランド統一 |
| サブ | メインより明るいトーン | `bg-primary-600` | 親しみやすさ |
| アクセント | 補色・コントラスト色 | `bg-accent-500` | CTA・行動喚起 |
| テキスト | `#1f2937` | `text-gray-800` | 可読性 |

**業種別カラー参考**:
- 士業・金融・官公庁: ネイビー系（`#1a3a6b`）
- 医療・福祉: グリーン系（`#065f46`）
- 美容・ファッション: ピンク・ゴールド系
- IT・スタートアップ: ブルー・パープル系
- 飲食・食品: オレンジ・アース系

---

## マーケティング心理テクニック（必須）

| テクニック | 配置場所 | 実装例 |
|---|---|---|
| **権威性** | プロフィールセクション | 実績数・資格・受賞歴バッジ |
| **ソーシャルプルーフ** | 実績セクション | 「お客様の声」カルーセル |
| **希少性（スケアシティ）** | CTA 近く | 「ご相談は月10件限定」 |
| **ベネフィット訴求** | FV サブコピー | 「あなたの課題を、解決に。」 |
| **マイクロコピー** | CTA ボタン下 | 「※無料・返信は24時間以内」 |

---

## チェックリスト

### デザイン
- [ ] FV にキャッチコピー + メイン画像 + CTA ボタンが揃っている
- [ ] カラースキームがブランドカラーで統一されている
- [ ] フォントサイズが PC / スマホで適切に変化する
- [ ] セクション間の余白（padding）が `py-16` 以上で十分にある
- [ ] ボタンにホバーエフェクト（`transition-colors duration-300`）がある

### HTML / CSS
- [ ] `<title>` と `<meta name="description">` が[クライアント名]・サービス内容を含んでいる
- [ ] OGP タグ（og:title / og:image）が設定されている
- [ ] 全 `<img>` に `alt` 属性がある
- [ ] CSS は Tailwind のみ（Bootstrap の混入がない）
- [ ] `<h1>` がページ内に1つだけある

### パフォーマンス
- [ ] 全画像が WebP 形式になっている
- [ ] FV 以外の画像に `loading="lazy"` が付いている
- [ ] Lighthouse Performance スコアが 90 以上
- [ ] Lighthouse Accessibility スコアが 95 以上

### レスポンシブ
- [ ] iPhone SE（375px）で崩れがない
- [ ] タブレット（768px）で2カラムが正しく機能する
- [ ] ハンバーガーメニューが開閉する

### デプロイ
- [ ] `npm run watch` が起動している（または手動で push 済み）
- [ ] Netlify のデプロイログが「Published」になっている
- [ ] 本番 URL で最終確認済み
- [ ] CHANGE_LOG.md に修正内容が記録されている
