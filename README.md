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

## users テーブル

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| name               | string | null: false |
| email              | string | null: false |
| encrypted_password | string | null: false |

### Association

- has_many :comments
- belongs_to :posts

## posts テーブル

| Column | Type   | Options     |
| ------ | ------ | ----------- |
| name   | string | null: false |
| place  | string | null: false |
| time   | string | null: false |
| supplement | string | null: false |

### Association

- has_many :comments
- belongs_to:users

## comments テーブル

| Column | Type       | Options                        |
| ------ | ---------- | ------------------------------ |
| water   |string | null: false |
| cold protection  | strings | null: false |
| posts | references |null: false,foreign_key: true|


### Association

- belongs_to :room
- belongs_to :user



* ...
