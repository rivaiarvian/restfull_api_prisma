# Address API Spec

## Create Address API

Endpoint : POST /api/contacts/:contactId/addresses/:addressId

Headers :
- Authorization : token

Request Body:

```json
{
    "street" : "Jalan O",
    "city" : "Jakarta Selatan",
    "province" : "DKI Jakarta",
    "Country" : "Indonesia",
    "code_post" : "12640"
}
```
Response Body Success:

```json
{
    "data": 
        {
            "id": 1 ,
            "street" : "Jalan O",
            "city" : "Jakarta Selatan",
            "province" : "DKI Jakarta",
            "country" : "Indonesia",
            "code_post" : "12640"
        }
}

```
Response Body Error:
```json
{
    "errors" : "Country is required"
}
```
## Update Address API

Endpoint : PUT /api/contacts/:contactId/addresses/:addressId

Headers :
- Authorization : token

Request Body:

```json
{
    "street" : "Jalan O",
    "city" : "Jakarta Selatan",
    "province" : "DKI Jakarta",
    "country" : "Indonesia",
    "code_post" : "12640"
}
```
Response Body Success:

```json
{
    "data": 
        {
            "id": 1 ,
            "street" : "Jalan O",
            "city" : "Jakarta Selatan",
            "province" : "DKI Jakarta",
            "country" : "Indonesia",
            "code_post" : "12640"
        }
}

```
Response Body Error:
```json
{
    "errors" : "Country is required"
}
```
## Get Address API

Endpoint : GET /api/contacts/:contactId/addresses/:addressId

Headers :
- Authorization : token

Response Body Success:

```json
{
    "data": 
        {
            "id": 1 ,
            "street" : "Jalan O",
            "city" : "Jakarta Selatan",
            "province" : "DKI Jakarta",
            "country" : "Indonesia",
            "code_post" : "12640"
        }
}
```
Response Body Error:
```json
{
    "errors" : "contact is not found"
}
```
## List Address API

Endpoint : GET /api/contacts/:contactId/address

Headers :
- Authorization : token

Response Body Success:

```json
{
    "data": [
        {
            "id": 1 ,
            "street" : "Jalan O",
            "city" : "Jakarta Selatan",
            "province" : "DKI Jakarta",
            "country" : "Indonesia",
            "code_post" : "12640"
        },
        {
            "id": 2 ,
            "street" : "Lenteng Agung",
            "city" : "Jakarta Selatan",
            "province" : "DKI Jakarta",
            "country" : "Indonesia",
            "code_post" : "12640"
        },
    ]
}
```
Response Body Error:
```json
{
    "errors" : "contact is not found"
}
```
## Remove Address API

Endpoint : DELETE /api/contacts/:contactId/address

Headers :
- Authorization : token

Response Body Success:

```json
{
    "data": "OK"
}
```
Response Body Error:
```json
{
    "errors" : "contact is not found"
}
```