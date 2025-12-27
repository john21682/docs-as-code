# Payments API

## Create a Payment

**POST** `/payments`

### Description
Creates a payment for an existing order. Payments are processed asynchronously and return a payment status.

---

### Request Body
```json
{
  "order_id": "ord_98765",
  "payment_method": "card",
  "amount": 2500,
  "currency": "INR"
}
```
Request Fields
Field	Type	Required	Description
order_id	string	Yes	Identifier of the order being paid
payment_method	string	Yes	Payment method (e.g., card, upi, netbanking)
amount	number	Yes	Payment amount
currency	string	Yes	ISO currency code

Response (201 Created)
```json
{
  "payment_id": "pay_45678",
  "order_id": "ord_98765",
  "status": "processing",
  "amount": 2500,
  "currency": "INR"
}
```

Response Fields
Field	Description
payment_id	Unique identifier for the payment
order_id	Associated order identifier
status	Current payment status
amount	Amount processed
currency	Currency code

Get Payment Status

GET /payments/{payment_id}

Response (200 OK)
```json
{
  "payment_id": "pay_45678",
  "order_id": "ord_98765",
  "status": "successful",
  "processed_at": "2025-01-15T10:30:00Z"
}
```

Payment Status Values
Status	Meaning
processing	Payment is being processed
successful	Payment completed successfully
failed	Payment failed
refunded	Payment was refunded

Error Responses

Example Error Response
```json
{
  "error": {
    "code": "PAYMENT_FAILED",
    "message": "Insufficient funds"
  }
}
```