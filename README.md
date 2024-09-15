<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Popup Message</title>
    <style>
        /* CSS untuk memposisikan pesan di tengah layar */
        .popup {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0.8); /* Mulai dengan skala kecil */
            background-color: rgba(51, 51, 51, 0.573);
            color: white;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 0 10px rgba(9, 91, 184, 0.822);
            opacity: 0; /* Mulai dengan opacity 0 */
            transition: opacity 0.6s ease-in-out, transform 0.6s ease-in-out; /* Transisi untuk opacity dan transform */
        }
        
        /* Latar belakang menggunakan gambar dari GitHub */
        body {
            margin: 0;
            padding: 0;
            background-image: url('https://raw.githubusercontent.com/syadamriski/tojuliani/main/IMG-20240810-WA0025.jpg');
            background-size: cover; /* Agar gambar mencakup seluruh halaman */
            background-position: center;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: Arial, sans-serif;
        }

        /* Animasi muncul popup */
        .popup.show {
            opacity: 1; /* Opacity menjadi 1 saat popup muncul */
            transform: translate(-50%, -50%) scale(1); /* Memperbesar popup ke skala penuh */
        }
    </style>
</head>
<body>

<div class="popup" id="popup">
    <br>Hai Ada Pesan Untuk Mu.<br>
    <br>Sebelum Lanjut, Puter dulu lagunya ya hehehe 😄<br>
    <br><button onclick="nextPopup()">Oke</button>
    <br><br>
    <!-- Tombol untuk memainkan audio dari GitHub -->
    <button onclick="playAudio()">KLIK LAGU</button>
</div>

<!-- Menambahkan elemen audio dengan link GitHub -->
<audio id="custom-audio">
    <source src="https://raw.githubusercontent.com/syadamriski/tojuliani/main/sempurna.m4a" type="audio/mp4">
    Your browser does not support the audio element.
</audio>

<script>
    // Variabel untuk melacak langkah pesan popup
    let popupStep = 1;

    // Fungsi untuk menampilkan popup berikutnya dengan konten yang berbeda
    function nextPopup() {
        const popup = document.getElementById('popup');
        popup.classList.remove('show'); // Hapus class show untuk memulai transisi keluar

        setTimeout(() => {
            if (popupStep === 1) {
                popup.innerHTML = 'Jull, Gua minta Maaf Terlepas Dari semua yg udh terjadi. <br><br><button onclick="nextPopup()">Oke</button>';
                popupStep++;
            } else if (popupStep === 2) {
                popup.innerHTML = 'Mungkin gua egois minta lu buat jgn pergi dri gua tpi gua gak bisa maksa lu,  karena kita cuma teman namun komitmen:). <br><br><button onclick="nextPopup()">Oke</button>';
                popupStep++;
            } else if (popupStep === 3) {
                popup.innerHTML = 'Yang Gua harap, lu gak ninggalin gua karena masalalu lu kembali ataupun orang baru yg jauh lebih dari gua.<br><br><button onclick="nextPopup()">Oke</button>';
                popupStep++;
            } else if (popupStep === 4) {
                popup.innerHTML = 'Mungkin gua orang terburuk yg pernah lu temui.<br><br><button onclick="nextPopup()">Oke</button>';
                popupStep++;
            } else if (popupStep === 5) {
                popup.innerHTML = 'tpi, yg lu harus tau, Rasa cinta gua Lebih dari apapun.<br><br><button onclick="nextPopup()">Oke</button>';
                popupStep++;
            } else if (popupStep === 6) {
                popup.innerHTML = 'Gua bener-bener minta maaf, mungkin cara ini bisa memaafkan gua:).<br><br><button onclick="nextPopup()">Oke</button>';
                popupStep++;
            } else if (popupStep === 7) {
                popup.innerHTML = 'karena ini gua bikin sendiri semua dari 0 hehehe.<br><br><button onclick="nextPopup()">Oke</button>';
                popupStep++;
            } else if (popupStep === 8) {
                popup.innerHTML = 'Jika lu butuh, kabarin gua ya hehehe.<br><br><button onclick="nextPopup()">Oke</button>';
                popupStep++;
            } else if (popupStep === 9) {
                popup.innerHTML = 'I love you more than anything.<br><br><button onclick="nextPopup()">Oke</button>';
                popupStep++;
            } else if (popupStep === 10) {
                popup.innerHTML = 'can i have you forever?.<br><br><button onclick="nextPopup()">Oke</button>';
                popupStep++;
            } else if (popupStep === 11) {
                popup.innerHTML = 'I love you with all my heart🤍🫶🏻.<br><br><button onclick="redirectToWhatsApp()">Oke</button>';
            }

            popup.classList.add('show'); // Tambahkan class show untuk memulai transisi masuk
        }, 500); // Delay agar transisi keluar selesai sebelum mengganti konten
    }

    // Fungsi untuk mengarahkan ke WhatsApp dengan pesan otomatis "TERIMAKASIH"
    function redirectToWhatsApp() {
        window.location.href = 'https://wa.me/6289519598121/?text=TERIMAKASIH'; // Tautan WhatsApp dengan pesan otomatis
    }

    // Fungsi untuk memainkan audio dari GitHub
    function playAudio() {
        const audio = document.getElementById('custom-audio');
        audio.play(); // Memutar audio ketika tombol diklik
    }

    // Tampilkan popup saat halaman dimuat
    document.getElementById('popup').classList.add('show');
</script>

</body>
</html>
