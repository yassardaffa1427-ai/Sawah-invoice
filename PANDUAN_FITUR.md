# 📋 Panduan Lengkap Invoice App - Sawah Studio

## 🚀 Fitur Utama

### 1. **Aplikasi Web Responsif**
- ✅ Desktop, tablet, dan mobile siap digunakan
- ✅ Interface yang intuitif dan user-friendly
- ✅ Real-time calculation untuk total, diskon, dan pajak
- ✅ Dark modern theme yang professional

---

## 📱 Cara Menggunakan Aplikasi

### **Step 1: Isi Detail Invoice**
1. Buka file `invoice_sawah.html` di browser
2. Nomor invoice otomatis terisi dengan format `#INV/XXX/YYYY`
3. Tanggal transaksi otomatis hari ini, bisa diubah sesuai kebutuhan

### **Step 2: Masukkan Data Pembeli**
1. Isi **Nama Pembeli** (wajib)
2. Isi **Rekening/Kontak** (opsional - nomor HP atau rekening bank)
3. Pilih **Metode Pembayaran** dari 6 opsi:
   - Transfer Bank
   - QRIS
   - Tunai / Cash
   - Dana
   - GoPay
   - OVO

### **Step 3: Tambah Item Layanan**
1. Klik tombol **"+ Tambah item"**
2. Isi **Keterangan** - nama produk atau jenis layanan
3. Isi **Qty** - jumlah item
4. Isi **Price** - harga satuan
5. **Jumlah Bayar** otomatis terhitung (Qty × Price)
6. Ulangi untuk item berikutnya

**Tips:** 
- Klik **×** untuk menghapus item
- Data akan langsung terupdate saat diubah
- Nomor item otomatis berurutan

### **Step 4: Atur Diskon & Pajak**
1. Masukkan persentase **Diskon** (dari subtotal)
2. Masukkan persentase **Pajak** (setelah diskon)
3. Ringkasan biaya akan langsung terupdate:
   - **Sub total** - jumlah semua item
   - **Diskon** - potongan harga (ditampilkan hijau)
   - **Pajak** - biaya tambahan (ditampilkan oranye)
   - **Total** - jumlah akhir yang harus dibayar

### **Step 5: Tambah Catatan**
1. Masukkan catatan atau syarat pembayaran di bagian **Catatan**
2. Teks ini akan muncul di preview dan Excel export
3. Contoh: "Pembayaran dalam 14 hari", "Terima kasih atas kerja samanya"

### **Step 6: Preview Invoice**
1. Klik tombol **"Preview"** untuk melihat tampilan invoice
2. Preview menampilkan invoice siap cetak dengan:
   - Header perusahaan (Sawah Studio)
   - Nomor invoice dan tanggal
   - Data pembeli dan metode pembayaran
   - Tabel item dengan detail lengkap
   - Summary biaya dengan perhitungan rinci
   - Catatan dan footer

### **Step 7: Cetak atau Simpan PDF**
Di tampilan Preview:
1. Klik tombol **"Cetak / Save PDF"**
2. Dialog print sistem akan muncul
3. Pilih printer atau "Save as PDF"
4. Klik Print untuk mengunduh

**Shortcut:**
- Gunakan `Ctrl+P` (Windows) atau `Cmd+P` (Mac)
- Pilih "Save as PDF" untuk menyimpan file

### **Step 8: Export ke Excel** (Opsional)
1. Klik tombol **"Export Excel"** untuk mengunduh file Excel
2. File akan berisi:
   - Formatted table dengan styling
   - Formula perhitungan otomatis
   - Header dan footer lengkap
   - Siap untuk dicetak atau dimodifikasi di Excel

---

## 🎯 Fitur-Fitur Khusus

### **📊 Kalkulasi Otomatis**
- Setiap perubahan langsung dihitung real-time
- Amount per item = Qty × Price
- Subtotal = Σ semua Amount
- Diskon = Subtotal × (Diskon %)
- Pajak = (Subtotal - Diskon) × (Pajak %)
- Total = Subtotal - Diskon + Pajak

### **👁️ Preview Mode**
- Tampilan profesional yang siap cetak
- Responsive di semua ukuran layar
- Bisa dibuka di mobile tetap rapi
- Print-friendly styling

### **📱 Responsive Design**
**Desktop:**
- Semua elemen terlihat dan mudah diakses
- Layout side-by-side untuk efisiensi
- Hover effects dan animasi smooth

**Tablet:**
- Single column yang terstruktur
- Touch-friendly button dan input
- Optimal untuk landscape & portrait

**Mobile:**
- Full responsive satu kolom
- Input fields diperbesar untuk kemudahan
- Button min 44px untuk tap yang mudah
- Payment options 2 kolom

### **🎨 Fitur Panduan**
- Klik tombol **"Panduan"** untuk melihat visual step-by-step
- Terdapat 6 langkah mudah membuat invoice
- Modal yang bisa di-scroll dan close dengan ESC key

---

## 💡 Tips & Trik

### **Input Data Cepat**
1. Gunakan Tab key untuk pindah antar field
2. Untuk qty dan price, gunakan angka saja
3. Deskripsi bisa multi-line dengan Enter

### **Menghapus Item**
1. Hover atau tap item yang ingin dihapus
2. Klik tombol × di sebelah kanan
3. Item akan hilang dan nomor otomatis ter-update

### **Mengubah Total**
Jika perlu mengubah nomor invoice atau tanggal:
1. Klik di field "No. Invoice" atau "Tanggal Transaksi"
2. Edit sesuai kebutuhan
3. Perubahan langsung tersimpan (auto-save)

### **Copy Invoice**
Untuk membuat invoice mirip:
1. Salin semua data dari invoice sebelumnya
2. Ganti nomor invoice dan tanggal baru
3. Update item dan pembeli
4. Klik Preview atau Export

---

## 📁 File-File yang Ada

```
invoice/
├── invoice_sawah.html          ← Aplikasi utama (buka ini)
├── invoice-preview-template.html   ← Contoh tampilan preview
├── user-flow-guide.html        ← Panduan visual user flow
└── PANDUAN_FITUR.md            ← File ini
```

### **Bagaimana Membuka Aplikasi?**
1. **Opsi 1: Direct Open**
   - Buka file `invoice_sawah.html` langsung di browser
   - Double-click file atau drag ke browser

2. **Opsi 2: Local Server** (Recommended)
   ```bash
   # Di folder invoice, jalankan:
   python -m http.server 8000
   # Buka browser ke: http://localhost:8000/invoice_sawah.html
   ```

3. **Opsi 3: Live Server** (Jika pakai VS Code)
   - Install extension "Live Server"
   - Right-click file → "Open with Live Server"

---

## 🖨️ Opsi Print/Export

### **Method 1: Preview + Print**
✅ Rekomendasi untuk hasil terbaik
1. Klik "Preview" di aplikasi
2. Tampilan invoice professional muncul
3. Klik "Cetak / Save PDF"
4. Pilih printer atau Save as PDF
5. File siap dikirim atau dicetak

### **Method 2: Print Langsung**
Dari aplikasi form, gunakan Ctrl+P (jika diperlukan custom)

### **Method 3: Export Excel**
1. Klik "Export Excel" di aplikasi
2. File .xlsx otomatis download
3. Buka di Excel untuk edit lanjutan
4. Print dari Excel jika perlu

---

## 🎨 Customization

### **Mengubah Warna**
Edit CSS di file `invoice_sawah.html` bagian `:root`:
```css
:root {
  --gold: #d4a843;      /* Warna accent (ubah sesuai brand) */
  --bg: #0d0d0d;        /* Background warna gelap */
  --surface: #181818;   /* Card background */
  --text: #efefef;      /* Text color */
}
```

### **Mengubah Font**
Edit bagian Google Fonts import di `<head>` tag:
```html
<link href="https://fonts.googleapis.com/css2?family=..." rel="stylesheet"/>
```

### **Mengubah Company Info**
Edit di aplikasi atau di print template:
- Company Name: "SAWAH STUDIO"
- Tagline: "Fresh made by people of sawah"
- Contact: "y26site.framer.ai | +62 85810803909"

---

## ❓ FAQ

**Q: Invoice bisa disimpan otomatis?**
A: Tidak, tapi data tetap ada selama tab browser terbuka. Simpan dengan Export Excel atau Print to PDF.

**Q: Bisa edit invoice yang sudah dibuat?**
A: Ya, cukup edit field yang ingin diubah, data langsung terupdate.

**Q: PDF yang dihasilkan bisa diedit?**
A: PDF standar tidak bisa diedit. Gunakan Excel export jika perlu edit formula.

**Q: Bisa custom nomor invoice?**
A: Ya, edit di field "No. Invoice" sesuai format yang ingin digunakan.

**Q: Harga bisa lebih dari 2 decimal?**
A: Ya, sistem otomatis round ke rupiah terdekat.

**Q: Bisa tambah logo?**
A: Bisa dengan edit HTML file dan tambahkan `<img>` tag di print template.

---

## 🆘 Troubleshooting

### **Preview tidak muncul**
- Pastikan sudah isi minimal nama pembeli
- Refresh browser dan coba lagi
- Cek console browser untuk error (F12)

### **Angka tidak terhitung**
- Pastikan format angka benar (hanya angka, tanpa Rp.)
- Qty dan Price harus numeric
- Refresh halaman jika masih error

### **Print output jelek**
- Pastikan browser zoom 100% (Ctrl+0)
- Disable headers/footers di print dialog
- Gunakan ukuran kertas A4 (default)

### **File Excel tidak bisa dibuka**
- Pastikan Microsoft Excel atau alternatif installed
- Coba open dengan Google Sheets atau LibreOffice

---

## 📞 Support

Untuk pertanyaan atau issue:
1. Baca FAQ di atas
2. Cek file dokumentasi yang ada
3. Lihat console browser (F12) untuk error messages

---

## ✨ Fitur Masa Depan (Planned)

- ✓ Template invoice multiple
- ✓ Database penyimpanan data
- ✓ Multi-currency support
- ✓ Recurring invoice
- ✓ Integration dengan payment gateway
- ✓ Mobile app native

---

**Invoice App v1.0**
Dibuat dengan ❤️ oleh Sawah Studio
Last Updated: 26 Agustus 2024