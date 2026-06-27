# Contributing

## 前提条件

- Xcode 15+
- iOS 17+ シミュレーターまたは実機
- Supabase CLI

## セットアップ

1. リポジトリをクローン
2. Supabaseのプロジェクト設定を `.env` に記述
3. Xcode でスキームを選択してビルド

## ブランチ戦略

| ブランチ | 用途 |
|---|---|
| `main` | リリース可能な状態を常に保つ |
| `dev` | 統合ブランチ。機能をまとめて検証してから `main` へマージ |
| `feature/*` | 機能開発 |
| `fix/*` | バグ修正 |

`main` への直接プッシュは禁止。必ずPRを経由する。
マージ順: `feature/*` → `dev` → `main`

## 開発フロー

1. `dev` から作業ブランチを切る
2. **TDDで実装する**（[rules/process.md](rules/process.md) 参照）
3. `dev` へPRを作成してレビューを依頼
4. CIが通ったらマージ
5. リリース時に `dev` → `main` へPRを作成してマージ

## コミットメッセージ

```
<type>: <概要>

例:
feat: スポット一覧にフィルター機能を追加
fix: Share Extension で URL が空になるバグを修正
test: PairRepositoryのユニットテストを追加
```

`type` は `feat` / `fix` / `test` / `refactor` / `docs` / `chore` のいずれか。

## PR のルール

- 1PR = 1機能 or 1バグ修正
- テストが含まれていないPRはマージしない
- レビュワーは最低1名の承認を必要とする
