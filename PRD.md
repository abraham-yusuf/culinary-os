# 📋 Product Requirements Document (PRD)

## 1. Visi Produk
Memberdayakan pedagang makanan ringan skala mikro untuk memiliki standar manajemen operasional layaknya *franchise* besar, dengan bantuan AI yang berjalan secara efisien dan gratis di perangkat kasir/laptop mereka sendiri.

## 2. Target Pengguna & Kasus Penggunaan (Use Case)
Fokus awal aplikasi ini adalah untuk operasional kedai/gerobak makanan dengan mobilitas bahan tinggi, seperti penjualan **Lumpia Beef** dan **Jasuke**. 
- Pengguna membutuhkan input transaksi yang sangat cepat (hitungan detik).
- Pengguna perlu tahu margin keuntungan bersih per hari tanpa menghitung manual sisa bahan.
- Pengguna butuh ide promosi saat bahan baku tertentu menumpuk (misal: stok jagung manis masih banyak menjelang akhir pekan).

## 3. Scope Fitur MVP (Minimum Viable Product)
- [ ] **Modul Inventaris:** CRUD bahan baku, harga beli terkini, dan resep/komposisi (Product-Ingredient mapping).
- [ ] **Modul Kasir (POS):** Input pesanan cepat.
- [ ] **Modul HPP:** Kalkulator otomatis laba bersih berbasis pergerakan harga beli bahan terakhir.
- [ ] **Modul AI (The "Vibe" Feature):** Tombol *Generate Insight* yang membaca status tabel inventaris dan penjualan untuk menghasilkan saran bisnis.

## 4. Non-Functional Requirements
- **Performa AI:** Inference LLM harus berjalan di *background thread* (Web Worker) dan tidak memblokir UI kasir.
- **Resource Limits:** Menggunakan model terkuantisasi (4-bit/q4) agar bisa berjalan di RAM 4GB-8GB.
