# Address API Spec

## Create Address

Endpoint: `POST /api/contacts/:contactId/addresses`

Headers:

- Authorization: token

Request Body:

```json
{
  "street": "Jalan Contoh, optional",
  "city": "Kota, optional",
  "province": "Provinsi, optional",
  "country": "Negara",
  "postal_code": "123456"
}
```

Response Body (Success):

```json
{
  "data": {
    "id": 1,
    "street": "Jalan Contoh, optional",
    "city": "Kota, optional",
    "province": "Provinsi, optional",
    "country": "Negara",
    "postal_code": "123456"
  }
}
```

## Get Address

Endpoint: `GET /api/contacts/:contactId/addresses`

Headers:

- Authorization: token

Response Body (Success):

```json
{
  "data": {
    "id": 1,
    "street": "Jalan Contoh, optional",
    "city": "Kota, optional",
    "province": "Provinsi, optional",
    "country": "Negara",
    "postal_code": "123456"
  }
}
```

## Update Address

Endpoint: `PUT /api/contacts/:contactId/addresses/:addressId`

Headers:

- Authorization: token

Request Body:

```json
{
  "street": "Jalan Contoh, optional",
  "city": "Kota, optional",
  "province": "Provinsi, optional",
  "country": "Negara",
  "postal_code": "123456"
}
```

Response Body (Success):

```json
{
  "data": {
    "id": 1,
    "street": "Jalan Contoh, optional",
    "city": "Kota, optional",
    "province": "Provinsi, optional",
    "country": "Negara",
    "postal_code": "123456"
  }
}
```

## Remove Address

Endpoint: `DELETE /api/contacts/:contactId/addresses/:addressId`

Headers:

- Authorization: token

Response Body (Success):

```json
{
  "data": true
}
```

## List Address

Endpoint: `GET /api/contacts/:contactId/addresses`

Headers:

- Authorization: token

Response Body (Success):

```json
{
  "data": [
    {
      "id": 1,
      "street": "Jalan Contoh, optional",
      "city": "Kota, optional",
      "province": "Provinsi, optional",
      "country": "Negara",
      "postal_code": "123456"
    },
    {
      "id": 2,
      "street": "Jalan Contoh, optional",
      "city": "Kota, optional",
      "province": "Provinsi, optional",
      "country": "Negara",
      "postal_code": "123456"
    }
  ]
}
```
