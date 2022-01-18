# dec_project(仮)

## 目次
1. [命名規則](#命名規則)

## 命名規則

### テーブル
* snake_case
* テーブル名
  * 複数形
* カラム名 単数形
  * 外部キーは参照先のテーブル名_カラム名

### モデル
* UpperCamel
* 単数形
  * テーブル名を単数形に変換したファイル名にする
* マイグレーションファイル
  * snake_case
* シーダーファイル
  * UpperCamel
  * 単数形or複数系
  * 最後はSeederとする

### コントローラー
* UpperCamel
* ファイル名の最後はControllerとする

### ビュー
* snake_case
* 単数形or複数系

### コーディング関連
* クラス名
  * UpperCamel
* メソッド名
  * lowerCamel
* 変数名
  * snace_case
* ディレクトリ名
  * UpperCamel
* ファイル名
  * snake_case       
