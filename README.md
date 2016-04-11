# Tululised Werewolf Moderator Bot

inspired by [WerewolfBot](https://telegram.me/werewolfbot)

[play me!](https://telegram.me/lycantulul_bot)

### Daftar Perintah
- `/start` - Mulai berhubungan dan mendaftarkan diri
- `/help` - Liat petunjuk (link ke github doang ini)
- `/bikin_baru` - Bikin game baru
- `/batalin` - Batalin game
- `/ikutan` - Ikutan main
- `/gajadi` - Ga jadi ikutan main
- `/mulai_main` - Mulai main
- `/siapa_aja` - Liat siapa aja yang lagi main
- `/hasil_voting` - Liat hasil voting sementara
- `/panggil_semua` - Panggil semua pemain
- `/panggil_yang_idup` - cukup jelas
- `/panggil_yang_belom_voting` - cukup jelas
- `/ilangin_keyboard` - Reply keyboard muncul terus? Cobain nih

### Jumlah & Penjelasan Peran

#### Jumlah dan Pola Kemunculan Peran
1. Warga Kampung: selalu ada, sisa pemain yang tidak dapat peran.
1. Pak Raden: muncul saat jumlah pemain 9 orang dengan kemungkinan 35%
1. Pak Ogah: muncul saat jumlah pemain 11 orang dengan kemungkinan 70%
1. TTS (Tulul-Tulul Serigala): selalu ada, bertambah setiap 5 pemain (5 pemain: 1 TTS, 10 pemain: 2 TTS, dst.).
1. Tukang Ngintip: muncul saat jumlah pemain 6 orang, bertambah setiap 12 pemain (6 pemain: 1 Tukang Ngintip, 18 pemain: 2 Tukang Ngintip, dst.).
1. Penjual Jimat: muncul saat jumlah pemain 8 orang, bertambah setiap 14 pemain (8 pemain: 1 Penjual Jimat, 22 pemain: 2 Penjual Jimat, dst.).
1. Mujahid: muncul saat jumlah pemain 12 orang, hanya ada 1 Mujahid
1. Pengidap Ebola: muncul saat jumlah pemain 14 orang, bertambah setiap 10 pemain (14 pemain: 1 Pengidap Ebola, 24 pemain: 2 Pengidap Ebola, dst.).

#### Penjelasan Tugas Peran
1. Warga Kampung
   - Dibunuh dan ikut voting eksekusi.
1. Pak Raden
   - Dibunuh dan ikut voting eksekusi.
   - Saat voting, bobot suaranya 3
1. Pak Ogah
   - Dibunuh dan ikut voting eksekusi.
   - Saat voting, bobot suaranya 0
1. TTS (Tulul-Tulul Serigala)
   - Membunuh semua yang bukan TTS.
   - Jika ada lebih dari 1 TTS, maka proses membunuh adalah voting antara para TTS. Jika tidak ada suara yang mayoritas, tidak ada yang mati.
   - Jika membunuh seseorang yang dilindungi Penjual Jimat, korban tidak akan mati.
   - Jika membunuh Pengidap Ebola, salah satu serigala yang masih hidup akan ikut mati (dipilih secara acak).
1. Tukang Ngintip
   - Mengintip peran pemain lain.
1. Penjual Jimat
   - Melindungi salah satu pemain dari dibunuh TTS.
   - Jika yang dilindungi adalah TTS, ada 25% kemungkinan si Penjual Jimat akan mati.
1. Mujahid
   - Menghidupkan salah satu pemain yang sudah mati.
   - Sebagai gantinya, si Mujahid akan mati.
1. Pengidap Ebola
   - Sama seperti Warga Kampung.
   - Jika dibunuh TTS, maka salah satu dari TTS akan ikut mati (dipilih secara acak).

### Akhir Permainan

Permainan berakhir saat:
- Tidak ada lagi yang bisa dibunuh oleh TTS (jumlah TTS yang hidup lebih banyak atau sama dengan jumlah pemain non-TTS yang hidup). Kemenangan bagi TTS.
- Semua TTS sudah mati dieksekusi. Kemenangan bagi warga.