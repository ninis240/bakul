# List untuk menyimpan data siswa
data_siswa = []

# Fungsi menampilkan menu
def tampilkan_menu():
    print("\n=== Menu Manajemen Siswa ===")
    print("1. Tambah Siswa")
    print("2. Lihat Siswa")
    print("3. Edit Siswa")
    print("4. Hapus Siswa")
    print("5. Keluar")

# Fungsi menambah siswa
def tambah_siswa():
    nama = input("Masukkan Nama: ")
    usia = input("Masukkan Usia: ")
    nilai = input("Masukkan Nilai Rata-rata: ")
    data_siswa.append({"Nama": nama, "Usia": usia, "Nilai": nilai})
    print(f"[Siswa {nama} berhasil ditambahkan!]")

# Fungsi melihat daftar siswa
def lihat_siswa():
    if not data_siswa:
        print("[Belum ada data siswa]")
    else:
        print("\n=== Daftar Siswa ===")
        for i, siswa in enumerate(data_siswa):
            print(f"{i+1}. Nama: {siswa['Nama']}, Usia: {siswa['Usia']}, Nilai: {siswa['Nilai']}")

# Fungsi mengedit data siswa
def edit_siswa():
    lihat_siswa()
    if data_siswa:
        try:
            index = int(input("Pilih nomor siswa yang ingin diedit: ")) - 1
            if 0 <= index < len(data_siswa):
                nama_baru = input("Masukkan Nama Baru: ")
                usia_baru = input("Masukkan Usia Baru: ")
                nilai_baru = input("Masukkan Nilai Rata-rata Baru: ")
                data_siswa[index] = {"Nama": nama_baru, "Usia": usia_baru, "Nilai": nilai_baru}
                print("[Data siswa berhasil diperbarui!]")
            else:
                print("[Nomor tidak valid!]")
        except ValueError:
            print("[Masukkan angka yang valid!]")

# Fungsi menghapus siswa
def hapus_siswa():
    lihat_siswa()
    if data_siswa:
        try:
            index = int(input("Pilih nomor siswa yang ingin dihapus: ")) - 1
            if 0 <= index < len(data_siswa):
                siswa_dihapus = data_siswa.pop(index)
                print(f"[Siswa {siswa_dihapus['Nama']} berhasil dihapus!]")
            else:
                print("[Nomor tidak valid!]")
        except ValueError:
            print("[Masukkan angka yang valid!]")

# Loop utama program
while True:
    tampilkan_menu()
    pilihan = input("Pilih menu: ")
    
    if pilihan == "1":
        tambah_siswa()
    elif pilihan == "2":
        lihat_siswa()
    elif pilihan == "3":
        edit_siswa()
    elif pilihan == "4":
        hapus_siswa()
    elif pilihan == "5":
        print("[Keluar dari program...]")
        break
    else:
        print("[Pilihan tidak valid, coba lagi!]")
