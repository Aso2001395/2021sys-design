## 購入テーブル

|テーブル名|項目名|型|PK|NN|FK|
|---------|------|--|--|--|--|
|d_purchase|order_id|bigint(20)|〇|〇|-|
|d_purchase|customer_code|varchar(50)|-|〇|-|
|d_purchase|purchase_date|date|-|〇|-|
|d_purchase|total_price|int(11)|-|〇|-|

## 購入テーブル詳細

|テーブル名|項目名|型|PK|NN|FK|
|---------|------|--|--|--|--|
|d_purchase_detail|detail_id|bigint(20)|〇|〇|-|
|d_purchase_detail|order_id|bigint(20)|〇|〇|-|
|d_purchase_detail|item_code|int(11)|-|〇|-|
|d_purchase_detail|price|int(11)|-|〇|-|
|d_purchase_detail|num|int(11)|-|〇|-|

## ユーザーテーブル

|テーブル名|項目名|型|PK|NN|FK|
|---------|------|--|--|--|--|
|m_customers|customer_code|varchar(50)|〇|〇|-|
|m_customers|pass|varchar(50)|-|〇|-|
|m_customers|name|varchar(20)|-|〇|-|
|m_customers|address|varchar(100)|-|〇|-|
|m_customers|tel|varchar(20)|-|〇|-|
|m_customers|mail|varchar(100)|-|〇|-|
|m_customers|del_flag|int(1)|-|-|-|
|m_customers|reg_date|date|-|〇|-|

## カテゴリテーブル

|テーブル名|項目名|型|PK|NN|FK|
|---------|------|--|--|--|--|
|m_category|category_id|int(11)|〇|〇|-|
|m_category|name|varchar(20)|-|〇|-|
|m_category|reg_date|date|-|〇|-|

## 商品テーブル

|テーブル名|項目名|型|PK|NN|FK|
|---------|------|--|--|--|--|
|m_items|item_code|int(11)|〇|〇|-|
|m_items|item_name|varchar(50)|-|〇|-|
|m_items|price|int(11)|-|〇|-|
|m_items|category_id|int(11)|-|〇|〇|
|m_items|image|varchar(200)|-|〇|-|
|m_items|detail|varchar(500)|-|-|-|
|m_items|del_flag|int(11)|-|-|-|
|m_items|reg_date|date|-|〇|-|
