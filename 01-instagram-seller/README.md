# Instagram Store — ER Diagram

## About

Database design for a small Instagram-based store selling thrifted
and handmade fashion products. The owner needed a proper system to
manage products, track inventory, handle customer orders, and maintain
payment and delivery records.

## Entities

| Entity            | Purpose                                      |
| ----------------- | -------------------------------------------- |
| `customer`        | Stores who placed the order                  |
| `order`           | A purchase made by a customer                |
| `orderItem`       | Each product line inside an order            |
| `product`         | Base info shared by all products             |
| `thriftedProduct` | Unique second-hand item, quantity = 1 always |
| `handmadeProduct` | Custom made item, multiple units possible    |
| `payment`         | Payment status linked to each order          |
| `shipping`        | Delivery tracking linked to each order       |

## Relationships

| Type        | Description                                                                  |
| ----------- | ---------------------------------------------------------------------------- |
| 1 → many    | A customer can place multiple orders                                         |
| 1 → many    | An order can contain multiple orderItems                                     |
| many → many | Orders and products are linked via orderItem (junction table)                |
| 1 → 1       | Each order has one payment record                                            |
| 1 → 1       | Each order has one shipping record                                           |
| 1 → 1       | A product is either a thriftedProduct or handmadeProduct (table inheritance) |

## Diagram

![ER Diagram](./Instagram%20Thrift%20Creator%20Store.png)

---

**Saurabh Ravte**  
GitHub: [github.com/SaurabhRavte](https://github.com/SaurabhRavte)
