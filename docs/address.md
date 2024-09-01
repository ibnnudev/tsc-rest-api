# Address API Spec

# Create Address

Endpoint: POST /api/contacts/:idContact/addresses

Request Header:

- X-API-TOKEN: token

Request Body:

```json
{
  "street": "Jl Sudirman",
  "city": "Malang",
  "province": "Jawa Timur",
  "country": "Indonesia",
  "postal_code": "67272"
}
```

Response Body (Success):

```json
{
  "data": {
    "id": 1,
    "street": "Jl Sudirman",
    "city": "Malang",
    "province": "Jawa Timur",
    "country": "Indonesia",
    "postal_code": "67272"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "Postal code is required, ..."
}
```

# Get Address

Endpoint: GET /api/contacts/:idContact/idAddress

Request Header:

- X-API-TOKEN: token

Response Body (Success):

```json
{
  "data": {
    "id": 1,
    "street": "Jl Sudirman",
    "city": "Malang",
    "province": "Jawa Timur",
    "country": "Indonesia",
    "postal_code": "67272"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "Address is not found, ..."
}
```

# Update Address

Endpoint: PUT /api/contacts/:idContact/:idAddress

Request Header:

- X-API-TOKEN: token

Request Body:

```json
{
  "street": "Jl Sudirman",
  "city": "Malang",
  "province": "Jawa Timur",
  "country": "Indonesia",
  "postal_code": "67272"
}
```

Response Body (Success):

```json
{
  "data": {
    "id": 1,
    "street": "Jl Sudirman",
    "city": "Malang",
    "province": "Jawa Timur",
    "country": "Indonesia",
    "postal_code": "67272"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "Postal code is required, ..."
}
```

# Remove Address

Endpoint: DELETE /api/contacts/:idContact/:idAddress

Request Header:

- X-API-TOKEN: token

Response Body (Success):

```json
{
  "data": "OK"
}
```

Response Body (Failed):

```json
{
  "errors": "Address is not found, ..."
}
```

# List Address

Endpoint: GET /api/contacts/:idContact/addresses

Request Header:

- X-API-TOKEN: token

Response Body (Success):

```json
{
  "data": [
    {
      "id": 1,
      "street": "Jl Sudirman",
      "city": "Malang",
      "province": "Jawa Timur",
      "country": "Indonesia",
      "postal_code": "67272"
    },
    {
      "id": 2,
      "street": "Jl Sudirman",
      "city": "Malang",
      "province": "Jawa Timur",
      "country": "Indonesia",
      "postal_code": "67272"
    }
  ]
}
```

Response Body (Failed):

```json
{
  "errors": "Contact is not found"
}
```
