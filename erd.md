```uml
@startuml erd

!include tables.md

customer ||-o{ order
order ||-o{ order_detail
order_detail ||-o| item
item ||-o{ category

@enduml
```
