##usersテーブル
| Columun     |  Type   | Options     |
| ----------- | ------- | ----------- |
| emal        | string  | null: false |
| password    | string  | null: false |
| name        | string  | null: false |
| profile     | text    | null: false |
| occupation  | text    | null: false |
| position    | text    | null: false |

###Association

-has_many :comments
-has_many :prototypes

##prototypesテーブル
| Columun     |   Type   | Options          |
| ----------- | -------- | -----------      |
| title       | string   | null: false      |
| catch_copy  | text     | null: false      |
| concept     | string   | null: false      |
| user        |references|foreign_key: true |

 
 ###Association

-has_many :users
-has_many :comments

commentsテーブル
| Columun     |  Type    | Options           |
| ----------- | -------- | -----------       |
| text        | string   | null: false       |
| user        |references| foreign_key: true | 
| prototypes  |references| foreign_key: true |

 ###Association

-has_many :users
-has_many :prototypes