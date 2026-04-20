---
sidebar_position: 4
title: Face Storing
description: ""
---

# Store Dummy Face

:::tip[Penyusun]

- Reza Nurfachmi :: Fullstack Developer Senior Associate - Operational Technology

:::

Endpoint ini digunakan untuk menyimpan data wajah untuk User OneSmile dengan nomor handphone 0812*****009 dan hanya akan berlaku saat development Gate.

## Headers

| key | value       | description            |
|-----|-------------|------------------------|

## Endpoint

| method | endpoint |
|--------|----------|
| POST   | `store-face`  |

## Multipart Form Body Request

| key         | required | type       | description         |
|-------------|----------|------------|---------------------|
| image_path     | YES      | Image File | Gambar wajah depan. |

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
  "data": {
    "member_id": 123,
    "member_username": "62812*****009",
    "image_path": "https://onesmilestorageprod.blob.core.windows.net/onesmile/img/faces/62812*****009/1213112314_1776640754.png"
  }
}
```

**Status code: 400**

```json
{
  "success": false,
  "msg": "image_path (file) wajib diupload",
  "data": []
}
```