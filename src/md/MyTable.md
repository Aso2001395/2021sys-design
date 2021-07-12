```startuml
@startuml

!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue

skinparam class {
    BackgroundColor Snow
    BorderColor Black
    ArrowColor Black
}

package "ECサイト" as target_system {

entity "顧客マスタ" as customer <m_customers> <<M,MASTER_MARK_COLOR>> {
        + customer_code [PK]
        --
        name
        mail
        tell
        address
        card_code
        pass
        del_flag
        reg_date
}

entity "購入テーブル" as order <d_purchase> <<T,TRANSACTION_MARK_COLOR>>{
        + order_id [PK]
        --
        customer_code
        item_code
        purchase_date
        price
}

entity "商品マスタ" as item <m_items> <<M,MASTER_MARK_COLOR>> {
        + item_code [PK]
        --
        item_name
        price
        image
        detail
        del_flag
        reg_date
}

customer |-|{ order
order }|- item

@enduml
```
