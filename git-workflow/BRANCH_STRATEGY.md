# Git ブランチ戦略

## ブランチ構成

### main（本番）
- 本番環境にデプロイされるコード
- 常に安定した状態を保つ
- 直接pushは禁止

### develop（開発）
- 開発中の最新コード
- feature ブランチの統合先
- 定期的に main にマージ

### feature/xxx（機能開発）
- 新機能開発用
- develop からブランチ
- 完了後 develop にマージ

### hotfix/xxx（緊急修正）
- 本番の緊急バグ修正
- main からブランチ
- 完了後 main と develop にマージ

## ブランチ命名規則
```
feature/ユーザー認証実装
feature/天気API連携
bugfix/ログインエラー修正
hotfix/決済処理の不具合
```

## 運用フロー

### 1. 機能開発
```bash
git checkout develop
git pull
git checkout -b feature/新機能名
# 開発作業
git add .
git commit -m "feat: 新機能の説明"
git push origin feature/新機能名
# Pull Request作成 → レビュー → マージ
```

### 2. バグ修正
```bash
git checkout develop
git checkout -b bugfix/バグ名
# 修正作業
git commit -m "fix: バグの説明"
```

### 3. 緊急修正
```bash
git checkout main
git checkout -b hotfix/問題名
# 修正
git commit -m "hotfix: 緊急修正の説明"
# main と develop の両方にマージ
```
