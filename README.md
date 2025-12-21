# javascript-course

hello! this is my journey starting to become a front-end developer

# Lesson 4: Review about HTML, CSS, and console.log

    console.log() berfungsi untuk menampilkan pesan pada inspect-console. sangat berfungsi ketika:
    1. Debugging/Testing
        Lebih cepat dan efisien menggunakan console.log daripada menampilkan apa yang di-debug melalui tampilan html. Kita bisa menuliskan pesan dalam console.log dan mengeceknya, apabila pesannya muncul berarti tidak ada masalah di kodenya, jika sebaliknya maka berarti ada masalah.
    2. Melihat isi variable atau data
        Ini sangat berguna apabila kita ingin tahu apakah sebuah data sesuai dengan harapan kita.
    3. Melacak alur program
        Kita juga dapat mengecek apakah alur program sudah benar atau belum tanpa menampilkannya di tampilan html, hanya di belakang saja (di console).

# Lesson 5: Variables

    Kenapa disitu kita pakai "let"? sebenarnya let digunakan jika variabel tersebut mendukung untuk bisa diubah saja, value yang digunakan di perintah selanjutnya adalah value yang paling terakhir disimpan (mengingat kuta menggunakan let, dimana value bisa diubah-ubah).

    Sedangkan jika kita menginginkan suatu variable dengan nilai yang tetap hingga akhir, kita bisa menggunakan 'const'.

    Nah, yang paling mungkin untuk digunakan biasanya dalah 'var', karena var pada javascript merepresentasikan 'variable', tapi itu biasa digunakan di javascript waktu dulu, sekarang jika tidak menggunakannya pun tidak masalah.

    Batasan untuk memberi nama pada variable:
    1. Tidak dapat menggunakan kata spesial/ tertentu
        Yaitu kata-kata yang sudah digunakan sebagai perintah tertentu di html/css/javascript.
        ex: let, int, dll. itu gabisa dipake buat nama variable
    2. Tidak dapat diawali dengan angka
        ex: let 2var = 5; itu ga bisa kalo nama variable nya kek gitu
    3. Tidak dapat menggunakan simbol-simbol
        ex: let name4&%@ = 6; itu juga tidak bisa

    eval(calculation) berguna untuk mengubah string yang ada di variable calculation menjadi angka. eval() adalah fungsi bawaan javascript yang akan menjalankan string seolah-olah itu kode JavaScript. Namun fungsi tersebut sebenarnya kurang aman untuk sekadar mengubah string menjadi angka, jadi ini untuk latihan saja.

# Lesson 6: Booleans and If-Statements

    Boolean adalah salah satu tipe dari value yang menyatakan "true" atau "false".

    Comparison Operator: >, <, >=, <=, ===, !==
    Perbedaan == dan === (umum digunakan di javascript):
    == tidak bisa mengidentifikasi perbedaan tipe data, 5 == '5.00' dianggap true, padahal satunya bertipe number dan satunya string. Dan harusnya 5 == '5.00' ini memiliki value false karena tipe datanya berbeda.

    Steps:
    1. Komputer adan memilih secara acak, menggunakan logika pengambilan angka acak dari Math.random() -> nilai akan disimpan di variable computerMove

       Logic pengambilan keputusan untuk komputer:
       Karena ada 3 pilihan (batu, kertas, gunting) maka kita akan
       bagi angka random (0-1) menjadi 3 bagian yaitu:
       0 - 1/3 untuk Rock
       1/3 - 2/3 untuk Paper
       2/3 - 1 untuk Scissors
       Kenapa sih kok pakai pecahan/desimal? itu karena di JavaScript selalu menghasilkan angka di antara 0 dan 1 (tidak termasuk 1). Mangkanya pakai pecahan/desimal gitu, biar universal/sesuai sama standart. Selain itu, 0-1 mudah dibagi/dipotong jadi pecahan sesuai jumlah pilihan.

        Scope: batas dari variable. Ketika keadaan seperti ini:
        onclick="
                const randomNumber =  Math.random();
                if(randomNumber >= 0 && randomNumber < 1/3){
                    const computerMove = 'rock';
                } else if(randomNumber >= 1/3 && randomNumber < 2/3){
                    const computerMove = 'paper';
                } else if(randomNumber >= 2/3 && randomNumber < 1){
                    const computerMove = 'scissors';
                }

                console.log(computerMove);
        NAH.. variable computerMove tidak bisa diakses di luar, karena dia
        dideklarasikan di dalam kondisi decision (variable yang
        dideklarasikan di dalam blok is/else + menggunakan const/let hanya
        dapat berlaku di dalam block scope itu sendiri), oleh karena itu
        ketika dijalankan, console mengeluarkan pesan error.
    2. Mengoversi pilihan dari komputer untuk disimpan di variable result
    3. Menampilkan hasilnya lewat pop-up

    Strategi untuk JavaScript:
    1. Temukan algoritma, jadi apa yang harus dilakukan untuk bisa menghasilkan output yang sesuai
    2. Ubah algoritma jadi code

    Tambahan: Truthy and Falsy value
    Falsy values: false, 0, '', NaN. undefined, null
    Selain yang ada di falsy values, itu adalah truthy values

# Lesson 7: Function

    Aturan untuk memberi nama function dan parameter:
    1. tidak dapat menggunakan nama spesial. ex: function()
    2. tidak bisa diawali dengan angka, ex:123functionname()
    3. tidak dapat diawali dengan spesial character, ex: %$functionname()
    PALING BAIK MENGGUNAKAN camelCase.

    Benefit menggunakan function dalam code adalah, kita bisa lebih efisien dalam pemrograman. Selain itu, kita tidak perlu menuliskan beberapa baris kode yang sama berulang kali. Dengan begitu hasilnya juga akan lebih konsisten.

    Return value dalam function dapat berupa seperti ini:
    return 2+2;
    return variable1;
    return Math.random();

    Fungsi diakhiri dengan return, jadi jika sudah dijalankan hingga baris return maka program otomatis langsung kembali ke awal, meskipun ada code di bawahnya return, itu tidak akan dieksekusi.
