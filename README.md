# テーブル設計

## userテーブル
| colum               | Type      | Option                |
|---------------------|-----------|-----------------------|
| email               | string    | null: false           |
| encrypted_password  | string    | null: false           |
| name                | text      | null: false           |
| profile             | text      | null: false           |
| occupation          | text      | null: false           |
| position            | text      | null: false           |

## commentsテーブル
| colum                | Type       | Option                          |
|----------------------|------------|---------------------------------|
| content              | text       | null: false                     |
| prototype            | references | null:  false, foreign_ket: true |
| user                 | references | null:  false, foreign_ket: true |

## prototypesテーブル
| colum                | Type       | Option                          |
|----------------------|------------|---------------------------------|
| title                | string     | null: false                     |
| catch_copy           | text       | null: false                     |
| concept              | text       | null: false                     |
| user                 | references | null:  false, foreign_ket: true |
