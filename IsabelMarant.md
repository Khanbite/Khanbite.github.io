## Isabel Marant ERD

```mermaid
erDiagram
PRODUCT ||--o{ SALE: "is sold in"
PRODUCT ||--|| INVENTORY: "is tracked in"
CUSTOMER ||--o{ SALE: makes
PRODUCT {
    int productid PK "101920448"
    string model "Isabel Marant Bekett"
    float price "735.99"
    string size "7"
}
CUSTOMER {
    string customerid PK "AHWGTZKWGT"
    string name "John Doe"
    string email "jdoe@gmail.com"
}
SALE {
    string id PK "KALSKWIMQOUBSMZN"
    date date "10/18/2024"
    string customerid FK "AHWGTZKWGT"
    int productid FK "101920448"
    int quantity "23456"
}
INVENTORY {
    int productid FK "101920448"
    int stock "Current Stock Available"
}
```

## Documentation
The Isabel Marant sales system works in a straightforward way using four main parts: PRODUCT, CUSTOMER, SALE, and INVENTORY. When a customer buys something, a sale record is created. This record includes details like which product was purchased, how much was bought, and when the sale happened. Each product has a unique ID and is tracked in inventory to keep an eye on stock levels. As sales happen, the inventory is updated to reflect what’s available. 