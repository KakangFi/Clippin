# ClipAI Studio

Prototype responsif untuk HP Android.

## Fitur yang tersedia
- Pilih dan preview video dari perangkat.
- Atur titik mulai dan durasi klip, lalu coba ekspor WebM menggunakan MediaRecorder browser.
- Saran highlight dari transkrip menggunakan Gemini API, jika backend dikonfigurasi.
- Antarmuka rasio dan teks sebagai panduan edit.

## Batasan jujur
Ekspor lokal bergantung pada dukungan browser dan dapat membebani HP. Format hasil umumnya WebM, bukan MP4. Pilihan rasio dan teks pada versi ini belum dibakar ke hasil video. Analisis AI membaca transkrip teks, bukan langsung memahami file video. Subtitle otomatis dari audio dan editor timeline belum tersedia.

## API key
Buat key melalui https://aistudio.google.com/. Jangan taruh key di HTML atau repository publik.

## Menjalankan backend
Perlu Node.js 18+. Atur environment variable lalu jalankan `npm start`.
PowerShell: `$env:GEMINI_API_KEY="API_KEY_ANDA"; npm start`
macOS/Linux: `GEMINI_API_KEY="API_KEY_ANDA" npm start`
Buka http://localhost:3000.

## Deploy
GitHub Pages hanya untuk frontend statis dan tidak menjalankan server Node.js. Deploy proyek ke hosting Node.js, set start command `npm start`, lalu tambahkan `GEMINI_API_KEY` pada Environment Variables. Jangan commit file `.env`.
