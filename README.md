# 🎣 Mancing Mania Skript - Custom Fishing Rewards

Skript ini menggantikan sistem loot memancing vanilla Minecraft dengan sistem *tier* dan *rarity* yang jauh lebih seru! Sangat cocok untuk memberikan pengalaman bermain yang *fun* dan *cozy* di server Survival Multiplayer (SMP) seperti Kazeno SMP. Pemain akan mendapatkan kejutan loot yang bervariasi mulai dari sampah hingga harta karun legendaris lengkap dengan efek suara, partikel, dan *broadcast* server.

[cite_start]**Versi:** 12.0 [cite: 1]

## ✨ Fitur Utama

[cite_start]Skript ini mendeteksi event `PlayerFishEvent` (saat pemain berhasil menangkap ikan) [cite: 2] [cite_start]dan secara acak memberikan hadiah berdasarkan 5 tingkat *rarity*[cite: 1]:

* [cite_start]🌌 **MYTHIC (Peluang 0.1%)** [cite: 1]
    * [cite_start]Loot: *Ancient Debris, Nether Star, Elytra/Beacon items, dll.* [cite: 4, 5]
    * [cite_start]Efek: Kembang api (firework) [cite: 7][cite_start], efek suara *challenge complete* [cite: 7][cite_start], dan *broadcast* pengumuman ke seluruh server[cite: 7, 8].
* [cite_start]👑 **LEGENDARY (Peluang 1%)** [cite: 1]
    * [cite_start]Loot: *Diamond, Emerald, Shulker Shell, Totem items, dll.* [cite: 8, 9]
    * [cite_start]Efek: Partikel Totem of Undying [cite: 11][cite_start], efek suara level-up [cite: 11][cite_start], dan pesan *broadcast* server[cite: 11].
* [cite_start]🟣 **EPIC (Peluang 5%)** [cite: 1]
    * [cite_start]Loot: *Raw ore blocks, Slime ball, Piston, TNT, dll.* [cite: 12, 13]
    * [cite_start]Efek: Efek suara EXP orb dan pesan personal ke pemain[cite: 15].
* [cite_start]🔵 **RARE (Peluang 15%)** [cite: 1]
    * [cite_start]Loot: *Raw ores, Quartz, Saplings, Buku, dll.* [cite: 16, 17, 18, 19]
    * [cite_start]Efek: Efek suara *item pickup* [cite: 20] [cite_start]dan notifikasi di *Action Bar*[cite: 20, 21].
* [cite_start]🟤 **JUNK (Peluang 25%)** [cite: 1]
    * [cite_start]Loot: *Rotten flesh, Sticks, Dirt, Seeds, dll.* [cite: 21, 22, 23, 24]
    * [cite_start]Efek: Efek suara *villager no* (zonk) dan pesan kecewa di chat[cite: 25].

[cite_start]*(Catatan: Semua item yang didapatkan memiliki deskripsi "Lore" khusus sesuai dengan tingkat rarity-nya[cite: 6, 10, 15, 20, 24].)*

## ⚙️ Persyaratan (Requirements)

* **Plugin Skript:** Pastikan plugin Skript sudah terpasang di server kamu.
* [cite_start]**Server Core:** Paper / Spigot (Telah diuji dan kompatibel dengan versi 1.21 [cite: 2]).

## 🚀 Cara Instalasi

1. Unduh file `mancingmania.sk`.
2. Masukkan file tersebut ke dalam folder plugin server kamu: `plugins/Skript/scripts/`.
3. Buka console server atau chat in-game (jika kamu memiliki akses OP), lalu ketik perintah:
   `/sk reload mancingmania`
4. [cite_start]Jika berhasil, kamu akan melihat pesan konfirmasi hijau di console yang menyatakan script berhasil dimuat[cite: 1, 2].

## 🛠️ Konfigurasi (Tuning Rarity)

Kamu bisa mengubah peluang (*chance*) untuk masing-masing *tier* dengan sangat mudah. [cite_start]Buka file `mancingmania.sk` dengan text editor, lalu ubah persentase di bagian `options`[cite: 1]:

```skript
options:
    p: &8[&b&lMANCING&8]
    chance_mythic: 0.1%  # Ubah angka ini sesuai kebutuhan ekonomi server
    chance_legend: 1%
    chance_epic: 5%
    chance_rare: 15%
    chance_junk: 25%
