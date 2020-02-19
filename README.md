## groupテーブル
|column|Type|Options|
|------|----|-------|
|group_id|integer|null: false|
|user_id|integer|null: false|
|Email|text|null:false|

## Association
has_many :user_id, through: :message

## userテーブル
|column|Type|Options|
|------|----|-------|
|group_id|integer|null: false|
|user_id|integer|null: false|
|Email|text|null:false|
|password|text|null: false|
|nickname|text|null: false|

## Association
has_many :group_id, through: :message

## Messageテーブル
|column|Type|Options|
|------|----|-------|
|body|text|null: false, foreign_key: true|
|image|string|null: false, foreign_key: true|
|group_id|integer|null: false|
|user_id|integer|null: false|

## Association
- belongs to :user_id
- belongs to :group_i

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user