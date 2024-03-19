# User API Spec

## Register User

Endpoint: `POST /api/users`

Request Body:

```json
{
  "username": "ekoteguh",
  "password": "rahasi4",
  "name": "Eko Teguh Widodo"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "ekoteguh",
    "name": "Eko Teguh Widodo"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "Username is already registered"
}
```

## Login User

Endpoint: `POST /api/users/login`

Request Body:

```json
{
  "username": "ekoteguh",
  "password": "rahasi4"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "ekoteguh",
    "name": "Eko Teguh Widodo",
    "token": "session_id_generated"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "Username or password is wrong"
}
```

## Get User

Endpoint: `GET /api/users/current`

Headers:

- Authorization: token

Response Body (Success):

```json
{
  "data": {
    "username": "ekoteguh",
    "name": "Eko Teguh Widodo"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "Unauthorization"
}
```

## Update User

Endpoint: `PATCH /api/users/current`

Headers:

- Authorization: token

Request Body:

```json
{
  "password": "rahasi4", // optional, if you want to change password
  "name": "Eko Teguh Widodo" // optional, if you want to change password
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "ekoteguh",
    "name": "Eko Teguh Widodo"
  }
}
```

## Logout User

Endpoint: `DELETE /api/users/current`

Headers:

- Authorization: token

Response Body (Success):

```json
{
  "data": true
}
```
