# Authentication

The API uses API key authentication.

## Sending the API Key

Include the API key in the request header:
## Example Request

```bash
curl -X GET https://api.samplecompany.com/v1/users \
  -H "Authorization: Bearer YOUR_API_KEY"