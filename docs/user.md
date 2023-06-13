# User API Spec

## Register User API

Endpoin : POST /api/users

Request Body :

```json
{
    "username": "rivaiarvian",
    "password": "bismillah",
    "name": "Rivai Arvian"
}
```

Response Body Success:
```json
{
    "data" : {
        "username": "rivaiarvian",
        "name" : "Rivai Arvian"
    }
}
```

Response Body Error:
```json
{
    "errors" : "Username already registered"
}
```

## Login User API

Endpoin : POST /api/users/login

Request Body :

```json
{
    "username": "rivaiarvian",
    "password": "bismillah",
}
```

Response Body Success:
```json
{
    "data" : {
        "token": "unique-token"
    }
}
```

Response Body Error:
```json
{
    "errors" : "Username or Password wrong"
}
```

## Update User API

Endpoin : PATCH /api/users/current

Headers:
- Authorization : token

Request Body :

```json
{
    "name": "RIVAI ARVIAN", //optional
    "password": "bismillah NEW", //optional
}
```

Response Body Success:
```json
{
    "data" : {
        "username": "rivaiarvian",
        "name" : "RIVAI ARVIAN"
    }
}
```

Response Body Error:
```json
{
    "errors" : "Name length max 100"
}
```

## Get User API

Endpoin : GET /api/users/current

Headers:
- Authorization : token


Response Body Success:
```json
{
    "data" : {
        "username": "rivaiarvian",
        "name" : "RIVAI ARVIAN"
    }
}
```

Response Body Error:
```json
{
    "errors" : "Unauthorized"
}
```

## Logout User API

Endpoin : DELETE /api/users/logout

Headers:
- Authorization : token

Response Body Success:
```json
{
    "data" : "OK"
}
```

Response Body Error:
```json
{
    "errors" : "Unauthorized"
}
```
