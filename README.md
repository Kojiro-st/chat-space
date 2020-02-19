## Messageテーブル

|column|Type|Options|
|------|----|-------|
|body|text|null: false, foreign_key: true|
|image|string|null: false, foreign_key: true|
|group_id|integer|null: false, |
|user_id|integer|null: false, |

## Association
- belongs to :user_id
- belongs to :group_i