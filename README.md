# project_UAS
# project uas
NAMA : SENA SANIRA
NIM : 312310606
KELAS : TI.23.A.6
MATA KULIAH : BAHASA PEMROGRAMAN

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

KODE PEMROGMAN

![gambar](UAS/UAS.png)


# Dictionary berisi opsi makanan dan harganya
menu = {
    'Nasi bakar': 20000,
    'Mie rebus telor': 12000,
    'Ayam bakar': 20000,
    'baso aci' : 13000,
    'Es Teh': 5000,
    'Es Jeruk': 10000,
    'Air Mineral': 5000
}

def tampilkan_menu():
    print("Menu Makanan/Minuman:")
    for item, harga in menu.items():
        print(f"{item}: Rp {harga}")

def hitung_total(harga, jumlah):
    return harga * jumlah

def main():
    pesanan = {}

    while True:
        tampilkan_menu()
        pilihan = input("Masukkan nama makanan/minuman yang ingin dipesan (ketik : 'sudah' untuk menampilkan struk): ")

        if pilihan.lower() == 'sudah':
            break

        if pilihan in menu:
            jumlah = int(input(f"Masukkan jumlah {pilihan}: "))
            harga_total = hitung_total(menu[pilihan], jumlah)
            pesanan[pilihan] = {'jumlah': jumlah, 'harga_total': harga_total}
        else:
            print("Menu tidak ada. Silakan pilih menu yang tersedia.")

    # Tampilkan struk pembelian
    print("\nStruk Pembelian:")
    total_pembelian = 0
    for item, detail in pesanan.items():
        print(f"{item} x{detail['jumlah']}: Rp {detail['harga_total']}")
        total_pembelian += detail['harga_total']

    print(f"\nTotal Pembelian: Rp {total_pembelian}")

if __name__ == "__main__":
    # Your code here
    # This block will be executed when the script is run directly

    main()

    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  
   Nasi bakar: Rp 20000
Mie rebus telor: Rp 12000
Ayam bakar: Rp 20000
baso aci: Rp 13000
Es Teh: Rp 5000
Es Jeruk: Rp 10000
Air Mineral: Rp 5000
Masukkan nama makanan/minuman yang ingin dipesan (ketik : 'sudah' untuk menampilkan struk): sudah

Struk Pembelian:

Total Pembelian: Rp 0
PS C:\Users\senas\OneDrive\Desktop\uas pemrograman>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------!

LANGKAH LANGKAN PENJELASAN PEMROGRAMAN

1. Menyiapkan daftar menu dan harga
Dalam contoh ini, kami menggunakan struktur data dictionary untuk menyimpan menu dan harganya. Setiap item menu adalah kunci dalam dictionary, dan nilainya adalah harga masing-masing item.
2. Menampilkan menu kepada pengguna
Dibuatlah fungsi display_menu() yang mengiterasi melalui dictionary menu untuk menampilkan pilihan makanan/minuman kepada pengguna.
3. Mengambil input pilihan pengguna
Di dalam fungsi utama main(), pengguna diminta untuk memilih menu makanan/minuman. Perulangan while digunakan untuk memungkinkan pengguna memasukkan pilihan secara berulang.
4. Menghitung total harga pesanan
Dibuatlah fungsi calculate_total() yang menerima daftar pilihan pesanan dan menghitung total harga berdasarkan menu yang dipilih.
5. Menampilkan struk pembelian
Setelah pengguna selesai memilih, program akan menampilkan struk pembelian berdasarkan pesanan yang dipilih.

