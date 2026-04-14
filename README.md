# genba-agent-prompts

現場で即使える **Claude Code プロンプト集**。コピペするだけで業務自動化。

---

## クイックスタート

```bash
# 1. リポジトリをクローン
git clone https://github.com/daisukekenkoudaiichi-lgtm/genba-agent-prompts.git

# 2. 使いたいプロンプトを開く
cat HP作成/01_セットアップ.md

# 3. Claude Code に貼り付けて実行
claude
```

---

## ファイル構成

```
genba-agent-prompts/
├── CLAUDE.md               # Claude が自動読み込みする設定・概要
├── README.md               # このファイル
├── HP作成/
│   ├── 01_セットアップ.md  # プロジェクト初期化プロンプト
│   ├── 02_HTML自動生成.md  # LP・サイト自動生成プロンプト
│   ├── 03_コマンド化.md    # 繰り返し実行用コマンド化
│   └── WORKFLOW.md         # HP作成の全体ワークフロー
├── 人事自動化/
│   └── README.md           # 人事系プロンプト一覧
└── マーケ自動化/
    └── README.md           # マーケ系プロンプト一覧
```

---

## カテゴリ別プロンプト

### HP作成
LP・コーポレートサイトをゼロから自動生成するプロンプト群。
HTML/CSS/JS のみで完結する静的サイトを対象としています。

### 人事自動化
採用管理・面接スコアリング・勤怠集計など、人事担当者の日常業務を自動化するプロンプト群。

### マーケ自動化
SNS投稿文・メルマガ本文・広告コピーの生成など、マーケティング業務を効率化するプロンプト群。

---

## ライセンス

MIT
