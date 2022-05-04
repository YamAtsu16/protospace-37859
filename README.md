# usersテーブル

| Colum              | Type   | Options               |
| ------------------ | ------ | --------------------- |
| email              | string | not_null, ユニーク制約  |
| encrypted_password | string | not_null              |
| name               | string | not_null              |
| profile            | text   | not_null              |
| occupation         | text   | not_null              |
| position           | text   | not_null              |

# prototypesテーブル

| Colum       | Type   | Options                 |
| ----------- | ------ | ----------------------- |
| title       | string       | not_null          |
| catch_copy  | text         | not_null          |
| concept     | text         | not_null          |
| user        | references   | not_null, 外部キー |

# commentsテーブル

| Colum       | Type         | Options           |
| ----------- | ------------ | ----------------- |
| concept     | text         | not_null          |
| prototype   | references   | not_null, 外部キー |
| user        | references   | not_null, 外部キー |