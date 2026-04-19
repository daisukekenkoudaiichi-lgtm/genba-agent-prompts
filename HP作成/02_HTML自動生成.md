【実行前提】
- セットアップ.md にクライアント情報が記載されていることを確認
- 新規プロジェクトフォルダを自動作成する必要がある

【ステップ0: 新フォルダ作成】
1. セットアップ.md からクライアント名を抽出
2. PROJECT_PATH = C:\Github\${CLIENT_NAME}-LP を生成
3. 新フォルダを自動作成：mkdir -p "${PROJECT_PATH}"
4. 初期ファイル構成を作成：
   - ${PROJECT_PATH}/index.html
   - ${PROJECT_PATH}/package.json
   - ${PROJECT_PATH}/scripts/
   - ${PROJECT_PATH}/assets/
   - ${PROJECT_PATH}/docs/
   - ${PROJECT_PATH}/root-files/

【ステップ1: クライアント情報抽出】
セットアップ.md から以下を抽出してコンテキストに保持：
- クライアント名
- 業種・特徴
- ターゲット層
- USP（ユニークセリングポイント）
- 参考サイト技術解析（HTML構造・CSS・色・レイアウト）
- 最適セクション構成（ヒーロー・サービス・事例・CTAなど）

【ステップ2: HTML自動生成】
セットアップの内容を基に、以下を自動生成：

## 1. index.html
- すべてを1ファイルにまとめて出力（完全自己完結型）
- CLAUDE.md のペルソナを反映
- SKILL.md のデザイン規約に準拠
- モバイルファースト設計
- Lighthouse 90+ 対応
- SEO最適化済み

## 2. package.json
- プロジェクト基本情報
- 必要な dependencies 記載
- scripts セクション：
  - "dev": dev server 起動
  - "build": production build
  - "start": start server
  - "push": auto-push スクリプト実行

## 3. scripts/ フォルダ
### 3-1. auto-push.js
- ${REFERENCE_LP} と同じ仕様
- 自動で git add / commit / push
- デプロイ前の自動テスト実行

### 3-2. watch.js
- ${REFERENCE_LP} と同じ仕様
- ファイル変更を監視
- Lighthouse スコア自動測定
- SEO自動チェック

### 3-3. setup-${CLIENT_NAME}-command.sh
- Bash エイリアス登録スクリプト
- ~/.bashrc に以下を追加：
```bash
  alias ${CLIENT_NAME}='function _${CLIENT_NAME}_agent() {
    cd "${PROJECT_PATH}"
    claude code "
    CLAUDE.md + SKILL.md + progress.md + task.md + KNOWLEDGE.md を読み込んで
    以下の修正を実行してください：
    $*
    【修正フロー】確認なし → 全て自動実行 → レポート表示
    "
  }; _${CLIENT_NAME}_agent'
```

## 4. assets/ フォルダ構成