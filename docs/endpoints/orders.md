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

{
  "order_id": "ord_98765",
  "status": "created"
}