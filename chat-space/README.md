# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|name|string|null: false,index: ture|

## Association
- has_many : messages
- has_many : group_users
- has_many : grousp, through: :group_users



## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|image|strig||
|text|text||
|user|references|foreign_key: true,null: false|
|group|references|foreign_key: true,null: false|

## Association
- belog_to :user
- belong_to :groups

## groupsテーブル
|Column|Type|Options|
|------|----|---|
|name|string|null: false|
## Association
- has_many :messages
- has_many :group_users
- has_many :users, through group_users

##　groups_usersテーブル
|Column|Type|Options|
|------|----|---|
|users|references|null: false,foreign_key:true|
|group|references|null: false,foreign_key:true|

- belog_to :user
- blong_to :group






