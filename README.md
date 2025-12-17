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
