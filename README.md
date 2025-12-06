# Praktikum7-Pertemuan-12

# Untuk menampilkan daftar nilai mahasiswa menggunakan program 

    class DaftarNilaiMahasiswa:
      def __init__(self):
          self.data_mahasiswa = {}

      def tambah(self, nama, nilai):
          """Method untuk menambah data mahasiswa baru."""
          if nama not in self.data_mahasiswa:
              self.data_mahasiswa[nama] = nilai
              print(f"Data {nama} berhasil ditambahkan.")
          else:
              print(f"Data {nama} sudah ada.")

      def tampilkan(self):
          """Method untuk menampilkan seluruh data mahasiswa."""
          if not self.data_mahasiswa:
              print("Daftar mahasiswa kosong.")
          else:
              print("Daftar Nilai Mahasiswa:")
              for nama, nilai in self.data_mahasiswa.items():
                  print(f"- Nama: {nama}, Nilai: {nilai}")

      def hapus(self, nama):
          """Method untuk menghapus data mahasiswa berdasarkan nama."""
          if nama in self.data_mahasiswa:
              del self.data_mahasiswa[nama]
              print(f"Data {nama} berhasil dihapus.")
          else:
              print(f"Data {nama} tidak ditemukan.")

      def ubah(self, nama, nilai_baru):
          """Method untuk mengubah data nilai mahasiswa berdasarkan nama."""
          if nama in self.data_mahasiswa:
              self.data_mahasiswa[nama] = nilai_baru
              print(f"Nilai {nama} berhasil diubah menjadi {nilai_baru}.")
          else:
              print(f"Data {nama} tidak ditemukan.")

      #Contoh penggunaan program:
      if __name__ == "__main__":
      app = DaftarNilaiMahasiswa()

      # Menambah data
      app.tambah("Budi", 85)
      app.tambah("Siti", 90)
      app.tambah("Budi", 80) # Menunjukkan data sudah ada

      # Menampilkan data
      app.tampilkan()

      # Mengubah data
      app.ubah("Budi", 88)
      app.ubah("Joko", 70) # Menunjukkan data tidak ditemukan

      # Menampilkan data setelah diubah
      app.tampilkan()

      # Menghapus data
      app.hapus("Siti")
      app.hapus("Joko") # Menunjukkan data tidak ditemukan

      # Menampilkan data setelah dihapus
      app.tampilkan()

# Penjelasan dari program diatas :
1. Konsep Dasar: Program ini dirancang menggunakan pendekatan berorientasi objek, di mana semua hal dianggap sebagai objek. Struktur utamanya adalah sebuah class yang berfungsi sebagai blueprint atau cetak biru untuk objek yang akan dibuat.
2. Definisi Kelas: Sebuah kelas akan dibuat, mungkin bernama DaftarNilaiMahasiswa atau sejenisnya, untuk mengorganisir data dan fungsionalitas terkait nilai mahasiswa.
3. Metode (Fungsi dalam Kelas): Di dalam kelas tersebut, akan didefinisikan beberapa metode menggunakan kata kunci def. Metode-metode ini adalah:
4. tambah(): Metode ini berfungsi untuk menambahkan data mahasiswa baru (misalnya nama dan nilai) ke dalam struktur data yang dikelola oleh kelas (seperti list atau dictionary).
5. tampilkan(): Metode ini akan menampilkan semua data mahasiswa yang tersimpan saat ini.
6. hapus(nama): Metode ini mengambil parameter nama untuk mengidentifikasi dan menghapus data mahasiswa yang sesuai dari daftar.
7. ubah(nama): Metode ini juga mengambil parameter nama untuk menemukan data mahasiswa tertentu dan memungkinkan pengguna untuk memperbarui informasinya (misalnya mengubah nilai).

# Hasil dari program diatas :

<img width="621" height="538" alt="Screenshot 2025-12-06 222035" src="https://github.com/user-attachments/assets/9d794633-be2e-45e0-a17b-050ce8eea54b" />

# FlowChart
<img width="853" height="1280" alt="image" src="https://github.com/user-attachments/assets/c0bf3ac7-1bbe-4ef5-ada2-0e5587599626" />




