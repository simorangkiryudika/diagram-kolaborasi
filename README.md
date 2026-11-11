
name: DevOps Digital Kampus

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  testing:
    name: Testing Aplikasi
    runs-on: ubuntu-latest

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

  deployment:
    name: Deployment ke GitHub Pages
    needs: testing
    if: github.event_name == 'push' && github.ref == 'refs/heads/main'
    runs-on: ubuntu-latest

    environment:
      name: github-pages
      url: ${{ steps.deploy.outputs.page_url }}

    steps:
      - name: Mengambil kode
        uses: actions/checkout@v4

      - name: Mengatur GitHub Pages
        uses: actions/configure-pages@v5

      - name: Menyiapkan file website
        uses: actions/upload-pages-artifact@v3
        with:
          path: .

      - name: Deploy aplikasi
        id: deploy
        uses: actions/deploy-pages@v4
