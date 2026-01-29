---
sidebar_position: 2
title: Gate
---

# Gate ID

**Gate ID** adalah **identitas unik** yang merepresentasikan satu gate fisik (misalnya gate masuk, gate keluar, atau gate area tertentu).

Gate ID digunakan oleh sistem untuk:

- Mengetahui **lokasi gate**
- Menerapkan **aturan akses**
- Melakukan **logging dan audit trail**

## Cara Mendapatkan Gate ID

Gate ID akan diberikan setelah proses setup gate selesai.

1. Setiap gate fisik didaftarkan ke sistem
2. Setiap gate akan memiliki:

    - `gate_id`
    - Nama gate
    - Tipe gate (IN / OUT)
    - Lokasi (opsional)

Contoh:

```
gate_id: 123
```

## Cara Menggunakan Gate ID

Gate ID dikirimkan sebagai bagian dari **request body** atau **query parameter**, tergantung endpoint.

