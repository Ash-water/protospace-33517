## users table

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| name       | string | null: false |
| email      | string | null: false |
| password   | string | null: false |
| profile    | text   | null: false |
| occupation | text   | null: false |
| position   | text   | null: false |

### Association

- has_many :comments
- has_many :prototypes

## comments table

| Column    | Type       | Options     |
| --------- | ---------- | ----------- |
| text      | text       | null: false |
| user      | references |             |
| prototype | references |             |

### Association

- belongs_to :user
- belongs_to :prototypes

## Prototypes table

| Column     | Type       | Options     |
| ---------  | ---------- | ----------- |
| title      | string     | null: false |
| catch_copy | text       | null: false |
| user       | references |             |
