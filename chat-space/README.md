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
|name|string|null: false|

## Association
- has_many : message
- has_many : group_users
- has_many : group through group_users



## messageテーブル
|Column|Type|Options|
|------|----|-------|
|image|strig||
|text|text|null: false|
|user_id|integer|foreign_key: true|
|group_id|integer|foreign_key: true|

## Association
- belog_to :users
- blong_to :group

## groupテーブル
|Column|Type|Options|
|------|----|---|
|user_id|integer|foreign_key: true|
|messsage_id|integer|foreign_key: true|

## Association
- has_many :message
- has_many :group_users
- has_many :users through group_users

##　group_usersテーブル
|Column|Type|Options|
|------|----|---|
|users_id|integer|null: false,foreign_key:true|
|group_id|integer|null: false,foreign_key:true|

- belog_to :users
- blong_to :group






