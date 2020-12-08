## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false
|email|string|unique: true
|password|string|null: false
### Association
- has_many :message
- has_many :users_message

## messageテーブル
|Column|Type|Options|
|------|----|-------|
|title|null: false
|text| null: false
### Association
- has_many :message
- has_many :users_message

## users_messageテーブル
|Column|Type|Options|
|------|----|-------|
|users_id|integer|null: false, foreign_key: true|
|message_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user