# Lab8
## Membuat program dengan menggunakan class dan atribut nya didalam python

<p> Berikut ini adalah flowchatnya

![gambar1](ss/ssflowchart.1.jpg)

* dibawah ini code untuk mengimport, untuk mendapatkan clear system, pada system os

```python
from os import system
```
* dibawah ini adalah code untuk membuat class, yang berfungsi untuk menampung data mahasiswa beserta atributnya

```python
class mahasiswa:   
    nim=""
    nama=""
    tugas=""
    uts=""
    uas=""
    akhir=""
```
* dibawah ini adalah variable unntuk menampung list data dari object mahasiswa

```python
pilih=0
datasiswa=[]
```
* dibawah ini adalah program atau method untuk menampilkan daftar menu

```python
def menu():
    system("cls")
    print("Menu Aplikasi Data Mahasiswa");
    print("-"*43)
    print("1. Input Data Mahasiswa")
    print("2. Tampilkan Data Mahasiswa")
    print("3. Update Data Mahasiswa")
    print("4. Hapus Data Mahasiswa")
    print("5. Keluar Aplikasi")
    pilih= int(input("Masukan Pilihan Anda : "))
    if pilih == 1:
        pilih1()
        menu()
    elif pilih == 2:
        tampil()
        input("Kembali Menu Utama")
        menu()
    elif pilih == 3:
        index_update=-1
        tampil()
        id_edit = int(input("Input NIM yang akan diupdate "))
        for a in range(0, len(datasiswa)):
            if id_edit==datasiswa[a].nim:
                index_update=a
                break
        if (index_update > -1):
            print("INPUT DATA YANG DI UPDATE")
            siswa=mahasiswa()
            siswa.nim=(int(input("Msdukan NIM                      : ")))
            siswa.nama=(input("Masukan Nama Mahasiswa          : "))
            siswa.tugas=(float(input("Masukan Nilai Tugas              : ")))
            siswa.uts=(float(input("Masukan Nilai Uts              : ")))
            siswa.uas=(float(input("Masukan Nilai Uas              : ")))
            siswa.akhir=siswa.tugas*0.30+siswa.uts*0.35+siswa.uas*0.35
            datasiswa=[index_update]=siswa
            print("Berhasil Update Data Mahasiswa")
        else : print("NIM Tidak Ditemukan")
        input("Kembali Menu Utama")
        menu()
    elif pilih ==4:
        system("cls")
        tampil()
        index_update=-1
        id_hapus = int(input("Input NIM Yang Akan Dihapus"))
        for a in range (0, len(data)):
            if id_hapus==datasiswa[a].nim:
                index_delete = a
                break
        if(index_delete > -1):
            del datasiswa[index_delete]
            print("Data Telah Dihapus")
        else: 
            print("NIM Tidak Ditemukan")
            input("Kembali Menu Utama")
            menu()
            menu()
    elif pilih ==5 :
        exit()
```        
* dibawah ini adalah program untuk menambahkan data

```python
def pilih1():
    ulang = "Y"
    while ulang in("y","Y"):
        system("cls")
        siswabaru=mahasiswa()
        print("INPUT DATA MAHASISWA")
        siswabaru.nim=(int(input("Masukan NIM            : ")))
        siswabaru.nama=(input("Masukan Nama Mahasiswa : "))
        siswabaru.tugas=(float(input("Masukan Nilai Tugas    : ")))
        siswabaru.uts=(float(input("Masukan Nilai UTS      : ")))
        siswabaru.uas=(float(input("Masukan Nilai UAS      : ")))
        siswabaru.akhir=siswabaru.tugas*0.30 + siswabaru.uts*0.35 + siswabaru.uas*0.35
        datasiswa.append(siswabaru)
        ulang=input("Apakah Anda Ingin Mengulang (Y/T)? ")
menu()
```
* dibawah ini adalah code untuk menampilkan data yang sudah tersimpan, cara mengaksesnya dengan mengetikan angka 2 ditampilan menu

```python
def tampil():
    system("cls")
    print("DATA MAHASISWA")
    for data in datasiswa:
        print("Nim          : "+str(data.nim)) 
        print("Nama         : "+data.nama)
        print("Nilai Tugas  : "+str(data.tugas))
        print("Nilai UTS    : "+str(data.uts))
        print("Nilai UAS    : "+str(data.uas))
        print("Nilai Akhir  : "+str(data.akhir))
        print("-"*18)
```
* dibawah ini adalah program untuk menghapus data        

```python
 elif pilih ==4:
        system("cls")
        tampil()
        index_update=-1
        id_hapus = int(input("Input NIM Yang Akan Dihapus"))
        for a in range (0, len(data)):
            if id_hapus==datasiswa[a].nim:
                index_delete = a
                break
        if(index_delete > -1):
            del datasiswa[index_delete]
            print("Data Telah Dihapus")
        else: 
            print("NIM Tidak Ditemukan")
            input("Kembali Menu Utama")
            menu()
            menu()
```
* dibawah ini adalah program untuk keluar atau mengakhiri program            

```python
elif pilih ==5 :
        exit()
```
### Berikut program ketika dijlankan
* dibawah ini adalah tampilan menu ketika program dijalankan

![gambar2](ss/ss1.PNG)

* dibawah tampilan ketika memasukan no 1, apabila kita melanjutkan y maka akan melanjutkan dan menambahkan data, sedangkan jika kita melanjutkan T maka kita akan di arahkan ke menu utama

![gambar3](ss/ss_2.PNG)

* dibawah ini adalah tampilan, menampilkan keseluruhan data yang sudah disimpan

![gambar4](ss/ss3.PNG)

### Sekian dan Terima kasih