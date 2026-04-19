---

## Step 1: セットアップ

プロジェクトフォルダを作成し、クライアント情報・競合分析を実施する。

**所要時間**: 5〜10分

**実行方法**:
```bash
cd C:\Github\genba-agent-prompts\HP作成
cursor code "@セットアップ/セットアップ.md を実行"
```

**出力ファイル**:
- `セットアップ/セットアップ.md` 
  - 以下を記載:
    - **クライアント名**: {値}
    - 業種
    - ターゲット層
    - 競合分析結果

---

## Step 2: HTML自動生成

セットアップから **CLIENT_NAME を自動抽出** し、HTML/CSS/JS を一括生成。

**所要時間**: 10〜30分（規模による）

**実行方法**:
```bash
cursor code "@02_HTML自動生成.md を実行。セットアップ.md から CLIENT_NAME を抽出して使用してください"
```

**自動実行内容**:
- セットアップ.md から CLIENT_NAME を抽出
- PROJECT_PATH = C:\Github\${CLIENT_NAME}-LP を自動設定
- 以下をファイル生成:
  - `${PROJECT_PATH}\index.html`
  - `${PROJECT_PATH}\package.json`
  - `${PROJECT_PATH}\scripts\auto-push.js`
  - `${PROJECT_PATH}\scripts\watch.js`
  - `${PROJECT_PATH}\scripts\setup-${CLIENT_NAME}-command.sh`
  - `${PROJECT_PATH}\docs\*`
  - `${PROJECT_PATH}\root-files\*`

---

## Step 3: コマンド化・エージェント化

完成したワークフローをカスタムコマンド化し、次回以降ワンコマンドで再現可能に。

**所要時間**: 5分

**実行方法**:
```bash
cursor code "@04_佐瀬LP自動化エージェント化.md を実行。CLIENT_NAME=${CLIENT_NAME} を使用してください"
```

**自動実行内容**:
- Bash エイリアス登録: `alias ${CLIENT_NAME}='function _${CLIENT_NAME}_agent() { ... }'`
- 修正コマンド自動化完成

---

## 🚀 ワンコマンド実行例

```bash
cursor code "セットアップ.md から CLIENT_NAME を抽出して、WORKFLOW.md に沿ってホームページを完全自動作成してください"
```

↓

**自動実行フロー**:
1. セットアップ.md を読み込む
2. CLIENT_NAME を抽出（例: "佐瀬大輔"）
3. PROJECT_PATH を自動設定（C:\Github\佐瀬大輔-LP）
4. HTML自動生成実行
5. コマンド化完成
6. GitHub push 準備完了

---

## チェックリスト

- [ ] WORKFLOW.md を読み込んだ
- [ ] セットアップ.md にクライアント名を記載した
- [ ] FV（ファーストビュー）が完成している
- [ ] CTA（問い合わせボタン等）が設置されている
- [ ] SP（スマホ）表示を確認した
- [ ] Lighthouse スコアを確認した（目標: Performance 90+）
- [ ] GitHub に push した
- [ ] コマンド化が完成している