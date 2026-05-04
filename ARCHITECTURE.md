# 🏗️ Arsitektur Sistem

## Pemisahan Thread (UI vs AI)
Untuk memastikan POS tetap responsif, kita menggunakan pola pendelegasian proses yang intensif (*heavy lifting*):

1. **Main Thread (Next.js UI):** Menangani *render* DOM, input *keyboard/touch*, manajemen *state* (React), dan komunikasi dengan IndexedDB untuk mencatat transaksi.
2. **Background Thread (Web Worker):** Eksklusif memuat *engine* Hugging Face. Saat diinisialisasi, worker akan meminta *browser* mengaktifkan akselerasi WebGPU.

## Alur Data Modul AI Insight:
`UI Kasir` -> *fetch data IndexedDB* -> `JSON Payload` -> `postMessage()` -> `Web Worker` -> *Format JSON ke Prompt Teks* -> `WebGPU Inference` -> *Teks Hasil* -> `postMessage()` -> `UI Kasir menampilkan Insight`.
