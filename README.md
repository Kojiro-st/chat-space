## groupテーブル
|column|Type|Options|
|------|----|-------|
|group_name|text|cnull: false|

## Association
has_many :user_id, through: :groups_users
has_many :message, groups_users

## userテーブル
|column|Type|Options|
|------|----|-------|
|Email|text|null:false|
|password|text|null: false|
|nickname|text|null: false|
|group_name|text|cnull: false|

## Association
has_many :group_id, through: :groups_users
has_many :message, :group

## Messageテーブル
|column|Type|Options|
|------|----|-------|
|body|text||
|image|string||
|group_id|integer|null: false|
|user_id|integer|null: false|

## Association
- belongs_to :users
- belongs_to :groups

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user