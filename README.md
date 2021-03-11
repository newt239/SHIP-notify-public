# SHIP-notify
## 概要
詳細は[こちら](https://newt-house.web.app/ship-notify/)。
## 仕様
これから書きます。

## 今後の予定
### ウェブサイトの説明記述の刷新
Discordへの移行に伴う記述の変更。時間のあるときにやる。またREADMEの仕様セクションの書き込みも並行して行う。
### 検索機能
特定の単語をHeroku postgresで検索し、タイトルやパスなどの一覧を返す機能。複数ワードに対応した形での実装が望ましい。
### Discordのbot command frameworkへの一部コードの置き換え
他の機能の実装と並行して行う。
### ファイルを直接送信する機能
7月末を目処に開発をすすめる。
#### 実装フロー
- プッシュ型
1. Herokuでデータの取得＆ファイルダウンロード
1. Discordの専用チャンネルへのファイル送信＆Firebase Strageへのアップロード
- レスポンス型
1. コマンドで指定されたidを取得
1. idをもとにFirebase Strageへアクセス
1. 該当するファイルの送信orサイズが大きい場合はダウンロードリンクを送信
#### スケジュール
4月: 実力試験後作業開始。ローカル環境でのFirebase Strageの操作方法を理解、その後Heroku上でどのようにダウンロードしたファイルにアクセスするのか確認する。

5月: shipcheck.pyに組み込み、微調整

6月: プッシュ型の正式実装

7月: レスポンス型の実装

スケジュールは適宜変更する。
