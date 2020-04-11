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
- belongs_to :group_user
- has_many :message



## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|group_name|integer|null: false|

### Association
- belongs_to :group_user


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

<!-- データベースの初期化 -->
* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
