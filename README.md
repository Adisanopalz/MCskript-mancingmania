# 🎣 Mancing Mania Skript - Custom Fishing Rewards

Skript ini menggantikan sistem loot memancing vanilla Minecraft dengan sistem *tier* dan *rarity* yang jauh lebih seru! Sangat cocok untuk memberikan pengalaman bermain yang *fun* dan *cozy* di server Survival Multiplayer (SMP) seperti Kazeno SMP. Pemain akan mendapatkan kejutan loot yang bervariasi mulai dari sampah hingga harta karun legendaris lengkap dengan efek suara, partikel, dan *broadcast* server.

**Versi:** 12.0

## ✨ Fitur Utama

Skript ini mendeteksi event `PlayerFishEvent` (saat pemain berhasil menangkap ikan) dan secara acak memberikan hadiah berdasarkan 5 tingkat *rarity*:

* 🌌 **MYTHIC (Peluang 0.1%)**
    * Loot: *Ancient Debris, Nether Star, Elytra/Beacon items, dll.*
    * Efek: Kembang api (firework), efek suara *challenge complete*, dan *broadcast* pengumuman ke seluruh server.
* 👑 **LEGENDARY (Peluang 1%)**
    * Loot: *Diamond, Emerald, Shulker Shell, Totem items, dll.*
    * Efek: Partikel Totem of Undying, efek suara level-up, dan pesan *broadcast* server.
* 🟣 **EPIC (Peluang 5%)**
    * Loot: *Raw ore blocks, Slime ball, Piston, TNT, dll.*
    * Efek: Efek suara EXP orb dan pesan personal ke pemain.
* 🔵 **RARE (Peluang 15%)**
    * Loot: *Raw ores, Quartz, Saplings, Buku, dll.*
    * Efek: Efek suara *item pickup* dan notifikasi di *Action Bar*.
* 🟤 **JUNK (Peluang 25%)**
    * Loot: *Rotten flesh, Sticks, Dirt, Seeds, dll.*
    * Efek: Efek suara *villager no* (zonk) dan pesan kecewa di chat.

*(Catatan: Semua item yang didapatkan memiliki deskripsi "Lore" khusus sesuai dengan tingkat rarity-nya.)*

## ⚙️ Persyaratan (Requirements)

* **Plugin Skript:** Pastikan plugin Skript sudah terpasang di server kamu.
* **Server Core:** Paper / Spigot (Telah diuji dan kompatibel dengan versi 1.21).

## 🚀 Cara Instalasi

1. Unduh file `mancingmania.sk`.
2. Masukkan file tersebut ke dalam folder plugin server kamu: `plugins/Skript/scripts/`.
3. Buka console server atau chat in-game (jika kamu memiliki akses OP), lalu ketik perintah:
   `/sk reload mancingmania`
4. Jika berhasil, kamu akan melihat pesan konfirmasi hijau di console yang menyatakan script berhasil dimuat.

## 🛠️ Konfigurasi (Tuning Rarity)

Kamu bisa mengubah peluang (*chance*) untuk masing-masing *tier* dengan sangat mudah. Buka file `mancingmania.sk` dengan text editor, lalu ubah persentase di bagian `options`:

```skript
options:
    p: &8[&b&lMANCING&8]
    chance_mythic: 0.1%  # Ubah angka ini sesuai kebutuhan ekonomi server
    chance_legend: 1%
    chance_epic: 5%
    chance_rare: 15%
    chance_junk: 25%
