## Langkah-langkah untuk menerbitkan artikel

1. Clone repositori weblog.

    ``` bash
    $ git clone git@github.com:rails-id/weblog.git
    ```

2. Buat posting di direktori `_posts` disertai tanggal dan permalink.

    ``` bash
    $ vi _posts/YYYY-MM-DD-permalink.md
    ```

    atau kalian bisa melihat contoh di rake

    ``` bash
    $ rake
    ```

3. Tulis posting kalian.

    ``` yaml
    ---
    layout: post
    title: Your post title
    categories: [Releases,Edge]
    author: Nama yang ada di weblog.rubyonrails.org jika mengambil dari sumber eksternal
    translator: Nama Kamu
    published: true
    date: 2019-01-01 01:01:00 +07:00
    ---
    Konten posting dalam format Markdown. Direkomendasikan menggunakan Markdown (.md, .markdown) dan hindari penulisan HTML kecuali ada sesuatu yang ingin di embed
    ```

4. Commit dan push.

    ``` bash
    $ git add . && git commit -m "Pesan commit yang diinginkan" && git push
    ```

5. Tidak ada langkah selanjutnya, nanti akan ter-deploy secara otomatis.

## Pedoman Kontribusi

1. Jika ingin memasukkan gambar, buat salinan di direktori `assets` jika memungkinkan.

2. Jika ingin menambahkan kategori baru, tambahkan halaman indeks kategori juga.

3. Hindari penggunaan definisi atau kata dalam satu baris.

4. Jika kalian kurang paham penggunakan Markdown silakan bisa dipejari disini https://guides.github.com/features/mastering-markdown/
