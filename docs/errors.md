# Errors

The API uses standard HTTP status codes.

| Code | Meaning |
|----|----|
| 400 | Bad Request |
| 401 | Unauthorized |
| 404 | Not Found |
| 500 | Server Error |

## Error Response Format

```json
{
  "error": {
    "code": "INVALID_REQUEST",
    "message": "Missing required field"
  }
}