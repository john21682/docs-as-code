# Authentication

The API uses API key authentication.

## Request Header

```
Authorization: Bearer YOUR_API_KEY
```

## Example

```bash
curl -X GET https://api.samplecompany.com/v1/users \
  -H "Authorization: Bearer YOUR_API_KEY"
```

Keep API keys confidential.
