# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

<!-- 構成 -->
* Configuration


<!-- データベースの作成 -->
* Database creation　

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false, add_index|
|adress|string|null: false|
|password|string|null: false|

### Association
- has_many :group_users
  has_many :groups, through: :group_users
- has_many :messages



## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|group_name|integer|null: false|

### Association
- has_many :group_users
  has_many :users, through: :group_users
  has_many :messages


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|image|

### Association
- belongs_to :user
  belongs_to :group

<!-- データベースの初期化 -->
* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
