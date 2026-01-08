---
sidebar_position: 2
---

# Logical Design

---

## Tabel User
- user_id (PK)
- nama
- email
- password
- role
- created_at

## Tabel Menu
- menu_id (PK)
- nama_menu
- kategori
- harga
- deskripsi
- status

## Tabel Pesanan
- pesanan_id (PK)
- user_id (FK → User.user_id)
- tanggal_pesanan
- total_harga
- status_pesanan

## Tabel Detail_Pesanan
- detail_id (PK)
- pesanan_id (FK → Pesanan.pesanan_id)
- menu_id (FK → Menu.menu_id)
- jumlah
- subtotal

##  Tabel Pembayaran
- pembayaran_id (PK)
- pesanan_id (FK → Pesanan.pesanan_id)
- metode_pembayaran
- status_pembayaran
- tanggal_pembayaran

## Tabel Promo
- promo_id (PK)
- kode_promo
- nama_promo
- deskripsi
- diskon_persen
- tanggal_mulai
- tanggal_selesai
- status

## Tabel Ulasan
- ulasan_id (PK)
- user_id (FK → User.user_id)
- menu_id (FK → Menu.menu_id)
- rating
- komentar
- tanggal_ulasan

## Relasi Antar Tabel
- User 1..* Pesanan
- Pesanan 1..* Detail_Pesanan
- Menu 1..* Detail_Pesanan
- Pesanan 1..1 Pembayaran
- User 1..* Ulasan
- Menu 1..* Ulasan
