# MMOくん

起動方法:

以下のようなsetting.jsonを作成してください。

```json
{
 "token": "YOUR BOT TOKEN"
}
```


必要なパッケージをインストールしてください。

```bash
pip install -r requirements.txt
```

データベースを作成してください。

```sql
$ sqlite3 mmo.db 
           
sqlite> CREATE TABLE player(user_id INTEGER, experience INTEGER);
sqlite> CREATE TABLE channel_status(channel_id INTEGER, boss_level INTEGER, boss_hp INTEGER);
sqlite> CREATE TABLE in_battle(channel_id INTEGER, user_id INTEGER, player_hp INTEGER);
sqlite> CREATE TABLE training(user_id INTEGER, training_question INTEGER);
sqlite> CREATE TABLE channel_in_transaction(channel_id INTEGER);
sqlite> CREATE TABLE item(user_id INTEGER, item_id INTEGER, count INTEGER);
```

起動します。

```bash
python mmo.py
```