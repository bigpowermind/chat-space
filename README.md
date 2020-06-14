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

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|

### Association
- has_many :user

## usersテーブル

Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|

### Association
- has_many :group

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## multiple_chat_functionテーブル

|Column|Type|Options|
|------|----|-------|
|multiple_body|text|null: false, foreign_key: true|

### Association
- has_many :user
- has_many :body

## search_function

|Column|Type|Options|
|------|----|-------|

|search|string|add_index: unique: true, null: false|

### Association
- belongs_to :user

## user_invitation_function

|Column|Type|Options|
|------|----|-------|
|user_invitation|integer|add_index: unique: true, null: false, foreign_key: true|

### Asociation
- belongs_to :user
- belongs_to :group

## chat_history_display_function

|Column|Type|Options|
|------|----|-------|
|history|text|null: false, foreign_key: true|

### Asociation
- belongs_to :user
- belongs_to :group

##  image_transmission_function

|Column|Type|Options|
|------|----|-------|
|image|string|null: false, foreign_key: true|

### Asociation
- belongs_to :user
- belongs_to :group

## chat_automatic_update_function

|Column|Type|Options|
|------|----|-------|
|chat_update|text|null: false, foreign_key: true|

### Asociation
- has_many :body
- belongs_to :group

