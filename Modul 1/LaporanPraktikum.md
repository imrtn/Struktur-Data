# <h1 align="center">Laporan Praktikum Modul 1 - Codeblocks IDE & Pengenalan Bahas C++ (Bagian Pertama)</h1>

<p align="center">Imroatun Sholikha - 109082500111</p>

## Dasar Teori

C++ merupakan bahasa pemrograman yang menggunakan struktur program dengan fungsi main() sebagai bagian utama program. Program C++ umumnya diawali dengan penggunaan header file dan preprocessor #include untuk memasukkan pustaka yang diperlukan. [1][2]

Tipe data digunakan untuk menentukan jenis data yang disimpan oleh suatu variabel. Dalam C++, tipe data dasar yang digunakan antara lain integer untuk bilangan bulat, float untuk bilangan pecahan, char untuk karakter, dan string untuk kumpulan karakter. [1][2]

Variabel harus dideklarasikan sebelum digunakan. Input dapat diberikan menggunakan cin, sedangkan output dapat ditampilkan menggunakan cout. Statement dalam C++ diakhiri dengan titik koma (;). [1]

Operator aritmatika digunakan untuk melakukan operasi penjumlahan, pengurangan, perkalian, dan pembagian. C++ juga menyediakan struktur percabangan dan perulangan untuk mengatur alur eksekusi program. [1][2]

#### A. Code::Blocks dan C++

Code::Blocks digunakan untuk menulis, melakukan compile, dan menjalankan program C++. Struktur dasar C++ terdiri dari library, variabel, dan fungsi `main()`.

#### B. Input, Output, dan Operator

`cin` digunakan untuk menerima input, sedangkan `cout` untuk menampilkan output. Operator digunakan untuk melakukan berbagai operasi pada data.

#### C. Kondisional, Perulangan, Struct, dan Fungsi

Kondisional digunakan untuk memilih proses, perulangan untuk menjalankan proses berulang, struct untuk mengelompokkan data, dan fungsi untuk membagi program menjadi beberapa bagian.


## Guided

### 1. 

```C++
#include<iostream>
using namespace std;
int main(){
    int w, x, y; float z;
    x = 7; y = 3; w = 1;
    z = (x + y)/(y + w);
    cout << "nilai z = "<< z << endl;
    return 0;
}
```

Program ini digunakan untuk menghitung empat operasi dasar, yaitu penjumlahan, pengurangan, perkalian, dan pembagian dari dua bilangan yang dimasukkan pengguna.

### 2. 

```C++
#include <iostream>
using namespace std;
int main(){
    int r = 10;
    int s;
    s=10 + ++r;
    cout<< "Nilai r= "<<r<<endl;
    cout<< "Nilai s= "<<s<<endl;
    return 0;
}
```

Kode ini menggunakan pre-increment ++r, sehingga nilai r ditambah 1 terlebih dahulu menjadi 11, lalu digunakan untuk menghitung s.

### 3. 

```C++
#include <iostream>
using namespace std;
int main(){
    double tot_pembelian, diskon;
    cout << " total pembelian : Rp";
    cin >> tot_pembelian;
    diskon = 0;
    if (tot_pembelian >= 100000)
        diskon = 0.05 * tot_pembelian;
    else
        diskon = 0;
    cout << "besar diskon = Rp"<<diskon;
}
```

Program ini digunakan untuk menghitung diskon pembelian. Jika total pembelian minimal Rp100.000, maka mendapat diskon 5%; jika kurang, tidak mendapat diskon.

### 4. 

```C++
#include <iostream>
using namespace std;
int main(){
    int kode_hari;
    puts("Menentukan hari kerja/libur\n");
    puts("1=senin 3=rabu 5=jumat 7=minggu ");
    puts("2=selasa 4=kamis 6=sabtu ");
    cin >> kode_hari;
    switch (kode_hari){
        case 1:
        case 2:
        case 3:
        case 4:
        case 5:
            cout << ("Hari kerja");
            break;
        case 6:
        case 7:
            cout << ("Hari libur");
            break;
        default :
            cout << ("code masukan salah") << endl;
    }
    return 0;
}
```

Program ini digunakan untuk menentukan apakah suatu kode hari termasuk hari kerja atau hari libur. switch digunakan untuk mengelompokkan kode 1–5 sebagai hari kerja, sedangkan 6–7 sebagai hari libur..

### 5. 

```C++
#include <iostream>
using namespace std;
int main(){
    int i = 1;
    int jum;
    cout<<"masukan banyak baris: ";
    cin>>jum;
    do{
        cout << "baris ke-"<< (i+1)<<endl;
        i++;
    } while (i < jum);
    return 0;
}
```

Program ini menggunakan perulangan do-while untuk menampilkan nomor baris sesuai jumlah yang dimasukkan. Perulangan tetap dijalankan minimal satu kali sebelum kondisi i < jum diperiksa.

### 6. 

```C++
#include <iostream>
using namespace std;
int main(){
    int i = 1;
    int jum;
    cout<<"masukan banyak baris: ";
    cin>>jum;
    while(i <= jum){
        cout << "baris ke-"<< i << endl;
        i++;
    }
    return 0;
}
```

Program ini menggunakan perulangan while untuk menampilkan nomor baris dari 1 sampai jumlah yang dimasukkan.

### 7. 

```C++
#include <iostream>
#define MAX 5
using namespace std;
int main(){
    int i;
    struct data{
        char nama[40];
        int nilai;
    };
    data siswa[MAX];
    for (i = 0; i < MAX; i++){
        cout << "masukkan data ke-"<<i+1<<endl;
        cout << "nama = ";
        cin >> siswa[i].nama;
        cout << "nilai = ";
        cin >> siswa[i].nilai;
    }
    cout << "\ndata siswa\n";
    cout << "=======";
    for (i = 0; i < MAX; i++){
        cout << "\n \ndata ke-"<<i+1;
        cout << "\n \nnama = "<<siswa[i].nama;
        cout << "\n \nnilai = "<<siswa[i].nilai;
    }
    return 0;
}
```

Program ini menggunakan **struct** untuk menyimpan nama dan nilai beberapa siswa. Data dimasukkan menggunakan perulangan `for`, kemudian ditampilkan kembali setelah semua data selesai dimasukkan.

### 8.

```C++
#include <iostream>
using namespace std;

float ctof(float celcius);
int main() {
    float celcius, fahrenheit;
    cout <<"nilai Celcius? ";
    cin >> celcius;
    fahrenheit = ctof(celcius);
    cout<<celcius<<" Celcius adalah "<<fahrenheit<<" Fahrenheit"<<endl;
    return 0;
}

float ctof(float celcius){
    return (celcius * 1.8) + 32;
}
```

Program ini menggunakan fungsi ctof() untuk mengubah suhu dari Celcius ke Fahrenheit. Nilai Celcius dimasukkan oleh pengguna, lalu hasil konversinya ditampilkan.


## Unguided

### 1. Buatlah program yang menerima input-an dua buah bilangan betipe float, kemudian memberikan output-an hasil penjumlahan, pengurangan, perkalian, dan pembagian dari dua bilangan tersebut.

```C++
#include <iostream>
using namespace std;

int main() {
    float a, b;
    
    cout << "Input dua bilangan: ";
    cin >> a >> b;

    cout << "Tambah = " << a + b << endl;
    cout << "Kurang = " << a - b << endl;
    cout << "Kali = " << a * b << endl;
    cout << "Bagi = " << a / b << endl;

    return 0;
}
```

### Output Unguided 1 :

##### Output 1

![Screenshot Output Unguide1](https://github.com/imrtn/Struktur-Data/blob/b6e098e1fc265677b745836ef8ff0b40ec2df2ba/Modul%201/Output/unguide1.png)

Program mendeklarasikan dua variabel bertipe float untuk menerima dua bilangan. Input dibaca menggunakan cin. Setelah itu, operator aritmatika digunakan untuk menghitung penjumlahan, pengurangan, perkalian, dan pembagian, lalu hasilnya ditampilkan menggunakan cout.

### 2. Buatlah sebuah program yang menerima masukan angka dan mengeluarkan output nilai angka tersebut dalam bentuk tulisan. Angka yang akan di-input-kan user adalah bilangan bulat positif mulai dari 0 s.d 100

```C++
#include <iostream>
using namespace std;

int main() {
    int angka;
    string satuan[] = {
        "nol", "satu", "dua", "tiga", "empat",
        "lima", "enam", "tujuh", "delapan", "sembilan"
    };

    cout << "Masukkan angka (0-100): ";
    cin >> angka;

    cout << angka << ": ";

    if (angka == 0) {
        cout << "nol";
    } else if (angka < 10) {
        cout << satuan[angka];
    } else if (angka == 10) {
        cout << "sepuluh";
    } else if (angka == 11) {
        cout << "sebelas";
    } else if (angka < 20) {
        cout << satuan[angka - 10] << " belas";
    } else if (angka < 100) {
        cout << satuan[angka / 10] << " puluh";
        if (angka % 10 != 0) {
            cout << " " << satuan[angka % 10];
        }
    } else {
        cout << "seratus";
    }

    cout << endl;

    return 0;
}
```

### Output Unguided 2 :

##### Output 1

![Screenshot Output Unguide2](https://github.com/imrtn/Struktur-Data/blob/b6e098e1fc265677b745836ef8ff0b40ec2df2ba/Modul%201/Output/unguide2.png)

Program menerima bilangan bulat 0 sampai 100. Percabangan if-else digunakan untuk membedakan angka satuan, belasan, puluhan, dan angka 100. Array string satuan menyimpan nama angka dari nol sampai sembilan sehingga nama angka dapat dipanggil berdasarkan indeksnya.

### 3. Buatlah program yang dapat memberikan input dan output sbb.

```C++
#include <iostream>
using namespace std;

int main() {
    int n;
    
    cout << "Input: ";
    cin >> n;
    
    cout << "Output:\n";

    for (int i = n; i >= 0; --i) {

        for (int j = 0; j < n - i; ++j)
            cout << "  ";

        for (int j = i; j > 0; --j)
            cout << j << " ";

        cout << "*";

        for (int j = 1; j <= i; ++j)
            cout << " " << j;

        cout << endl;
    }

    return 0;
}
```

### Output Unguided 3 :

##### Output 1

![Screenshot Output Unguide3](https://github.com/imrtn/Struktur-Data/blob/b6e098e1fc265677b745836ef8ff0b40ec2df2ba/Modul%201/Output/unguide1.png)

Program menerima nilai n sebagai jumlah awal pola. Perulangan for pertama mengatur jumlah baris dari n sampai 1. Perulangan kedua mencetak angka secara menurun dari nilai baris menuju 1, kemudian karakter * dicetak sebagai pembatas. Perulangan ketiga mencetak angka secara menaik dari 1 sampai nilai baris. Setelah seluruh baris selesai, program mencetak satu karakter * pada baris terakhir.

## Kesimpulan

Berdasarkan latihan yang dikerjakan, konsep dasar C++ dapat digunakan untuk membuat program yang menerima input dan menghasilkan output sesuai kebutuhan. Latihan pertama menerapkan tipe data float dan operator aritmatika. Latihan kedua menerapkan input, string, array, dan percabangan untuk mengubah angka menjadi tulisan. Latihan ketiga menerapkan perulangan bersarang (nested loop) untuk membentuk pola output Mirror.

## Referensi

[1] Triase. (2020). Diktat Edisi Revisi: STRUKTUR DATA. Medan: Universitas Islam Negeri Sumatera Utara Medan.
[2] Indahyati, Uce., Rahmawati Yunianita. (2020). "BUKU AJAR ALGORITMA DAN PEMROGRAMAN DALAM BAHASA C++". Sidoarjo: Umsida Press. Diakses pada 10 Maret 2024 melalui https://doi.org/10.21070/2020/978-623-6833-67-4.
