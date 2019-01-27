## Langkah Untuk Menerbitkan Artikel

- Clone repositori weblog.

    ``` bash
    $ git clone git@github.com:rails-id/weblog.git
    ```

- Buat posting di direktori `_posts` disertai tanggal dan permalink.

    ``` bash
    $ vi _posts/YYYY-MM-DD-permalink.md
    ```
    tentang perintah lainnya kalian bisa lihat di perintah rake

    ``` bash
    $ rake
    ```

- Selanjutnya lengkapi postingan di file yang baru saja ditambahkan dan gunakan text editor favorit kalian.

    ``` markdown
    ---
    layout: post
    title: Your post title
    categories: [Releases, Edge]
    author: Nama yang ada di weblog.rubyonrails.org jika mengambil dari sumber eksternal
    translator: Nama Kamu
    published: true
    date: 2019-01-01 01:01:00 +07:00
    ---
    Konten posting dalam format Markdown. Direkomendasikan menggunakan Markdown (.md, .markdown) dan hindari penulisan HTML kecuali ada sesuatu yang ingin di embed
    ```

- Commit dan push.

    ``` bash
    $ git add . && git commit -m "Pesan commit yang diinginkan" && git push
    ```

- Tidak ada langkah selanjutnya, nanti akan ter-deploy secara otomatis.

## Pedoman Kontribusi

- Jika ingin memasukkan gambar, buat salinan di direktori `assets` jika memungkinkan.
- Jika ingin menambahkan kategori baru, tambahkan halaman indeks kategori juga.
- Hindari penggunaan definisi atau kata dalam satu baris.
- Jika kalian kurang paham penggunakan Markdown silakan bisa pelajari di [Mastering Markdown](https://guides.github.com/features/mastering-markdown/).
