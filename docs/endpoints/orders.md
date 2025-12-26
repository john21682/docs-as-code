# Orders API

## Create an Order

**POST** `/orders`

### Request Body
```json
{
  "user_id": "usr_12345",
  "amount": 2500,
  "currency": "INR"
}
### Response (201 Created)
```json
{
  "order_id": "ord_98765",
  "status": "created",
  "amount": 2500,
  "currency": "INR"
}
**Response Fields**

| Field | Description |
|------|------------|
| order_id | Unique identifier for the order |
| status | Current order status |
| amount | Order amount |
| currency | Currency code |