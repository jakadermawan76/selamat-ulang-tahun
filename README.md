# selamat-ulang-tahun
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Selamat Ulang Tahun Pacarku</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #1e1e2f, #2b2b45);
      color: #ffffff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      text-align: center;
    }

    .card {
      background: rgba(255, 255, 255, 0.08);
      padding: 30px;
      border-radius: 20px;
      max-width: 400px;
      width: 90%;
      box-shadow: 0 10px 30px rgba(0,0,0,0.4);
    }

    h1 {
      font-size: 1.8rem;
      margin-bottom: 10px;
    }

    p {
      font-size: 1rem;
      opacity: 0.9;
    }

    input[type="date"] {
      margin-top: 15px;
      padding: 10px;
      width: 100%;
      border-radius: 10px;
      border: none;
      font-size: 1rem;
    }

    button {
      margin-top: 20px;
      padding: 12px;
      width: 100%;
      border-radius: 12px;
      border: none;
      background: #ff5f9e;
      color: white;
      font-size: 1rem;
      cursor: pointer;
    }

    button:hover {
      background: #ff3f87;
    }

    .link-box {
      margin-top: 25px;
      display: none;
    }

    a {
      color: #ffd1e6;
      text-decoration: none;
      font-weight: bold;
    }

    .error {
      color: #ff9aa2;
      margin-top: 15px;
    }
  </style>
</head>

<body>

  <div class="card">
    <h1>🎉 Selamat Ulang Tahun 🎉</h1>
    <p>Masukkan tanggal lahirmu untuk membuka hadiah spesial 💝</p>

    <input type="date" id="tanggal">

    <button onclick="cekTanggal()">BUKA JIKA SUDAH BERUMUR 23 TAHUN</button>

    <div class="error" id="error"></div>

    <div class="link-box" id="hadiah">
      <p>✨ Hadiah untukmu ✨</p>
      <a href="https://drive.google.com/file/d/1yZvB48q349gxhKzS11ar5sFNNX6eMoo-/view?usp=drivesdk" target="_blank">
        👉 Klik di sini untuk membukanya 💌
      </a>
    </div>
  </div>

  <script>
    function cekTanggal() {
      const input = document.getElementById("tanggal").value;
      const error = document.getElementById("error");
      const hadiah = document.getElementById("hadiah");

      if (input === "2003-01-19") {
        hadiah.style.display = "block";
        error.textContent = "";
      } else {
        hadiah.style.display = "none";
        error.textContent = "Tanggal lahir tidak sesuai 😢";
      }
    }
  </script>

</body>
</html>
