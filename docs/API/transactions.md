---
sidebar_position: 2
title: Transactions
description: ""
---

# Transactions

## Headers

| key           | value       |
|---------------|-------------|
| Authorization | Basic [KEY] |

## Endpoint

| method | endpoint       |
|--------|----------------|
| POST   | `scan-qr-gate` |

## Body Request

| key         | required | type    | description               |
|-------------|----------|---------|---------------------------|
| token       | YES      | String  | QR or FR string           |
| access      | YES      | String  | options: `qrcode`, `face` |
| gate_id     | YES      | Integer | Gate ID from OneSmile     |
| gate        | YES      | String  | Gate method               |
| waktuqr     | YES      | Integer | Timestamp                 |
| waktubeacon | YES      | Integer | Timestamp                 |

## Request Example

```json
{
   "token": "8888888876c4497eb1388557364a5281",
   "access": "qrcode",
   "gate_id": 11,
   "gate": "IN",
   "waktuqr": 0,
   "waktubeacon": 0
}
```

## Responses

| key      | type    |
|----------|---------|
| success  | Boolean |
| msg      | String  |
| data     | Object  |
| data.msg | String  |

### Success Response

**Status code: 200**

```json
{
  "success": true,
  "msg": "Muhlis Habib Pradana, Terima Kasih",
  "data": {}
}
```

### Failure Response

**Status code: 200**

```json
{
  "success": false,
  "msg": "QR tidak valid",
  "data": {
    "msg": "QR tidak valid"
  }
}
```

**Status code: 500**

```json
{
  "success": false,
  "msg": "QR tidak valid"
}
```

