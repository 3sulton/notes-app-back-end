Nodemon
Tools pertama adalah nodemon, ia bisa dikatakan wajib digunakan selama proses pengembangan. Pasalnya, dengan tools ini kita tak perlu menjalankan ulang server ketika terjadi perubahan pada berkas JavaScript. Nodemon akan mendeteksi perubahan kode JavaScript dan mengeksekusi ulang secara otomatis.

Untuk menggunakannya, pasanglah package nodemon pada devDependencies dengan mengeksekusi perintah berikut di Terminal proyek:

npm install nodemon --save-dev

ESLint
Tools yang kedua adalah ESLint, ia dapat membantu atau membimbing Anda untuk selalu menuliskan kode JavaScript dengan gaya yang konsisten. Seperti yang Anda tahu, JavaScript tidak memiliki aturan yang baku untuk gaya penulisan kode, bahkan penggunaan semicolon. Karena itu, terkadang kita jadi tidak konsisten dalam menuliskannya.

npm install eslint --save-dev

Sebelum digunakan, Anda perlu melakukan konfigurasi terlebih dahulu. Caranya dengan menggunakan perintah berikut di Terminal proyek.

npx eslint --init

How would you like to use ESLint? -> To check, find problems, and enforce code style.
What type of modules does your project use? -> CommonJS (require/exports).
Which framework did you use? -> None of these. 
Does your project use TypeScript? -> N.
Where does your code run? -> Node (pilih menggunakan spasi).
How would you like to define a style for your project? -> Use a popular style guide.
Which style guide do you want to follow? -> (Anda bebas memilih, sebagai contoh pilih AirBnB).
What format do you want your config file to be in? -> JSON.
Would you like to …… (seluruh pertanyaan selanjutnya) -> Y.

Setelah membuat konfigurasi ESLint, selanjutnya kita gunakan ESLint untuk memeriksa kode JavaScript yang ada pada proyek. Namun sebelum itu, kita perlu menambahkan npm runner berikut di dalam berkas package.json:

"scripts": {
  "start": "nodemon server.js",
  "lint": "eslint ./"
},

Kriteria menyebutkan, properti id merupakan string dan harus unik, kita akan menggunakan bantuan library pihak ketiga untuk menghasilkan nilainya. nanoid merupakan salah satu library yang populer untuk menangani ini. Jadi, silakan pasang library tersebut dengan perintah.

npm install nanoid@3.x.x
Catatan: Pastikan Anda memasang nanoid dengan versi 3.x.x. Karena jika menggunakan versi terbaru, nanoid tidak dapat digunakan dengan format module CommonJS.

ERROR CORS
https://www.dicoding.com/academies/261/discussions/133122
"C:\Program Files\Google\Chrome\Application\chrome.exe" --user-data-dir="C:/Chrome dev session" --disable-web-security

security group -> firewall, ngatur inbound outbound jaringan. nambahin inbound untuk application port dan ssh port
ec2 -> bikin instance, bikin keypair buat connect ke instance, network setting pilih dari security group
