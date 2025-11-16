# 開発テンプレート集

プロジェクト開発で繰り返し使えるチェックリスト・テンプレート集

## 📂 構成と使用タイミング

### �� code-review/
**コードレビュー時に使用**

- `REVIEW_CHECKLIST.md` - 汎用レビューチェックリスト
- `PYTHON_REVIEW.md` - Python特化版
- `API_REVIEW.md` - Web API特化版

**使用例：**
```bash
# プロジェクトにコピー
curl -o docs/REVIEW_CHECKLIST.md https://raw.githubusercontent.com/isyu-tsuji/dev-templates/main/code-review/REVIEW_CHECKLIST.md

# Cursorでレビュー時に参照
# @docs/REVIEW_CHECKLIST.md に従って @api.py をレビューして
```

---

### 🌿 git-workflow/
**プロジェクト開始時・新メンバー参加時に使用**

- `BRANCH_STRATEGY.md` - ブランチ戦略とフロー
- `COMMIT_MESSAGE.md` - コミットメッセージ規約
- `PULL_REQUEST_TEMPLATE.md` - PRテンプレート

**使用例：**
```bash
# プロジェクト開始時にチームで確認
cat git-workflow/BRANCH_STRATEGY.md

# PRテンプレートをGitHubに設定
mkdir .github
cp git-workflow/PULL_REQUEST_TEMPLATE.md .github/PULL_REQUEST_TEMPLATE.md
```

---

### 🚀 project-setup/
**新プロジェクト作成時に使用**

- `PROJECT_INIT_CHECKLIST.md` - 初期設定チェックリスト
- `README_TEMPLATE.md` - READMEテンプレート
- `GITIGNORE_PYTHON.txt` - Python用 .gitignore
- `GITIGNORE_NODE.txt` - Node.js用 .gitignore

**使用例：**
```bash
# 新プロジェクト作成時
mkdir new-project && cd new-project
git init

# テンプレートをコピー
curl -o README.md https://raw.githubusercontent.com/isyu-tsuji/dev-templates/main/project-setup/README_TEMPLATE.md
curl -o .gitignore https://raw.githubusercontent.com/isyu-tsuji/dev-templates/main/project-setup/GITIGNORE_PYTHON.txt

# チェックリストに従ってセットアップ
```

---

## 🎯 典型的な使用フロー

### 1. 新プロジェクト開始時
```bash
# ① セットアップ
└─ project-setup/PROJECT_INIT_CHECKLIST.md を確認
└─ README_TEMPLATE.md をコピー
└─ .gitignore をコピー

# ② Git運用ルール決定
└─ git-workflow/BRANCH_STRATEGY.md をチームで確認
└─ COMMIT_MESSAGE.md を共有
```

### 2. 開発中
```bash
# コミット前
└─ git-workflow/COMMIT_MESSAGE.md に従ってメッセージ作成

# PR作成時
└─ git-workflow/PULL_REQUEST_TEMPLATE.md を使用

# コードレビュー時
└─ code-review/REVIEW_CHECKLIST.md でチェック
```

---

## 💡 Tips

### Cursorで活用
```
@docs/REVIEW_CHECKLIST.md に従って @api.py を日本語でレビューして
```

### GitHub設定
```bash
# PRテンプレートを設定
mkdir .github
cp git-workflow/PULL_REQUEST_TEMPLATE.md .github/
```

### エイリアスで素早くアクセス
```bash
# ~/.bashrc or ~/.zshrc
alias review='curl -s https://raw.githubusercontent.com/isyu-tsuji/dev-templates/main/code-review/REVIEW_CHECKLIST.md'
```

---

## 📝 今後追加予定

- [ ] テストケースチェックリスト
- [ ] セキュリティチェックリスト
- [ ] パフォーマンス最適化ガイド
- [ ] デプロイメントチェックリスト

---

## 🤝 コントリビューション

改善提案やテンプレート追加は Issue/PR でお願いします！

## 📄 ライセンス

MIT License - 自由に使ってください
