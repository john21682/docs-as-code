# Payments API

## Create a Payment

**POST** `/payments`

### Description
Creates a payment for an existing order.

### Request Body
```json
{
  "order_id": "ord_98765",
  "payment_method": "card",
  "amount": 2500,
  "currency": "INR"
}
```

### Response (201 Created)
```json
{
  "payment_id": "pay_45678",
  "order_id": "ord_98765",
  "status": "processing",
  "amount": 2500,
  "currency": "INR"
}
```

## Get Payment Status

**GET** `/payments/{payment_id}`

### Response (200 OK)
```json
{
  "payment_id": "pay_45678",
  "order_id": "ord_98765",
  "status": "successful",
  "processed_at": "2025-01-15T10:30:00Z"
}
```
