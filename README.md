# Status Response
```text
OK | BAD_REQUEST | NOT FOUND | UNAUTHORIZED | EXPIRED
```
---
## **POST Login**
```javascript
{
  method: 'POST',
  body: {
    username: STRING,
    password: STRING
  },
  response: {
    status_string: 'OK',
    message: STRING,
    data: {
      user: {
        username: STRING,
        name: STRING,
        nik: STRING,
        email: STRING,
        phone_number: STRING,
        alamat: STRING,
        jenis_kelamin: STRING
      },
      token_key: STRING
    }
  }
}
```
---
## **POST Submit Laporan**
```javascript
{
  method: 'POST',
  header: {
    'Token-Key': STRING
  },
  body: {
    topik_laporan: STRING,
    tanggal_kejadian: STRING,
    jam_kejadian: STRING,
    keterangan: STRING,
    nama_terlapor: STRING,
    nip: STRING,
    jabatan: STRING,
    unit_kerja: STRING,
    lampiran: JSON_STRINGIFY_ARRAY,
    is_anonym: BOOLEAN
  },
  response: {
    status_string: 'OK',
    message: STRING
  }
}
```
---
## **GET Daftar Laporan**
```javascript
{
  method: 'GET',
  header: {
    'Token-Key': STRING
  },
  params: {
    page: STRING,
    limit: STRING
  },
  response: {
    status_string: 'OK',
    message: STRING,
    data: [
      {
        pelaporan_id: STRING,
        topik_laporan: STRING,
        tanggal_kejadian: STRING,
        jam_kejadian: STRING,
        keterangan: STRING,
        nama_terlapor: STRING,
        nip: STRING,
        jabatan: STRING,
        unit_kerja: STRING,
        lampiran: ARRAY_URL_ATTACHMENT,
        is_anonym: BOOLEAN,
        status: STRING
      }
    ]
  }
}
```
---
## **GET Detail Laporan**
```javascript
{
  method: 'GET',
  header: {
    'Token-Key': STRING
  },
  params: {
    pelaporan_id: STRING
  },
  response: {
    status_string: 'OK',
    message: STRING,
    data: {
      pelaporan_id: STRING,
      topik_laporan: STRING,
      tanggal_kejadian: STRING,
      jam_kejadian: STRING,
      keterangan: STRING,
      nama_terlapor: STRING,
      nip: STRING,
      jabatan: STRING,
      unit_kerja: STRING,
      lampiran: ARRAY_URL_ATTACHMENT,
      is_anonym: BOOLEAN,
      status: STRING
    }
  }
}
```
---
## **POST Register**
```javascript
{
  method: 'POST',
  header: {
    'Token-Key': STRING
  },
  body: {
    nik: STRING,
    username: STRING,
    password: STRING,
    email: STRING,
    phone_number: STRING,
    alamat: STRING,
    jenis_kelamin: STRING
  },
  response: {
    status_string: 'OK',
    message: STRING
  }
}
```
