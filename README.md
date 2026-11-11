<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Kampus - CI/CD DevOps</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background: #f1f5f9;
            color: #1e293b;
        }

        header {
            background: #164e8a;
            color: white;
            text-align: center;
            padding: 30px;
        }

        nav {
            background: #0f3155;
            padding: 15px;
            text-align: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 10px;
        }

        .container {
            max-width: 1100px;
            margin: 30px auto;
            padding: 20px;
        }

        .welcome, .card, .diagram {
            background: white;
            padding: 25px;
            border-radius: 10px;
            margin-bottom: 20px;
            box-shadow: 0 3px 8px #00000012;
        }

        .cards {
            display: grid;
            grid-template-columns:
                repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .card {
            text-align: center;
        }

        .card h3 {
            color: #164e8a;
            margin-bottom: 12px;
        }

        .card p {
            margin-bottom: 15px;
        }

        button {
            background: #164e8a;
            color: white;
            padding: 10px 18px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background: #0f3155;
        }

        .diagram {
            text-align: center;
        }

        .step {
            background: #164e8a;
            color: white;
            padding: 15px;
            margin: 10px auto;
            max-width: 350px;
            border-radius: 7px;
        }

        .arrow {
            font-size: 25px;
            color: #164e8a;
        }

        .success {
            background: #15803d;
        }

        footer {
            background: #0f3155;
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 40px;
        }

        @media(max-width: 600px) {
            nav a {
                display: inline-block;
                margin: 7px;
            }
        }
    </style>
</head>

<body>

<header>
    <h1>DIGITAL KAMPUS</h1>
    <p>Sistem Informasi Akademik Universitas</p>
</header>

<nav>
    <a href="#beranda">Beranda</a>
    <a href="#pendaftaran">Pendaftaran</a>
    <a href="#krs">KRS</a>
    <a href="#nilai">Nilai</a>
    <a href="#ukt">Pembayaran UKT</a>
    <a href="#cicd">Diagram CI/CD</a>
</nav>

<div class="container">

    <section class="welcome" id="beranda">
        <h2>Selamat Datang di Digital Kampus</h2>
        <br>
        <p>
            Digital Kampus merupakan aplikasi berbasis web
            yang membantu mahasiswa mengakses informasi
            akademik dengan lebih mudah dan praktis.
        </p>
    </section>

    <h2>Layanan Akademik</h2>
    <br>

    <div class="cards">

        <div class="card" id="pendaftaran">
            <h3>Pendaftaran Mahasiswa</h3>
            <p>Informasi pendaftaran mahasiswa baru.</p>
            <button onclick="tampilkanPesan('Pendaftaran Mahasiswa')">
                Lihat Informasi
            </button>
        </div>

        <div class="card" id="krs">
            <h3>Pengisian KRS</h3>
            <p>Informasi rencana studi mahasiswa.</p>
            <button onclick="tampilkanPesan('Pengisian KRS')">
                Lihat Informasi
            </button>
        </div>

        <div class="card" id="nilai">
            <h3>Pengumuman Nilai</h3>
            <p>Informasi hasil nilai akademik mahasiswa.</p>
            <button onclick="tampilkanPesan('Pengumuman Nilai')">
                Lihat Informasi
            </button>
        </div>

        <div class="card" id="ukt">
            <h3>Pembayaran UKT</h3>
            <p>Informasi pembayaran uang kuliah.</p>
            <button onclick="tampilkanPesan('Pembayaran UKT')">
                Lihat Informasi
            </button>
        </div>

    </div>

    <br>

    <section class="diagram" id="cicd">
        <h2>DIAGRAM CI/CD DEVOPS</h2>
        <br>

        <div class="step">1. Developer</div>
        <div class="arrow">↓</div>

        <div class="step">2. GitHub Repository</div>
        <div class="arrow">↓</div>

        <div class="step">3. Commit dan Push</div>
        <div class="arrow">↓</div>

        <div class="step">4. GitHub Actions</div>
        <div class="arrow">↓</div>

        <div class="step">5. Continuous Integration (CI)</div>
        <div class="arrow">↓</div>

        <div class="step">6. Testing Aplikasi</div>
        <div class="arrow">↓</div>

        <div class="step success">7. Testing Berhasil</div>
        <div class="arrow">↓</div>

        <div class="step">8. Continuous Deployment (CD)</div>
        <div class="arrow">↓</div>

        <div class="step">9. GitHub Pages</div>
        <div class="arrow">↓</div>

        <div class="step success">10. Website Berhasil Dipublikasikan</div>
    </section>

    <section class="welcome">
        <h2>Penjelasan CI/CD</h2>
        <br>

        <p>
            <b>Continuous Integration (CI)</b> adalah proses
            pengujian kode secara otomatis setiap kali
            developer melakukan perubahan pada repository.
        </p>

        <br>

        <p>
            <b>Continuous Deployment (CD)</b> adalah proses
            mempublikasikan aplikasi secara otomatis setelah
            pengujian berhasil dilakukan.
        </p>

        <br>

        <p>
            GitHub Actions digunakan untuk menjalankan
            proses CI/CD, sedangkan GitHub Pages digunakan
            untuk mempublikasikan website.
        </p>
    </section>

</div>

<footer>
    <p>&copy; 2026 Digital Kampus | Implementasi DevOps CI/CD</p>
</footer>

<script>
    function tampilkanPesan(fitur) {
        alert("Anda memilih fitur " + fitur);
    }
</script>

</body>
</html>
