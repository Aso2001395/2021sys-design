```startuml
@startuml tables

!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue

skinparam class {
    BackgroundColor Snow
    BorderColor Black
    ArrowColor Black
}

entity "顧客マスタ" as customer {
        + customer_code [PK]
        --
        pass
        name
        address
        tel
        mail
        del_flag
        reg_date
}

entity "購入テーブル" as order {
        + order_id [PK]
        --
        customer_code [FK]
        purchase_date
        total_price
}

entity "購入詳細テーブル" as order_datail {
        + order_id [PK]
        + detail_id [PK]
        --
        item_id [FK]
        price
        num
}

entity "商品マスタ" as item {
        + item_code [PK]
        --
        item_name
        price
        category_id [FK]
        image
        detail
        del_flag
        reg_date
}

entity "カテゴリマスタ" as category {
        + category_id [PK]
        --
        name
        reg_date
}
@enduml
```
