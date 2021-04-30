# README

## usersテーブル

| Column     |  Type  | Options     |
| ---------- | ------ | ----------- |
| email      | string | nill: false |
| password   | string | nill: false |
| name       | string | nill: false |
| profile    | text   | nill: false |
| occupation | text   | nill: false |
| position   | text   | nill: false |


## Association
- has-many :prototype
- has-many :comment



## prototypesテーブル

| Column     | Type       | Options           |
| -------    | ------     | ----------------- |
| title      | string     | nill: false       |
| catch_copy | text       | nill: false       |
| concept    | text       | nill: false       |
| user       | references | foreign_key: true |


## Association
- belongs_to :user
- has-many :comments

## commentsテーブル

| Column    | Type      | Options           |
| --------- | --------- | ----------------- |
| text      | text      | nill: false       |
| user      | reference | foreign_key: true |
| prototype | reference | foreign_key: true |


## Association
- belongs_to :user
- belongs_to :prototype
