#Visualize your schema

Open this file in your text editor and visualize your schema. At the top is your table name. Listed below are all the columns in that table.

## User

id
first_name
last_name

## Address

id
user_id
street
street2
city
state
zip_code
country

In the example above, each Address can belong to a User. This is achieved by adding a column called `user_id`, which can match only ONE of the values in the `id` column of the User table. Remember, `id`s are unique; no table can have two `id` values that are the same.

Using the above format, jot down the database for your apps below!

## GrubHub Online Ordering

## orders

id PK int
menu_item_id int FK >- menu_items.id
user_id int FK >- users.id

## restaurants

id PK int
name string
address string
menu_item_id int FK >- menu_items.id

## menu_items

id PK int
name string
price int
available boolean

## users

id PK int
first_name string
last_name string
phone_number string

## Blue Apron

## users

id PK int
first_name string
last_name string
address string
service_plan_id int FK >- service_plans.id

## service_plans

id PK int
promotion_id int FK >- promotions.id
delivery_id int FK >- deliveries.id

## recipes

id PK int
ingredient string

## promotions

id PK int
discount_percentage int

## deliveries

id PK int
is_available boolean
price int

## Instagram

## users

id PK int
first_name string
last_name string
display_name string

## posts

id PK int
content string
user_id int FK >- users.id

## comments

id PK int
content string
post_id int FK >- posts.id

## likes

id PK int
comment_id int FK >- comments.id

## follows

id PK int
user_id int FK >- users.id
