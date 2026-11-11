steps:
  - name: Mengambil kode dari GitHub
    uses: actions/checkout@v4

  - name: Memeriksa file aplikasi
    run: |
      test -f index.html
      echo "File aplikasi ditemukan"

  - name: Menguji struktur HTML
    run: |
      grep -qi "<html" index.html
      grep -qi "</html>" index.html
      echo "Pengujian HTML berhasil"
