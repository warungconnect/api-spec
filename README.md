# api-spec

## Get User

Request :

- Method : GET
- Endpoint : `/api/users`
- Header :
  - Accept: application/json

Response :

```json
{
  "code": 200,
  "status": "Success",
  "message": "Data User berhasil ditemukan.",
  "data": [
    {
      "uuid": "string",
      "nama": "string",
      "email": "string",
      "role": "string",
      "createdAt": "date",
      "updatedAt": "date"
    }
  ]
}
```

## Create User

Request :

- Method : POST
- Endpoint : `/api/users`
- Header :
  - Content-Type: application/json
  - Accept: application/json
- Body :

```json
{
  "nama": "string",
  "email": "string",
  "password": "string",
  "konfirmPassword": "string",
  "role": "string"
}
```

Response :

```json
{
  "status": 201,
  "message": "Data user berhasil dibuat",
  "data": [
    {
      "nama": "string",
      "email": "string",
      "role": "string"
    }
  ]
}
```

## Get User by uuid

Request :

- Method : GET
- Endpoint : `/api/users/{uuid}`
- Header :
  - Accept: application/json

Response :

```json
{
  "code": 200,
  "status": "Success",
  "message": "Data User: {uuid} berhasil ditemukan.",
  "data": {
    "uuid": "string",
    "nama": "string",
    "email": "string",
    "role": "string",
    "createdAt": "date",
    "updatedAt": "date"
  }
}
```

## Update User

Request :

- Method : PATCH
- Endpoint : `/api/users/{uuid}`
- Header :
  - Content-Type: application/json
  - Accept: application/json
- Body :

```json
{
  "nama": "string",
  "email": "string",
  "password": "string",
  "konfirmPassword": "string",
  "role": "string"
}
```

Response :

```json
{
  "code": 200,
  "status": "Success",
  "message": "Update data berhasil",
  "data": [
    {
      "nama": "string",
      "email": "string",
      "role": "string",
      "createdAt": "date",
      "updatedAt": "date"
    }
  ]
}
```

## Delete User

Request :

- Method : DELETE
- Endpoint : `/api/users/{uuid}`
- Header :
  - Accept: application/json

Response :

```json
{
  "code": 200,
  "status": "Success",
  "message": "Hapus data berhasil"
}
```

## Login

Request :

- Method : POST
- Endpoint : `/api/login`
- Header :
  - Content-Type: application/json
  - Accept: application/json
- Body :

```json
{
  "email": "string",
  "password": "string"
}
```

Response :

```json
{
  "code": 200,
  "status": "Success",
  "message": "Login berhasil",
  "data": [
    {
      "nama": "string",
      "email": "string",
      "role": "string"
    }
  ]
}
```

## Logout

Request :

- Method : DELETE
- Endpoint : `/api/logout`
- Header :
  - Accept: application/json

Response :

```json
{
  "code": 200,
  "status": "Success",
  "message": "Anda telah logout"
}
```
