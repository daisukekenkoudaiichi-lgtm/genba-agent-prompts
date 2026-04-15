claude code "
genba-agent-prompts/HP作成/02_HTML自動生成.md を改良してください。

【改良内容】
以下の内容をすべて含める：

# 02 — HTML自動生成 + フル構成自動化

## このプロンプトをコピペして使用

\`\`\`
以下をすべて自動生成してください。

【参考ファイル】
セットアップ.md（01で生成済み）の内容を読み込んでください。

【作業内容】
1. セットアップ.md の「クライアント情報」を抽出
2. セットアップ.md の「参考サイト技術解析」を反映
3. セットアップ.md の「最適セクション構成」を使用
4. CLAUDE.md のペルソナに基づいて HTML 生成
5. SKILL.md のデザイン規約に基づいて CSS 生成

【デザイン要件】
- SKILL.md で定義されたカラースキーム
- モバイルファースト
- Lighthouse 90+

【コーディング規約】
- 純粋な HTML / CSS / JS のみ
- CSS は <style> タグ内に記述
- 画像は unsplash またはプレースホルダー

【自動生成ファイル一覧】

## 1. index.html
すべてを 1ファイルにまとめて出力してください。

## 2. package.json
\`\`\`json
{
  \"name\": \"[クライアント名]-lp\",
  \"version\": \"1.0.0\",
  \"scripts\": {
    \"watch\": \"node scripts/watch.js\",
    \"push\": \"node scripts/auto-push.js\"
  }
}
\`\`\`

## 3. scripts/ フォルダ
- auto-push.js（yamaguti-LP と同じ仕様）
- watch.js（yamaguti-LP と同じ仕様）
- setup-[クライアント名]-command.sh（Bash エイリアス登録）

## 4. assets/ フォルダ構成
\`\`\`
assets/
├── images/
├── icons/
└── logo/
\`\`\`

## 5. docs/ フォルダ
- DEPLOYMENT.md
- PERFORMANCE.md
- SEO.md

## 6. root ファイル
- .gitignore
- .gitattributes
- README.md
- KNOWLEDGE.md
- progress.md
- task.md
- CHANGE_LOG.md（初期テンプレート）

【参考】
yamaguti-LP/ の構成をベースに、[クライアント名] でカスタマイズしてください。

すべてのファイルを生成してください。
\`\`\`

---

## バリエーション

### シンプル版（セクション最小化）

\`\`\`
シンプルな構成（FV → サービス → Contact のみ）で生成してください。
\`\`\`

### リッチ版（アニメーション重視）

\`\`\`
以下のアニメーションを追加してください：
- パーティクル背景（FV）
- カウントアップアニメーション（実績数値）
- スムーススクロール
- ハンバーガーメニュー（SP）
\`\`\`

---

## 実行後の確認

- [ ] 全ファイルが生成されている
- [ ] package.json に scripts が定義されている
- [ ] スマホ表示が崩れていない
- [ ] Lighthouse スコア 90+ 達成可能な構成か
- [ ] GitHub push で自動デプロイできる構成か
"