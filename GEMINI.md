# 🤖 GEMINI / VIBE CODING RULES

File ini berisi instruksi khusus untuk asisten AI (Cursor/Windsurf/Gemini) yang membantu penulisan kode dalam *repository* ini.

## Aturan Penulisan Kode:
1. **Tech Stack Utama:** Next.js App Router (`/app`), TypeScript, Tailwind CSS.
2. **Strict TypeScript:** Gunakan *interface* atau *type* untuk semua *payload* database, props komponen, dan respons Web Worker.
3. **Web Worker Isolation:** Jangan pernah memanggil modul `transformers.js` atau WebGPU di dalam *main thread* UI komponen React. Selalu letakkan logika AI di `/workers` dan gunakan mekanisme pengiriman pesan (`postMessage`).
4. **Offline First:** Dahulukan operasi baca/tulis ke IndexedDB. Sinkronisasi jaringan (jika ada) dilakukan secara asinkron di latar belakang.
5. **UI/UX:** Desain komponen harus *mobile-first* karena sering diakses melalui tablet kasir. Gunakan indikator *loading* yang jelas untuk proses AI.
6. **Konteks Data:** Saat membuat *mock data* atau skema awal, gunakan konteks bahan baku relevan (Kulit lumpia, Daging Sapi, Jagung, Keju) dan produk akhir (Lumpia Beef, Jasuke).
