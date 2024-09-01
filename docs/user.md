# User API Spec

## Register User

Enpoint: POST /api/users

Request Body:

```json
{
  "username": "ibnu",
  "password": "rahasia"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "ibnu",
    "name": "Ibnu Abs"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "Username must not blank, ..."
}
```

## Login User

Enpoint: POST /api/users/login

Request Body:

```json
{
  "username": "ibnu",
  "password": "rahasia"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "ibnu",
    "name": "Ibnu Abs",
    "token": "uuid"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "Username or password wrong!"
}
```

## Get User

Enpoint: GET /api/users/current

Request Header:

- X-API-TOKEN: token

Response Body (Success):

```json
{
  "data": {
    "username": "ibnu",
    "name": "Ibnu Abs",
    "token": "uuid"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "Unautorized!"
}
```

## Update User

Enpoint: PATCH /api/users/login

Request Header:

- X-API-TOKEN: token

Request Body:

```json
{
  "name": "ibnu", // tidak wajib
  "password": "rahasia" // tidak wajib
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "ibnu",
    "name": "Ibnu Abs"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "Unautorized!"
}
```

## Logout User

Enpoint: DELETE /api/users/current

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
  "errors": "Unautorized!"
}
```
