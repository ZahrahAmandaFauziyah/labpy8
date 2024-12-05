# labpy8
Tugas Praktikum 08

KODE PYTHON:

    class DaftarNilaiMahasiswa:
    def __init__(self):  
        self.mahasiswa = {}

    def tambah(self, nama, nilai):
        """Menambah data mahasiswa."""
        self.mahasiswa[nama] = nilai
        print(f"Data {nama} dengan nilai {nilai} berhasil ditambahkan.")

    def tampilkan(self):
        """Menampilkan semua data mahasiswa."""
        if not self.mahasiswa:
            print("Tidak ada data mahasiswa.")
        else:
            print("Daftar Nilai Mahasiswa:")
            for nama, nilai in self.mahasiswa.items():
                print(f"Nama: {nama}, Nilai: {nilai}")

    def hapus(self, nama):
        """Menghapus data mahasiswa berdasarkan nama."""
        if nama in self.mahasiswa:
            del self.mahasiswa[nama]
            print(f"Data {nama} berhasil dihapus.")
        else:
            print(f"Data {nama} tidak ditemukan.")

    def ubah(self, nama, nilai_baru): 
        """Mengubah data mahasiswa berdasarkan nama."""
        if nama in self.mahasiswa:
            self.mahasiswa[nama] = nilai_baru
            print(f"Data {nama} berhasil diubah menjadi nilai {nilai_baru}.")
        else:
            print(f"Data {nama} tidak ditemukan.")

    def main():
    daftar = DaftarNilaiMahasiswa()

    while True:
        print("\nMenu:")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Hapus Data")
        print("4. Ubah Data")
        print("5. Keluar")

        pilihan = input("Pilih menu: ")

        if pilihan == '1':
            nama = input("Masukkan nama mahasiswa: ")
            try:
                nilai = int(input("Masukkan nilai mahasiswa: "))
                daftar.tambah(nama, nilai)
            except ValueError:
                print("Nilai harus berupa angka.")
        elif pilihan == '2':
            daftar.tampilkan()
        elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            daftar.hapus(nama)
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            try:
                nilai_baru = int(input("Masukkan nilai baru: "))
                daftar.ubah(nama, nilai_baru)
            except ValueError:
                print("Nilai harus berupa angka.")
        elif pilihan == '5':
            print("Keluar dari program.")
            break
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")

    if __name__ == "__main__":
    main()

![Cuplikan layar 2024-12-05 205016](https://github.com/user-attachments/assets/d9bb5c1c-0d89-44a1-a056-bbf45c7cca2f)
![Cuplikan layar 2024-12-05 210148](https://github.com/user-attachments/assets/d3994d7f-5428-42c7-af03-44f1e4459a5f)
![Cuplikan layar 2024-12-05 210212](https://github.com/user-attachments/assets/8ba077f5-5873-42e0-ae51-63c07ed8d2ca)

PENJELASAN:

1. Tambah Data: Menyimpan nama dan nilai mahasiswa ke dalam dictionary.
2. Tampilkan Data: Menampilkan semua data mahasiswa dalam format daftar.
3. Hapus Data: Menghapus data mahasiswa berdasarkan nama berdasarkan nama.
4. Ubah Data: Mengupdate nilai mahasiswa berdasarkan nama.
Program menyediakan menu interaktif berbasis teks untuk pengguna, berjalan dalam loop hingga memilih opsi Keluar.

FLOWCHART:
![FLOWCHART PERT 12](https://github.com/user-attachments/assets/7a1d7bff-3c33-4503-98a4-ab6629716985)

DIAGRAM CLASS:
![diagram](https://github.com/user-attachments/assets/173ccabc-23f1-4028-b2b8-cc34e928203f)

PENJELASAN DIAGRAM CLASS: Atribut: mahasiswa: Dictionary untuk menyimpan data mahasiswa (nama sebagai key, nilai sebagai value).

Metode:

1. _init_(): Menginisialisasi atribut mahasiswa sebagai dictionary kosong.
2. tambah(nama, nilai): Menambahkan data mahasiswa.
3. tampilkan(): Menampilkan semua data mahasiswa.
4. hapus(nama): Menghapus data berdasarkan nama.
5. ubah(nama, nilai_baru): Memperbarui nilai mahasiswa.






