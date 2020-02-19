## groupテーブル
|column|Type|Options|
|------|----|-------|
|name|string|null: false|

## Association
has_many :users, through: :groups_users
has_many :messages
has_many :groups_users

## userテーブル
|column|Type|Options|
|------|----|-------|
|Email|text|null:false|
|password|text|null: false|
|nickname|text|null: false|

## Association
has_many :groups, through: :groups_users
has_many :messages
has_many :groups_users

## Messageテーブル
|column|Type|Options|
|------|----|-------|
|body|text||
|image|string||
|group_id|integer|null: false|
|user_id|integer|null: false|

## Association
- belongs_to :user
- belongs_to :group

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user