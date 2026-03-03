# SS Hasil Code
| Fitur           | Deskripsi                                                                                                                                               | Screenshot                                                                                               |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| **Tambah Data** | Menambahkan user baru melalui form (nama dan umur), kemudian klik **Simpan Data**. Data akan tersimpan dengan ID otomatis dan langsung tampil di tabel. | <img src="https://github.com/user-attachments/assets/de88a7f4-cbd3-499c-b71d-b64d58020549" width="600"/> |
| **Update User** | Mengedit data user **Friska**, mengubah umur dari 21 menjadi 20, lalu klik **Update User**. Perubahan langsung ter-update di tabel.                     | <img src="https://github.com/user-attachments/assets/8725e8c3-2ca0-4035-972b-498f760c7544" width="600"/> |
| **Hapus User**  | Menghapus user **Friska** dengan menekan tombol **Hapus** dan melakukan konfirmasi. Data akan terhapus dari tabel.                                      | <img src="https://github.com/user-attachments/assets/eca287ba-291e-4980-8898-782401808f47" width="600"/> |

# Dokumentasi API: Manajemen User
Dokumentasi ini menjelaskan endpoint yang tersedia untuk mengelola data pengguna (user). Semua request dan response menggunakan format JSON.

## Base URL
http://localhost:8080 (Default Spring Boot)

## Tambah User Endpoint: POST /api/users

Request Body:
```json
{
  "name": "String",
  "age": "Integer"
}
```
Respon Body (201 Created):
```json
{
  "status": "success",
  "data": {
    "id": "uuid-string",
    "name": "String",
    "age": 0
  }
}
```
## Ambil Semua User Endpoint: GET /api/users

Respon Sukses (201 Created):
```json
{
  "status": "success",
  "data": {
    "id": "uuid-string",
    "name": "String",
    "age": 0
  }
}
```

Response Sukses (200 OK):
```json
{
  "status": "success",
  "data": [
    {
      "id": "uuid-string",
      "name": "String",
      "age": 0
    }
  ]
}
```
## Ambil User Berdasarkan ID Endpoint: GET /api/users/{id}
Response Sukses (200 OK):

```json
{
  "status": "success",
  "data": {
    "id": "uuid-string",
    "name": "String",
    "age": 0
  }
}
```
## Update User Endpoint: PUT /api/users/{id}
Request Body:
```json
{
  "name": "String Updated",
  "age": 25
}
```
Respon Sukses (200 OK):
```json
{
  "status": "success",
  "data": {
    "id": "uuid-string",
    "name": "String Updated",
    "age": 25
  }
}
```
## Hapus User Endpoint: DELETE /api/users/{id}

Respon Sukses (200 OK):
```json
{
  "status": "success delete user with id {id}"
}
```
