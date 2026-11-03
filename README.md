# Kumpulan Cheat Pokémon R.O.W.E v2.1b

Kode cheat siap pakai untuk game **Pokémon R.O.W.E v2.1b** (Game Boy Advance).
Tinggal salin, tempel ke emulator, selesai.

> ⚠️ File game (ROM `.gba`) **tidak disertakan** di sini. Cari dan gunakan ROM milikmu sendiri.

- **Tipe kode:** CodeBreaker (kalau emulator tidak punya pilihan itu, pakai GameShark)
- **Sudah dites di:** Pizza Boy (emulator Android)
- **Versi ROM:** Pokemon R.O.W.E v2.1b.gba (sha256 diawali `1eee3cb4`, diakhiri `fb96f`)

---

## Cara Pakai (untuk pemula)

1. **Save game dulu** di dalam game, jaga-jaga kalau ada masalah.
2. Buka salah satu file di folder [`cheats/`](cheats/).
3. Salin **semua** isinya.
4. Di emulator, buka menu cheat dan tambah cheat baru. Pilih tipe **CodeBreaker**, lalu tempel kodenya sebagai **satu** cheat.
5. Aktifkan cheat tersebut. Sebaiknya **satu cheat saja** dalam satu waktu.
6. Setelah selesai dipakai, **matikan lagi** cheat-nya.

---

## Daftar Cheat

| No | File | Fungsinya | Status |
|----|------|-----------|--------|
| 1 | `1_Catch_100.txt` | Semua Poké Ball pasti berhasil menangkap (pengganti Master Ball) | ✅ Berhasil |
| 2 | `2_Infinite_EXP_tahan_R.txt` | Tahan tombol **R** setelah menang battle, EXP terus bertambah (pengganti Rare Candy) | ✅ Berhasil |
| 3 | `3_Easy_Battle.txt` | Stat Pokémon kita jadi maksimal, stat lawan jadi minimal | ✅ Berhasil |
| 4 | `4_Mart_Item_TEMPLATE.txt` | Barang pertama di Poké Mart diganti barang pilihanmu | ✅ Berhasil |
| 5 | `5_PC_Nugget_x5.txt` | 5 Nugget di PC (Item Storage), terisi lagi tiap diambil. Jual ke Mart untuk uang | ⚠️ Belum dites |
| 6 | `6_PC_Item_TEMPLATE_x5.txt` | 5 buah item apa saja di PC (Item Storage) | ⚠️ Belum dites |

### Cheat "TEMPLATE" (no. 4 dan 6)

File yang namanya ada `TEMPLATE` berisi tulisan `YYYY`. Ganti **semua** `YYYY` dengan kode item yang kamu mau.

Contoh: mau **Nugget** → ganti `YYYY` jadi `007C`.

```
820051B4 YYYY   →   820051B4 007C
```

Daftar lengkap kode item ada di [`data/item_ids.txt`](data/item_ids.txt) (lihat catatan validasi di bawah).

### Catatan khusus cheat no. 5 dan 6

- Kodenya terlalu panjang untuk satu cheat, jadi di dalam file dibagi jadi **4 BAGIAN**. Salin tiap bagian sebagai **cheat terpisah** (jadi ada 4 cheat), lalu **aktifkan keempatnya sekaligus**.
- Cara pakai lengkap ada di bagian atas tiap file. Jangan ikut menyalin teks penjelasan, cukup baris kodenya.
- Item di slot pertama PC Item Storage akan **tertimpa**.
- Jumlahnya sengaja dibatasi 5. Versi 999 membuat game **reset** saat membuka PC (game ini punya anti-cheat).
- Kalau game reset: matikan cheat-nya, lalu buang (toss) item cheat dari PC.

---

## Kode Item yang Sering Dipakai

| Item | Kode |
|------|------|
| Nugget | `007C` |
| Max Revive | `0028` |
| PP Max | `004E` |
| Ability Capsule | `005D` |
| Leftovers | `00E5` |
| Mega Bracelet | `01BC` |
| TM01 – TM120 | `01E2` – `0259` |
| HM01 – HM08 | `02AA` – `02B1` |

File data:

> ⚠️ **Belum divalidasi.** Isi folder `data/` dibaca dari ROM tapi belum dicek satu per satu di dalam game, jadi bisa ada kode yang salah. Ini juga berlaku untuk tabel kode item di atas. Kalau ketemu yang salah, silakan buka Issue.

- [`data/item_ids.txt`](data/item_ids.txt): 843 item, diambil langsung dari ROM ini
- [`data/pokemon_ids.txt`](data/pokemon_ids.txt): 1025 Pokémon (disiapkan untuk cheat DexNav, belum dibuat)

---

## Yang Tidak Bisa

| Percobaan | Alasan | Solusinya |
|-----------|--------|-----------|
| Rare Candy (`004B`) | Dimatikan oleh pembuat ROWE ("time and place") | Pakai cheat no. 2 |
| Master Ball (`0001`) | Diubah jadi Poké Ball biasa | Pakai cheat no. 1 |
| Semua harga jadi $1 | Sudah dites, tidak berhasil | — |
| Item langsung masuk tas | Lokasi data save berpindah acak tiap load/pindah map, jumlah item dienkripsi | Pakai cheat no. 4, 5, atau 6 |

---

## Catatan Teknis (untuk yang penasaran)

- Pointer SaveBlock1 = `03004B7C`, posisinya = `02026268 + (0..7C)`, PC item = `+0x408`
- Skrip battle `02024DB4`: gagal-goyang `08398BB1` → berhasil `08398B3C`
- DexNav: pointer pencarian `0203E828` (heap), variabel Quick Search `0x40F7`

---

Gunakan dengan risiko sendiri. Selalu save sebelum mencoba cheat. 🎮
