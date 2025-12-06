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
