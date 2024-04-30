Membuat program kalkulator 
Nama : Muhammad Refky Wastio 
NIM : 090305820024020 

Disini saya menggunakan kode program sebagai berikut dengan perintah vi kalkulator.sh 
#!/bin/bash

# Fungsi untuk menambahkan
tambah() {
    echo $(($1 + $2))
}

# Fungsi untuk mengurangkan
kurang() {
    echo $(($1 - $2))
}

# Fungsi untuk mengalikan
kali() {
    echo $(($1 * $2))
}

# Fungsi untuk membagi
bagi() {
    echo $(($1 / $2))
}

# Meminta input operasi dari pengguna
echo "Masukkan operasi (contoh: 5 + 3):"
read operasi

# Memisahkan angka dan operator dari input
angka1=$(echo $operasi | cut -d' ' -f1)
operator=$(echo $operasi | cut -d' ' -f2)
angka2=$(echo $operasi | cut -d' ' -f3)

# Memeriksa operator dan melakukan operasi yang sesuai
case $operator in
    "+")
        tambah $angka1 $angka2
        ;;
    "-")
        kurang $angka1 $angka2
        ;;
    "*")
        kali $angka1 $angka2
        ;;
    "/")
        bagi $angka1 $angka2
        ;;
    *)
        echo "Operator tidak valid"
        ;;
esac

kemudian kita berikan akses untuk eksekusi kalkulator.sh dengan perintah chmod +x kalkulator.sh 
![alt text](https://github.com/MuhammadRefkyWastio/tugasPSO/blob/main/Gambarkalkulator/chmodkalk.jpg?raw=true)

kemudian kita tes apakah kalkulator tersebut berhasil 
![alt text](https://github.com/MuhammadRefkyWastio/tugasPSO/blob/main/Gambarkalkulator/teskalk.jpg?raw=true)

kalkulator telah dapat digunakan 
