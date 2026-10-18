# dev-standard

アプリケーションやWeb開発で繰り返し使える設計標準、実装パターン、テンプレートを蓄積するリポジトリです。

Reusable development standards, patterns, and implementation templates for application and web development.

## 目的 / Vision

開発で繰り返し発生する設計判断を、再利用・テスト可能で機械可読な標準として整理します。将来的には、AIとの対話を通じて要件に合う部品を選択し、組み合わせられる開発基盤を目指します。

Reduce repeated development effort by turning recurring engineering decisions into reusable, testable, machine-readable standards that can be selected and assembled through AI dialogue.

## 標準化モデル / Model

`Feature → Pattern → Standard → Template → Variant`

- **Feature（機能）**：認証、検索、ファイルアップロードなど、アプリが提供する機能
- **Pattern（パターン）**：機能を実現する代表的な方式
- **Standard（標準）**：品質・セキュリティなど、共通して満たすべき仕様や基準
- **Template（テンプレート）**：実装時に再利用できるコードや構成
- **Variant（派生形）**：特定の技術スタックや条件に合わせたバリエーション

最初からすべてを完成させるのではなく、PoCや実利用で再利用性を確認しながら段階的に整備します。

The goal is to evolve from a human-maintained standard library into an AI-accessible development foundation.

## リポジトリ利用上の必須ルール / Mandatory rules

このリポジトリは**公開リポジトリ**です。顧客・勤務先に固有の情報、機密情報、認証情報、個人情報などをコミットしないでください。

AIエージェントが変更を行う場合は、必ず [`AI_RULES.md`](./AI_RULES.md) に従ってください。セキュリティ、公開可否、分類、レビューのルールは必須です。

This is a **public repository**. Do not commit confidential, customer-specific, employer-specific, credential, personal, or otherwise non-public information.

## ドキュメント案内 / Repository guide

- [`docs/philosophy.md`](./docs/philosophy.md)：設計思想・原則
- [`docs/architecture.md`](./docs/architecture.md)：全体モデルとAIによる選択フロー
- [`docs/repository-structure.md`](./docs/repository-structure.md)：ディレクトリ構成と責務
- [`docs/contribution.md`](./docs/contribution.md)：Issue / PRを使った開発フロー
- [`AI_RULES.md`](./AI_RULES.md)：AIが変更する際の必須ルール
- [`catalog/features.md`](./catalog/features.md)：標準化対象の機能カタログ
- [`catalog/patterns.md`](./catalog/patterns.md)：再利用可能なパターンのカタログ

## 現在の状況 / Current status

リポジトリの基本構造と共通ルールを整備し、現在は **Authentication（認証）** を最初の概念実証（PoC）として、次の一連の流れを検証しています。

`Feature → Pattern → Standard → Template → Variant`

機能カタログには、Authentication、User、Authorization、CRUD、Form、Validation、Error Handling、API、Database、File Uploadなどを掲載しています。対象を一度に増やすのではなく、最初のPoCを通じて標準化の流れを検証してから拡張します。

## 次の作業 / Next focus

1. 認証PoCを完成させる
2. 各成果物が再利用・組み合わせ可能か検証する
3. 一連の流れを検証した後、対象となる標準を追加する
4. 実際の利用結果をもとに、AIが読み取り・選択しやすいメタデータとルールを改善する
