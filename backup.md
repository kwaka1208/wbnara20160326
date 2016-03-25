## MySQL
すべてのデータベースのデータを"backup.sql"に保存する。  
以下のコマンドを実行するとパスワードを聞かれるので、`username`のパスワードを入力。

### バックアップ対象のデータ
|データ|バックアップの可否|
|:--:|:--:|
|投稿データ|○|
|画像データ|×|
|プラグイン|×|

`mysqldump -u {username} -p -x --all-databases > backup.sql`

## wp-cli `export`コマンド

### バックアップ対象のデータ
|データ|バックアップの可否|
|:--:|:--:|
|投稿データ|○|
|画像データ|○|
|プラグイン|○|

`wp export --dir=/tmp/ --user=admin --post_type=post --start_date=2011-01-01 --end_date=2011-12-31`
