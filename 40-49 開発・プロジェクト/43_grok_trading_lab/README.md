# Grok Trading Lab

暗号資産のAI自動トレードを研究する個人開発プロジェクト。

**現在はペーパー取引の検証段階。実資金による運用は対象外。**

## 現状（2026-11-16）

- Windows / PowerShell / Python 3.13 / `.venv` を使用。
- Grokを用いるトレードBotとStreamlitダッシュボードを開発中。
- SQLiteに資産履歴を保存する機能を追加。
- 初期資金1,000 USDT、保有銘柄なし、取引0件、資産記録1件を確認。
- 日次損失ガードを追加・重複処理を修正。発動試験は未確認。

## 目標

まず暗号資産のみを対象に、複数の専門AIが独立分析・反論・検証を行い、統括AIが最終判断する組織会議方式を構築する。独立したリスク管理プログラムには拒否権を持たせる。FX・株式は資金が集まった後の将来構想。

## 起動方法

詳細は [SETUP](docs/SETUP.md) を参照。

```powershell
python -m streamlit run app/dashboard.py
```

## ドキュメント

- [実装機能](docs/FEATURES.md)
- [システム構成](docs/ARCHITECTURE.md)
- [AI組織設計](docs/AI_ORGANIZATION.md)
- [セットアップ](docs/SETUP.md)
- [テスト計画](docs/TEST_PLAN.md)
- [ロードマップ](ROADMAP.md)
- [変更履歴](CHANGELOG.md)

## 注意

本資料は会話中の開発記録に基づく。最新ソース全体やGitHubリポジトリは未照合。未確認の設定・機能は実装済みとみなさない。収益性や実取引の安全性は保証しない。APIキーや実データは公開しない。
