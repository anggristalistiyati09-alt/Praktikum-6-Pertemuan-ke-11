# Praktikum-6-Pertemuan-ke-11

# daftar nilai mahasiswa

    # Inisialisasi kamus kosong untuk menyimpan data nilai mahasiswa
    data_mahasiswa = {}

    # Fungsi untuk menambah data mahasiswa baru
    def tambah():
      nama = input("Masukkan nama mahasiswa: ")
      nilai = input("Masukkan nilai mahasiswa: ")
      data_mahasiswa[nama] = nilai
      print(f"Data {nama} berhasil ditambahkan.")

    # Fungsi untuk menampilkan seluruh data mahasiswa
    def tampilkan():
        if not data_mahasiswa:
            print("Daftar nilai mahasiswa kosong.")
        else:
            print("Daftar Nilai Mahasiswa:")
            for nama, nilai in data_mahasiswa.items():
                print(f"Nama: {nama}, Nilai: {nilai}")

    # Fungsi untuk menghapus data mahasiswa berdasarkan nama
    def hapus(nama):
        if nama in data_mahasiswa:
            del data_mahasiswa[nama]
            print(f"Data {nama} berhasil dihapus.")
        else:
            print(f"Data {nama} tidak ditemukan.")

    # Fungsi untuk mengubah data mahasiswa berdasarkan nama
    def ubah(nama):
        if nama in data_mahasiswa:
            nilai_baru = input(f"Masukkan nilai baru untuk {nama}: ")
            data_mahasiswa[nama] = nilai_baru
            print(f"Data {nama} berhasil diubah.")
        else:
            print(f"Data {nama} tidak ditemukan.")

    # Loop utama program untuk menampilkan menu dan memproses input pengguna
    while True:
        print("\nMenu Program:")
        print("1. Tambah data mahasiswa")
        print("2. Tampilkan data mahasiswa")
        print("3. Hapus data mahasiswa")
        print("4. Ubah data mahasiswa")
        print("5. Keluar")

        pilihan = input("Masukkan pilihan Anda (1-5): ")

        if pilihan == '1':
            tambah()
        elif pilihan == '2':
            tampilkan()
        elif pilihan == '3':
            nama_hapus = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            hapus(nama_hapus)
        elif pilihan == '4':
            nama_ubah = input("Masukkan nama mahasiswa yang ingin diubah: ")
            ubah(nama_ubah)
        elif pilihan == '5':
            print("Program selesai.")
            break
        else:
            print("Pilihan tidak valid. Silakan masukkan angka 1-5.")

# hasil dari program tersebut

<img width="266" height="284" alt="image" src="https://github.com/user-attachments/assets/1730699d-9a73-44a4-bfb7-09a7656b720d" />

# FlowChart

<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/bc6adabf-1b09-48c0-bfb4-a672f036b58d" />

# Penjelasan Program
1. Inisialisasi struktur data
Program ini akan menggunakan sebuah list global bernama daftar_nilai untuk menyimpan data mahasiswa. Setiap data mahasiswa akan disimpan dalam bentuk dictionary yang berisi 'nama' dan 'nilai'.
2. Implementasi fungsi tambah()
Fungsi tambah() akan meminta input nama dan nilai dari pengguna, kemudian menambahkannya ke dalam list daftar_nilai.
3. Implementasi fungsi tampilkan()
Fungsi tampilkan() akan menampilkan seluruh data mahasiswa yang ada di dalam list daftar_nilai dalam format yang mudah dibaca.
4. Implementasi fungsi hapus(nama)
Fungsi hapus(nama) akan mencari dan menghapus data mahasiswa berdasarkan nama yang diberikan sebagai parameter.
5. Implementasi menu utama program
Tambahkan menu utama untuk memudahkan interaksi pengguna dengan program, memungkinkan mereka memilih fungsi mana yang ingin dijalankan.

