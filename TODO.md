# ✅ Task Tracker

## Phase 1: Foundation & Database
- [ ] Inisialisasi Next.js dengan Tailwind & TypeScript.
- [ ] Setup arsitektur folder (components, lib, workers).
- [ ] Konfigurasi IndexedDB (bisa menggunakan *wrapper* lokal seperti `idb` atau `dexie`).
- [ ] Buat skema tabel lokal: `ingredients`, `products`, `product_ingredients`, `sales`.

## Phase 2: Core POS & HPP
- [ ] Buat UI halaman Kasir.
- [ ] Buat fungsi utilitas kalkulator HPP otomatis berdasarkan komposisi resep.
- [ ] Implementasi *mock data* awal (Lumpia Beef & Jasuke).

## Phase 3: The "Vibe" AI Integration
- [ ] Install `@xenova/transformers`.
- [ ] Setup `next.config.mjs` untuk mendukung WebAssembly dan arsitektur *worker*.
- [ ] Buat `ai.worker.ts` dengan pola Singleton dan inisialisasi WebGPU `dtype: q4`.
- [ ] Buat komponen React untuk menjembatani komunikasi UI ke Worker.

## Phase 4: Polish & Deployment
- [ ] Setup Dockerfile untuk kontainerisasi aplikasi web.
- [ ] Uji coba eksekusi *offline*.
- [ ] Perekaman video *showcase* untuk submisi #JuaraVibeCoding.
