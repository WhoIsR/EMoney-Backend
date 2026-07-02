# Kashi E-Money Backend

Backend API untuk aplikasi Kashi E money pada tugas UAS Aplikasi Mobile Lanjutan.

## Fitur

- Verifikasi Firebase token.
- Registrasi dan data user wallet.
- Data saldo dan riwayat transaksi.
- Top up dan transfer.
- OTP email, OTP Firebase, dan TOTP.

## Menjalankan Backend

```bash
go mod download
go run .
```

Salin `.env.example` menjadi `.env`, lalu isi konfigurasi database, Redis,
Firebase, SMTP, dan JWT sesuai environment lokal.

## Endpoint Utama

```text
GET  /v1/health
POST /v1/auth/verify-token
POST /v1/auth/register
GET  /v1/auth/me
GET  /v1/account
GET  /v1/account/transactions
POST /v1/payment/topup
POST /v1/payment/transfer
POST /v1/otp/send-email
POST /v1/otp/send-firebase
POST /v1/otp/confirm
POST /v1/otp/totp/register
POST /v1/otp/totp/verify
```

## Catatan Secret

File `.env` dan `firebase_service_account.json` tidak ikut repo karena berisi
credential lokal.
