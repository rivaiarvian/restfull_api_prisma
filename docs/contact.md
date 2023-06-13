# Contact API Spec

## Create Contact API

Endpoint: POST /api/contact

Headers:
- Authorization : token

Requst Body:
```json
{
    "first_name" : "Rivai",
    "last_name" : "Arvian",
    "email" : "rivai.arviannn@gmail.com",
    "phone" : "081212883804",
}
```
Response Body Success:

```json
{
    "id" : 1,
    "first_name" : "Rivai",
    "last_name" : "Arvian",
    "email" : "rivai.arviannn@gmail.com",
    "phone" : "081212883804",
}
```
Response Body Error:

```json
{
    "errors" : "email is not valid format"
}
```
## Update Contact API

Endpoint: PUT /api/contact

Headers:
- Authorization : token

Requst Body:
```json
{
    "first_name" : "Rivai",
    "last_name" : "Arvian",
    "email" : "rivai.arviannn@gmail.com",
    "phone" : "081212883804",
}
```
Response Body Success:

```json
{
    "id" : 1,
    "first_name" : "Rivai",
    "last_name" : "Arvian",
    "email" : "rivai.arviannn@gmail.com",
    "phone" : "081212883804",
}
```
Response Body Error:

```json
{
    "errors" : "email is not valid format"
}
```

## Get Contact API

Endpoint: GET /api/contact

Headers:
- Authorization : token

Response Body Success:

```json
{
    "data" : {
        "id" : 1,
        "first_name" : "Rivai",
        "last_name" : "Arvian",
        "email" : "rivai.arviannn@gmail.com",
        "phone" : "081212883804",
    } 
}
```
Response Body Error:

```json
{
    "errors" : "contact is not found"
}
```

## Search Contact API

Endpoint: GET /api/contact

Headers:
- Authorization : token

Query params:
- name : Search by first_name or last_name, using like, optional
- email : Search by email, using like, optional
- phone : Search by phone, using like, optional
- page : number of page, default 1
- size : size per page, default 10

Response Body Success:

```json
{
    "data" : [ 
        {
            "id" : 1,
            "first_name" : "Rivai",
            "last_name" : "Arvian",
            "email" : "rivai.arviannn@gmail.com",
            "phone" : "081212883804",
        },
        {
            "id" : 2,
            "first_name" : "Wira",
            "last_name" : "Utami",
            "email" : "wirautami.p@gmail.com",
            "phone" : "081212883805",
        },
    ],
    "paging" : {
        "page": 1,
        "total_page" : 3,
        "total_item" : 30
    }
}
```
Response Body Error:

```json
{
    "errors" : "contact is not found"
}
```

## Remove Contact API

Endpoint: DELETE /api/contact

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
    "errors" : "contact is not found"
}
