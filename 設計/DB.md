# DB設計書
[ER図](ER図.md)

## 目次
### [テーブル一覧](#テーブル一覧)
* [ユーザーテーブル](#users)
* [ログインテーブル](#authorizations)
* [質問テーブル](#questions)
* [回答テーブル](#answers)
* [記事テーブル](#articles)
* [引用テーブル](#quotes)
### データ分析に関する雑記表   

## テーブル一覧

### users
|論理名|物理名|型|PK|FK|NN|
|:---|:---|:---|:---:|:---:|:---:|
|ユーザーID|id|integer|○||○|
|ユーザー名|name|string|||○|
|メールアドレス|email|string|||○|
|パスワード|password|string|||○|
|作成日時|created_at|datetime|||○|
|更新日時|updated_at|datetime|||○|
|削除日時|deleted_at|datetime||||

### authorizations
|論理名|物理名|型|PK|FK|NN|
|:---|:---|:---|:---:|:---:|:---:|
|ログインID|id|string|○|||
|ユーザーID|users_id|integer||○||
|作成日時|created_at|datetime|||○|
|更新日時|updated_at|datetime|||○|

### follow
|論理名|物理名|型|PK|FK|NN|
|:---|:---|:---|:---:|:---:|:---:|
|ユーザーID|users_id|integer|○|○||
|フォローID|followee_id|integer|○|○||
|作成日時|created_at|datetime|||○|

### questions
|論理名|物理名|型|PK|FK|NN|
|:---|:---|:---|:---:|:---:|:---:|
|質問ID|id|integer|○||○|
|ユーザーID|users_id|integer||○|○|
|質問タイトル|title|string|||○|
|質問本文|content|string|||○|
|質問補足|content|string||||
|作成日時|created_at|datetime|||○|
|更新日時|updated_at|datetime|||○|
|削除日時|deleted_at|datetime||||

### answers
|論理名|物理名|型|PK|FK|NN|
|:---|:---|:---|:---:|:---:|:---:|
|回答ID|id|integer|○||○|
|質問ID|questions_id|integer||○|○|
|ユーザーID|users_id|integer||○|○|
|回答本文|content|string|||○|
|作成日時|created_at|datetime|||○|
|更新日時|updated_at|datetime|||○|
|削除日時|deleted_at|datetime||||

### articles
|論理名|物理名|型|PK|FK|NN|
|:---|:---|:---|:---:|:---:|:---:|
|記事ID|id|integer|○||○|
|ユーザーID|users_id|integer||○|○|
|記事タイトル|title|string|||○|
|回答本文|content|string|||○|
|作成日時|created_at|datetime|||○|
|更新日時|updated_at|datetime|||○|
|削除日時|deleted_at|datetime||||

### quotes
|論理名|物理名|型|PK|FK|NN|
|:---|:---|:---|:---:|:---:|:---:|
|引用ID|id|integer|○||○|
|記事ID|users_id|integer||○|○|
|質問ID|questions_id|string|||○|
|作成日時|created_at|datetime|||○|
|更新日時|updated_at|datetime|||○|
|削除日時|deleted_at|datetime||||
