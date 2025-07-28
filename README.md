# README
# フルスタックToDoアプリケーション ✅

このアプリケーションは以下で構成されています：
- 複数ユーザー対応の **Ruby on Rails（API専用）** バックエンド
- Rails API と通信するモダンな **React フロントエンド**

---

## プロジェクト概要

バックエンドは Rails（APIモード）と PostgreSQL で構築されており、`User` モデルと `Task` モデル（Task は User に属する）を備えています。  
フロントエンドは React により構築され、Axios を使ってバックエンドと通信します。スタイルには TailwindCSS（任意）を使用可能です。

---

## 技術スタック

### バックエンド
- Ruby on Rails 7（APIモード）
- PostgreSQL
- Rack CORS（クロスオリジンリクエスト対応）
- bcrypt（パスワードハッシュ化）

### フロントエンド
- React（Hooks使用）
- Axios（HTTPクライアント）
- TailwindCSS（任意）

---

## ER図（データベースモデル）
+––––+             +––––+
|  User  |───< has_many|  Task  |
+––––+             +––––+
| id     |             | id     |
| name   |             | title  |
| email  |             | done   |
| password_digest      | user_id|
| created_at           | created_at
| updated_at           | updated_at
+––––+             +––––+

---

## セットアップ手順

```bash
# バックエンド
cd todo-api
bundle install
rails db:create db:migrate
rails s

# フロントエンド
cd todo-frontend
npm install
npm start

⸻

機能一覧
	•	✅ タスクの追加 / 編集 / 削除
	•	✅ タスクにユーザーを関連付け
	•	✅ React フロントエンドと連携する API 専用バックエンド