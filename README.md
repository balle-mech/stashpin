# Stashpin

SNSで見つけた「行きたい場所」を3タップで保存でき、他社とリストを共有もできるiOSアプリ。

## 特徴

- **Share Extension対応** — Instagram / TikTok / X / Webの共有シートからそのまま保存
- **きっかけへの導線** — 「どのSNSで見たか」を元URL付きで記録、いつでも元投稿に戻れる
- **ペアリスト** — 招待コードで2人を紐づけ、リアルタイム同期
- **ステータス管理** — 「行きたい」→「行った！」で記録

## 技術スタック

| レイヤー | 技術 |
|---|---|
| フロントエンド | SwiftUI（iOS 17+） |
| Share Extension | SwiftUI + App Groups |
| 認証 | Supabase Auth（Apple / Google） |
| データベース | Supabase (PostgreSQL + RLS) |
| リアルタイム同期 | Supabase Realtime |
| プッシュ通知 | APNs + Supabase Edge Functions |
| CI/CD | Xcode Cloud or GitHub Actions |

## 画面構成（MVP）

- ログイン / ペアリング
- スポット一覧（ホーム）
- スポット詳細
- スポット手動追加
- Share Extension UI（ミニシート）
- 設定

## 開発体制

- 開発: 2人（週末中心、週4h程度）
- 環境: Xcode / GitHub / Supabase
- Phase 1 MVP目標: 約2ヶ月
