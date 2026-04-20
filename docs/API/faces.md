---
sidebar_position: 3
title: Faces
description: ""
---

# Faces

:::tip[Penyusun]

- Reza Nurfachmi :: Fullstack Developer Senior Associate - Operational Technology

:::

Endpoint ini digunakan untuk Gate dapat mengambil data wajah.

## Headers

| key           | value       | description            |
|---------------|-------------|------------------------|
| Authorization | Basic [KEY] | KEY in base64 encoding |

## Endpoint

| method | endpoint |
|--------|----------|
| GET    | `faces`  |

## JSON Body Request

| key         | required | type    | description                                           |
|-------------|----------|---------|-------------------------------------------------------|
| gate_id     | YES      | Integer | Gate ID from OneSmile. Tiap Gate mendapatkan ID unik. |

## Responses

| key      | type         |
|----------|--------------|
| success  | Boolean      |
| msg      | String       |
| data     | Object Array |

### Success Response

**Status code: 200**

```json
{
  "success": true,
  "msg": "success",
  "data": [
    {
      "member_id": 108996,
      "image_path": "https://onesmilestorageprod.blob.core.windows.net/onesmile/img/faces/6285694859455/108996_1776640754.png",
      "created_at": "2026-04-20 06:19:16"
    }
  ]
}
```

### Failure Response

**Status code: 403**

```json
{
  "success": false,
  "msg": "Unauthorized",
  "data": []
}
```