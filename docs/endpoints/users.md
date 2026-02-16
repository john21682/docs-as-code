# Users API

## Create a User

**POST** `/users`

### Request Body
```json
{
  "name": "John Doe",
  "email": "john.doe@example.com"
}
```

### Response (201 Created)
```json
{
  "id": "usr_12345",
  "name": "John Doe",
  "email": "john.doe@example.com",
  "created_at": "2025-01-10T10:15:00Z"
}
```

## Get User by ID

**GET** `/users/{id}`

### Response (200 OK)
```json
{
  "id": "usr_12345",
  "name": "John Doe",
  "email": "john.doe@example.com"
}
```
