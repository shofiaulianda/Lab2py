# Lab2py

### NAMA : SHOFI AULIANDA
### NIM : 312510183
### KELAS : TI.25.A.2

## Laporan hasil latihan praktikum 2 : 

### Latihan 1: Membuat program menentukan nilai akhir

## Code Program :      
<img width="610" height="391" alt="image" src="https://github.com/user-attachments/assets/988868c1-1eaf-452a-beb4-c42b813e9840" />

## Output :     
<img width="592" height="233" alt="image" src="https://github.com/user-attachments/assets/9a870204-1a35-4a5c-9e4a-d0c4f42b8981" />

## Penjelasan Program :     
1. Input data mahasiswa   
Program meminta pengguna untuk mengisi:   

nama → nama mahasiswa    
uts → nilai Ujian Tengah Semester    
uas → nilai Ujian Akhir Semester    
tugas → nilai tugas    
```
nama = input("Masukkan nama: ")
uts = input("Masukkan nilai UTS: ")
uas = input("Masukkan nilai UAS: ")
tugas = input("Masukkan nilai Tugas: ")
```
Semua nilai yang diinput masih berupa string, jadi nanti diubah ke integer supaya bisa dihitung.

2. Hitung nilai akhir

Nilai akhir dihitung dengan bobot:    
Tugas = 20%     
UTS = 40%       
UAS = 40%     

akhir = (int(tugas) * 0.2) + (int(uts) * 0.4) + (int(uas) * 0.4)
Jadi nilai akhir adalah hasil rata-rata berbobot dari ketiga komponen.     

3. Menentukan keterangan lulus/tidak     
Menggunakan operator ternary di Python:    
keterangan = ("TIDAK LULUS", "LULUS")[akhir > 60.0]     

Artinya:

Jika akhir > 60, maka keterangan = "LULUS"

Jika akhir <= 60, maka keterangan = "TIDAK LULUS"

4. Menentukan nilai huruf

Gunakan if-elif-else untuk menentukan huruf sesuai rentang nilai:

Nilai Akhir	Nilai Huruf
> 80	A     
> 70	B       
> 50	C    
> 40	D     
≤ 40	E
```   
if akhir > 80:   
    huruf = "A"   
elif akhir > 70:    
    huruf = "B"     
elif akhir > 50:    
    huruf = "C"    
elif akhir > 40:    
    huruf = "D"   
else:   
    huruf = "E"   
```

5. Menampilkan hasil akhir

Program mencetak hasil lengkap:   
```
print("\nNama :", nama)
print("Nilai UTS :", uts)
print("Nilai UAS :", uas)
print("Nilai Tugas :", tugas)
print("Nilai Akhir :", round(akhir, 2))
print("\nNilai Huruf :", huruf)
print("Keterangan :", keterangan)
```

round(akhir, 2) digunakan agar nilai akhir tidak memiliki banyak angka di belakang koma.

### Latihan 2: Membuat program menampilkan status gaji karyawan.    

## Code Program :    
<img width="521" height="289" alt="image" src="https://github.com/user-attachments/assets/c9ae90aa-8eac-492e-afc7-5103af7fd073" />

## Output : 
<img width="594" height="133" alt="image" src="https://github.com/user-attachments/assets/a9fd8f4a-1cbf-4628-9362-6782e58179a0" />

## Penjelasan Program :     
1. Input data dari pengguna
```
gaji = int(input("Masukkan gaji: "))
berkeluarga = (False, True)[input("Sudah berkeluarga? (Y/T): ") == "Y"]
punya_rumah = (False, True)[input("Punya rumah? (Y/T): ") == "Y"]
```
Penjelasan:  
input() digunakan untuk meminta data dari pengguna.

int() mengubah nilai gaji yang dimasukkan (string) menjadi angka bulat (integer) agar bisa dibandingkan.

(False, True)[input(...) == "Y"] adalah operator ternary versi Python:

Jika pengguna menjawab "Y", maka hasilnya True.

Jika "T", maka hasilnya False.

Jadi variabel berkeluarga dan punya_rumah akan berisi nilai boolean (True atau False).

Contoh input:
```
Masukkan gaji: 4500000
Sudah berkeluarga? (Y/T): Y
Punya rumah? (Y/T): T
```   
2. Cek apakah gaji di atas UMR
```
if gaji > 3000000:
    print("Gaji sudah di atas UMR")
```

Jika gaji lebih dari Rp3.000.000, maka program akan menampilkan “Gaji sudah di atas UMR”.

Jika tidak, maka akan masuk ke blok else: di bawah dan menampilkan “Gaji belum UMR”.

3. Cek status keluarga
```
if berkeluarga:
    print("Wajib ikutan asuransi dan menabung untuk pensiun")
else:
    print("Tidak perlu ikutan asuransi")
```

Kalau berkeluarga == True → tampilkan kewajiban ikut asuransi dan menabung pensiun.

Kalau berkeluarga == False → tidak perlu ikut asuransi.

4. Cek status kepemilikan rumah
```
if punya_rumah:
    print("Wajib bayar pajak rumah")
else:
    print("Tidak wajib bayar pajak rumah")
```

Jika punya_rumah == True → wajib bayar pajak rumah.

Jika False → tidak wajib bayar pajak rumah.

5. Kondisi jika gaji di bawah atau sama dengan UMR
```
else:
    print("Gaji belum UMR")
```

Blok else ini hanya dijalankan kalau gaji <= 3000000.

Dalam hal ini, program tidak lagi memeriksa status keluarga atau rumah, karena fokusnya pada kondisi ekonomi di bawah UMR.

## Latihan 3: penggunaan kondisi OR    
program membandingkan 3 input bilangan, apabila penjumlahan 2 bilangan hasilnya    
sama dengan bilangan lainnya, maka cetak pernyataan “BENAR”    

## Code Program :    
<img width="395" height="151" alt="image" src="https://github.com/user-attachments/assets/da3344df-e7aa-491a-9802-fab64a6ce003" />

## Output :    
Kondisi benar :    
<img width="596" height="114" alt="image" src="https://github.com/user-attachments/assets/2d1daa87-7afb-49f5-b545-5dca52b0d3c8" />   

Kondisi salah :    
<img width="595" height="99" alt="image" src="https://github.com/user-attachments/assets/b2b32496-2232-420b-8333-ab925d5dbf84" />

## Latihan 3: Buat program python untuk kasus berikut:    
## Kasus 1: Program Pemesanan Tiket Bioskop   

## Code Program :    
<img width="453" height="394" alt="image" src="https://github.com/user-attachments/assets/2991b143-e214-4ce6-9b24-f7d61ff20714" />

## Output :   
<img width="587" height="189" alt="image" src="https://github.com/user-attachments/assets/0e2b302d-d5e6-42a3-9d40-aaa85dd59d71" />

## Penjelasan Program :   
1. Menampilkan judul dan pilihan tiket
```
print("=== PEMESANAN TIKET BIOSKOP ===")
print("Tipe tiket tersedia: Reguler / VIP")
```

Baris ini hanya menampilkan teks di layar agar user tahu bahwa ini program pemesanan tiket, serta pilihan tiket yang tersedia.

2. Input dari pengguna
```
tipe = input("Masukkan tipe tiket: ").lower()
member = input("Apakah kamu punya kartu member? (Y/T): ").upper()
```
Penjelasan:

input() digunakan untuk meminta data dari pengguna.

.lower() membuat input “Reguler” atau “VIP” menjadi huruf kecil semua supaya mudah dicek (jadi “reguler” atau “vip”).

.upper() membuat jawaban “Y” atau “T” selalu huruf besar.
Jadi, pengguna tidak perlu khawatir salah kapitalisasi.

3. Menentukan harga tiket
```
if tipe == "reguler":
    harga = 50000
elif tipe == "vip":
    harga = 100000
else:
    print("Tipe tiket tidak valid!")
    exit()
```

Penjelasan:

Jika user memilih reguler, maka harga tiket = Rp50.000.

Jika user memilih vip, maka harga tiket = Rp100.000.

Jika input selain dua itu, program akan berhenti (exit()) karena tidak valid.

4. Menghitung diskon menggunakan operator ternary
```
diskon = 0.2 if member == "Y" else 0
```

Ini adalah operator ternary, bentuk singkat dari if-else.

Artinya:

Kalau member == "Y", maka diskon = 0.2 (20%).

Kalau bukan, maka diskon = 0 (tidak ada diskon).

5. Hitung total harga setelah diskon
```
total = harga - (harga * diskon)
```

Misalnya:

Harga tiket VIP = Rp100.000

Diskon 20% → Rp100.000 × 0.2 = Rp20.000

Total bayar = Rp100.000 – Rp20.000 = Rp80.000

6. Menampilkan hasil akhir
```
print("\n=== RINCIAN PEMBAYARAN ===")
print("Tipe Tiket   :", tipe.capitalize())
print("Harga Tiket  : Rp", harga)
print("Diskon Member:", f"{int(diskon * 100)}%")
print("Total Bayar  : Rp", int(total))
```

Penjelasan:

.capitalize() membuat tampilan “Reguler” / “Vip” rapi (huruf pertama besar).

f"{int(diskon * 100)}%" mengubah nilai diskon (0.2) jadi “20%”.

int(total) menampilkan angka tanpa koma (pembulatan ke bawah).

## Kasus 2: Program Kalkulator Sederhana

## Code Program :    
<img width="542" height="378" alt="image" src="https://github.com/user-attachments/assets/c3b3f448-e492-4562-9d95-664937b7cf0c" />

## Output :   
<img width="587" height="131" alt="image" src="https://github.com/user-attachments/assets/4f9fa4ab-7966-4c95-b571-af0ece24c4bf" />

## Penjelasan Program :    
1. Menampilkan Judul dan Panduan
```
print("=== KALKULATOR SEDERHANA ===")
print("Operator yang tersedia: +, -, *, /")
```

Hanya menampilkan teks pembuka agar pengguna tahu program apa ini dan operator apa saja yang bisa digunakan.

2. Input dari Pengguna
```
angka1 = float(input("Masukkan angka pertama: "))
operator = input("Masukkan operator (+, -, *, /): ")
angka2 = float(input("Masukkan angka kedua: "))
```

Penjelasan:

input() digunakan untuk mengambil data dari pengguna.

float() digunakan supaya bisa menghitung bilangan desimal (misalnya 2.5 + 1.2).

operator adalah simbol aritmatika yang dimasukkan user (+, -, *, /).

Contoh input:
```
Masukkan angka pertama: 2
Masukkan operator (+, -, *, /): *
Masukkan angka kedua: 4
```
3. Proses Perhitungan dengan if-elif-else
```
if operator == "+":
    hasil = angka1 + angka2
elif operator == "-":
    hasil = angka1 - angka2
elif operator == "*":
    hasil = angka1 * angka2
elif operator == "/":
    if angka2 != 0:
        hasil = angka1 / angka2
    else:
        print("Error: Pembagian dengan nol tidak diperbolehkan!")
        exit()
else:
    print("Operator tidak valid!")
    exit()
```

Penjelasan:

if pertama: Jika operator adalah +, maka lakukan penjumlahan.

elif kedua: Jika operator adalah -, lakukan pengurangan.

elif ketiga: Jika operator adalah *, lakukan perkalian.

elif keempat: Jika operator adalah /, lakukan pembagian.

Ada tambahan pengecekan if angka2 != 0 untuk menghindari pembagian dengan nol (karena itu menyebabkan error di Python).

else terakhir: Jika operator selain + - * /, program berhenti dengan pesan “Operator tidak valid”.

4. Menampilkan Hasil Perhitungan
```
print(f"\nHasil: {angka1} {operator} {angka2} = {hasil}")
```

Baris ini mencetak hasil akhir dalam format yang mudah dibaca.
Contohnya:

Hasil: 2.0 + 4.0 = 6.0

