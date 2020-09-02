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

# テーブル設計

## users テーブル

| Colum    | Type   | Options     |
| -------- | ------ | ----------- |
| nickname | string | nill: false |
| email    | string | nill: false |
| password | string | nill: false |

### Association

has_many :musics

## musics テーブル

| Column         | Type       | Options                        |
| -------------- | ---------- | ------------------------------ |
| user           | references | nill: false, foreign_key: true |
| name           | string     | nill: false                    |
| genre_id       | integer    | nill: false                    |
| representative | string     | nill: false                    |
| mail           | string     | nill: false                    |
| prefecture_id  | integer    | nill: false                    |
| post_code      | string     | nill: false                    |
| city           | string     | null: false                    |
| house_number   | string     | null: false                    |
| building_name  | string     |                                |
| phone_number   | string     | null: false                    |
| station        | string     | null: false                    |
| walk           | integer    | null: false                    |

### Association

belongs_to :user
