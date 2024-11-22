## Kode program 
```
# Program Daftar Nilai Mahasiswa Menggunakan Dictionary

# Dictionary untuk menyimpan data mahasiswa
data_mahasiswa = {}

def tambah_data():
    nama = input("Masukkan nama mahasiswa: ")
    tugas = float(input("Masukkan nilai tugas: "))
    uts = float(input("Masukkan nilai UTS: "))
    uas = float(input("Masukkan nilai UAS: "))
    nilai_akhir = (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)
    data_mahasiswa[nama] = {'Tugas': tugas, 'UTS': uts, 'UAS': uas, 'Nilai Akhir': nilai_akhir}
    print("Data berhasil ditambahkan!")

def ubah_data():
    nama = input("Masukkan nama mahasiswa yang akan diubah: ")
    if nama in data_mahasiswa:
        tugas = float(input("Masukkan nilai tugas baru: "))
        uts = float(input("Masukkan nilai UTS baru: "))
        uas = float(input("Masukkan nilai UAS baru: "))
        nilai_akhir = (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)
        data_mahasiswa[nama] = {'Tugas': tugas, 'UTS': uts, 'UAS': uas, 'Nilai Akhir': nilai_akhir}
        print("Data berhasil diubah!")
    else:
        print("Data tidak ditemukan!")

def hapus_data():
    nama = input("Masukkan nama mahasiswa yang akan dihapus: ")
    if nama in data_mahasiswa:
        del data_mahasiswa[nama]
        print("Data berhasil dihapus!")
    else:
        print("Data tidak ditemukan!")

def tampilkan_data():
    if data_mahasiswa:
        print("Daftar Nilai Mahasiswa")
        print("="*40)
        print(f"{'Nama':<15}{'Tugas':<10}{'UTS':<10}{'UAS':<10}{'Akhir':<10}")
        print("="*40)
        for nama, nilai in data_mahasiswa.items():
            print(f"{nama:<15}{nilai['Tugas']:<10}{nilai['UTS']:<10}{nilai['UAS']:<10}{nilai['Nilai Akhir']:<10.2f}")
        print("="*40)
    else:
        print("Belum ada data mahasiswa!")

def cari_data():
    nama = input("Masukkan nama mahasiswa yang dicari: ")
    if nama in data_mahasiswa:
        print(f"Nama: {nama}")
        print(f"Nilai Tugas: {data_mahasiswa[nama]['Tugas']}")
        print(f"Nilai UTS: {data_mahasiswa[nama]['UTS']}")
        print(f"Nilai UAS: {data_mahasiswa[nama]['UAS']}")
        print(f"Nilai Akhir: {data_mahasiswa[nama]['Nilai Akhir']:.2f}")
    else:
        print("Data tidak ditemukan!")

# Menu utama
while True:
    print("\nMenu:")
    print("1. Tambah nilai")
    print("2. Ubah Data")
    print("3. Hapus Data")
    print("4. Tampilkan nilai")
    print("5. Cari Data")
    print("6. Keluar")
    pilihan = input("Pilih menu (1-6): ")

    if pilihan == "1":
        tambah_data()
    elif pilihan == "2":
        ubah_data()
    elif pilihan == "3":
        hapus_data()
    elif pilihan == "4":
        tampilkan_data()
    elif pilihan == "5":
        cari_data()
    elif pilihan == "6":
        print("Program selesai. Terimakasih")
        break
    else:
        print("Pilihan tidak valid. Silakan pilih menu yang tersedia.")
```


## Output program
```
Daftar Nilai Mahasiswa
========================================
Nama           Tugas     UTS       UAS       Akhir
========================================
M Syarif       80.0      90.0      98.0      89.80
M Fikri        100.0     78.0      99.0      91.95
putri komala   100.0     98.0      99.0      98.95
========================================
```

## Flowchart
![flowchart](/flowchart6.png)
