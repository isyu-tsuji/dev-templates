# Pythonコードレビューチェックリスト

## Python固有
- [ ] PEP8準拠（black, flake8）
- [ ] 型ヒント（typing）の使用
- [ ] with文の活用（ファイル、DB接続）
- [ ] 例外の適切な継承
- [ ] リスト内包表記の活用
- [ ] __all__ の定義
- [ ] docstringの記述（Google/NumPy形式）

## パッケージ管理
- [ ] requirements.txtの更新
- [ ] 仮想環境の使用
- [ ] 依存バージョンの固定

## Flask/Django特化
- [ ] ルーティングの適切性
- [ ] テンプレートのXSS対策
- [ ] Blueprint/App活用
- [ ] セッション管理
- [ ] ORMの適切な使用
