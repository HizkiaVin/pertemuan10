# DICTIONARY
• Membuat Dictionary
\
a = {} # dictionary kosong
\
a = {'n1': 100, 'n2': 20, 'n3': 7} # dictionary dengan key:value


• Mengakses Dictionary
\
print(a['n2']) # print element dengan key 'n2'
\
print(a.keys()) # print all key dari dictionary
\
print(a.values()) # print all value dari dictionary
\
print(a.items()) # print list of tuple(key, value) dari dictionary


• Mengubah element Dictionary
\
a['n2'] = 10 # merubah value untuk key 'n2'


• Menambah element Dictionary
\
a['n4'] = 15 # menambah item with key 'n4'


• Menghapus element Dictionary
\
del a[key]
\
a.pop() # bisa mendapatkan nilai kembali dari data yang telah dihapus


• Loop Dictionary
\
for item in a.items():
\
print(item) # print tuple (key, value)
\
print(item[0]) # print key item

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

