# Simulasi Strategi Credit Transfer - Auction House Forza Horizon

Dokumen ini berisi analisis dan simulasi strategi pengiriman *credit* (CR) dari Akun A ke Akun B dengan meminimalkan dampak pajak 15% serta mengatasi keterbatasan modal awal Akun B (475K CR). Strategi ini menggunakan metode **"Naik Tangga"**, yaitu memutar modal dari mobil termurah hingga mencapai target profit maksimal menggunakan Daytona Shelby.

---

## 1. Perhitungan Profit Bersih B per Transaksi

Sebelum memulai simulasi, berikut adalah perhitungan profit bersih untuk setiap mobil setelah dipotong pajak sebesar 15% pada pendapatan Akun B.
Rumus: `Profit Bersih B = (Harga Jual Kiri × 85%) - Harga Beli Kanan`

| Mobil | Harga Beli (Kanan) | Harga Jual (Kiri) | Pendapatan B (Setelah Pajak 15%) | Profit Bersih B |
| :--- | :---: | :---: | :---: | :---: |
| **Daytona Shelby** | 10.000K | 20.000K | 17.000K | **+7.000K** |
| **MISSION R** | 2.500K | 5.000K | 4.250K | **+1.750K** |
| **Huayra BC COUPE** | 1.800K | 3.600K | 3.060K | **+1.260K** |
| **Monza Sp2** | 1.250K | 2.500K | 2.125K | **+875K** |
| **Lotus Evija** | 1.225K | 2.450K | 2.082,5K | **+857,5K** |
| **Jaguar XJR-15** | 475K | 950K | 807,5K | **+332,5K** |

---

## 2. Simulasi "Naik Tangga" (Transaksi 1 - 10)

Pada tahap awal, Akun B hanya memiliki modal **475K CR**. Setiap transaksi mewakili 1x limit *upload* lelang. Akun B akan selalu membeli mobil dengan profit tertinggi yang **bisa dijangkau oleh saldo saat itu**.

* **Transaksi 1:** Saldo 475K → Beli Jaguar (+332,5K) → **Saldo Akhir: 807,5K**
* **Transaksi 2:** Saldo 807,5K → Beli Jaguar (+332,5K) → **Saldo Akhir: 1.140K**
* **Transaksi 3:** Saldo 1.140K → Beli Jaguar (+332,5K) → **Saldo Akhir: 1.472,5K**
* **Transaksi 4:** Saldo 1.472,5K → Beli Monza (+875K) → **Saldo Akhir: 2.347,5K** *(Melewati Lotus karena Monza lebih menguntungkan)*
* **Transaksi 5:** Saldo 2.347,5K → Beli Huayra (+1.260K) → **Saldo Akhir: 3.607,5K**
* **Transaksi 6:** Saldo 3.607,5K → Beli Mission R (+1.750K) → **Saldo Akhir: 5.357,5K**
* **Transaksi 7:** Saldo 5.357,5K → Beli Mission R (+1.750K) → **Saldo Akhir: 7.107,5K**
* **Transaksi 8:** Saldo 7.107,5K → Beli Mission R (+1.750K) → **Saldo Akhir: 8.857,5K**
* **Transaksi 9:** Saldo 8.857,5K → Beli Mission R (+1.750K) → **Saldo Akhir: 10.607,5K**
* **Transaksi 10:** Saldo 10.607,5K → Beli Daytona Shelby (+7.000K) → **Saldo Akhir: 17.607,5K**

> **Catatan:** Pada transaksi ke-10, saldo B sudah menembus angka 10.000K CR, sehingga syarat modal minimum untuk membeli Daytona Shelby akhirnya terpenuhi.

---

## 3. Total Pendapatan Akun B Berdasarkan Batas Limit Transaksi

Mulai dari transaksi ke-11 dan seterusnya, modal Akun B sudah sangat mencukupi. Akun A dan B dapat melakukan *spam* transaksi **Daytona Shelby** secara terus-menerus untuk mencetak profit maksimal berkelanjutan (+7.000K per transaksi).

Berikut adalah akumulasi total saldo akhir di akun B berdasarkan variasi batasan limit transaksi harian:

### 📊 Ringkasan Pendapatan Bersih

| Jumlah Transaksi | Skema Perputaran | Total Saldo Akhir (CR) |
| :---: | :--- | :--- |
| **10 Kali** | 10 Transaksi Fase Awal ("Naik Tangga") | **17.607.500 CR** |
| **20 Kali** | 10 Transaksi Awal + 10x Transaksi Daytona Shelby | **87.607.500 CR** |
| **24 Kali** | 10 Transaksi Awal + 14x Transaksi Daytona Shelby | **115.607.500 CR** |
| **25 Kali** | 10 Transaksi Awal + 15x Transaksi Daytona Shelby (Limit Maksimal) | **122.607.500 CR** |

---
*Dokumen simulasi ini dibuat untuk membantu optimalisasi efisiensi transfer ekonomi di dalam game.*
