---
sidebar_position: 1
title: Authorization
---

# Authorization

**API Key** adalah kredensial rahasia yang digunakan untuk **mengautentikasi sistem Anda** saat mengakses Gate Integration API.

API Key bersifat **unik untuk setiap client**, dan digunakan untuk memastikan bahwa setiap request berasal dari sistem yang terdaftar dan berizin.

## Cara Mendapatkan API Key

1. Hubungi tim support / account manager OneSmile
2. Berikan informasi berikut

    - Nama perusahaan
    - Nama sistem / aplikasi
    - Lokasi gate

3. Setelah proses registrasi selesai, Anda akan menerima:

    - API Key
    - (Opsional) masa berlaku atau scope akses

:::danger[Catatan Keamanan]

Simpan API Key dengan aman dan jangan pernah menaruhnya di client-side (frontend) atau membagikannya ke pihak lain.

:::

## Cara Menggunakan API Key

API Key harus dikirimkan melalui HTTP Header pada setiap request API.

**Contoh Header:**

```
Authorization: Basic [KEY]
```

## Contoh Request (cURL)

```bash
curl -X POST https://our-base-url.com/api/endpoint \
  -H "Authorization: Basic YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{ ... }'

```