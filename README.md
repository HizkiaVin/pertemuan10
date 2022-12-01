# DICTIONARY
**• Membuat Dictionary**
\
`a = {}`  dictionary kosong
\
`a = {'n1': 100, 'n2': 20, 'n3': 7}` dictionary dengan key:value


**• Mengakses Dictionary**
\
`print(a['n2'])` print element dengan key 'n2'
\
`print(a.keys())` print all key dari dictionary
\
`print(a.values())` print all value dari dictionary
\
`print(a.items())` print list of tuple(key, value) dari dictionary


**• Mengubah element Dictionary**
\
`a['n2'] = 10` merubah value untuk key 'n2'


**• Menambah element Dictionary**
\
`a['n4'] = 15` menambah item with key 'n4'


**• Menghapus element Dictionary**
\
`del a[key]`
\
`a.pop()` bisa mendapatkan nilai kembali dari data yang telah dihapus


**• Loop Dictionary**
\
`for item in a.items():`
\
`print(item)` print tuple (key, value)
\
`print(item[0]`) print key item

## Latihan 1
![latihan1 dict](https://user-images.githubusercontent.com/116176746/204817936-39cfb9b0-2427-4bab-b391-66e5b44f5db1.png)

```python
#membuat dictionary
kontak = {'Ari':'081267888', 'Dina' : '087677776'}

#mengakses dictionary
print("Menampilkan Kontak Ari")
print(" Ari     | ",kontak['Ari'])

print(30*"=")
#menambah element dictionary
print("Menambah kontak Riko")
kontak['Riko'] = '087654544'
print(" Riko    | ",kontak['Riko'])

print(30*"=")
#mengubah element dictionary
print("Mengubah kontak Dina")
kontak['Dina'] = '088999776'
print(" Dina    |",kontak['Dina'])
print(30*"=")

#mengakses semua dictionary
print("Tampilkan Semua Nama")
print(kontak.keys())
print(30*"=")
print("Tampilkan Semua Nomor")
print(kontak.values())
print(30*"=")
print("Tampilkan Semua Nama dan Nomor")
print(kontak.items())
print(30*"=")   

#mengubah element dicitonary
print("Hapus Kontak Dina")
del kontak['Dina']
print(kontak.items())
print(30*"=")
```

Output :

![output dict](https://user-images.githubusercontent.com/116176746/204818294-c0de2328-e823-4f8c-bf0e-fe6db2f51e33.png)

## Tugas Praktikum

Code:
```python
x = {}

while True:
    c = input("\n(T)ambah, (U)bah, (H)apus, (C)ari, (L)ihat, (K)eluar: ")

    if c.lower() == 't':
        print("Tambah Data")
        nama = input("Nama           : ")
        nim = int(input("NIM            : "))
        uts = int(input("Nilai UTS      : "))
        uas = int(input("Nilai UAS      : "))
        tugas = int(input("Nilai Tugas    : "))
        akhir = tugas*30/100 + uts*35/100 + uas*35/100
        x[nama] = nim, uts, uas, tugas, akhir

    elif c.lower() == 'u':
        print("Ubah Data")
        nama = input("Masukkan Nama  : ")
        if nama in x.keys():
            nim = int(input("NIM            : "))
            uts = int(input("Nilai UTS      : "))
            uas = int(input("Nilai UAS      : "))
            tugas = int(input("Nilai Tugas    : "))
            akhir = tugas * 30 / 100 + uts * 35 / 100 + uas * 35 / 100
            x[nama] = nim, uts, uas, tugas, akhir
        else:
            print("Nama {0} tidak ditemukan".format(nama))

    elif c.lower() == 'h':
        print("Hapus Data")
        nama = input("Masukkan Nama  : ")
        if nama in x.keys():
            del x[nama]
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))

    elif c.lower() == 'c':
        print("Cari Data")
        nama = input("Masukkan Nama : ")
        if nama in x.keys():
            print("="*73)
            print("|                             Daftar Mahasiswa                          |")
            print("="*73)
            print("| Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*73)
            print("| {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                  .format(nama, nim, uts, uas, tugas, akhir))
            print("="*73)
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))

    elif c.lower() == 'l':
        if x.items():
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            i = 0
            for z in x.items():
                i += 1
                print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                      .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
            print("=" * 78)
        else:
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            print("|                                TIDAK ADA DATA                              |")
            print("="*78)

    elif c. lower() == 'k':
        break

    else:
        print("Pilih menu yang tersedia")
```

output : 
![data1](https://user-images.githubusercontent.com/116176746/205081588-f929735c-34f0-4978-8b45-02b0b79a831c.png)

\

![data2](https://user-images.githubusercontent.com/116176746/205081582-84035c38-9fdb-44fa-a51b-2adc00658a82.png)


