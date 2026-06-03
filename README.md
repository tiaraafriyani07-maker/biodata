<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>Tiara Afriyani | Student Profile - IPS & Petualang Kuliner</title>
    <!-- Font Awesome 6 (free) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            background: linear-gradient(145deg, #f7ede3 0%, #fee9db 100%);
            font-family: 'Poppins', 'Segoe UI', system-ui, -apple-system, 'Quicksand', sans-serif;
            padding: 2rem 1.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Container utama seperti kartu elegan */
        .profile-card {
            max-width: 1000px;
            width: 100%;
            margin: 0 auto;
            background: rgba(255, 255, 245, 0.96);
            backdrop-filter: blur(2px);
            border-radius: 64px;
            box-shadow: 0 30px 45px -20px rgba(0,0,0,0.3), 0 0 0 1px rgba(255,215,180,0.6), 0 8px 20px rgba(0,0,0,0.1);
            overflow: hidden;
            transition: all 0.3s ease;
        }

        /* Bagian header dengan avatar dan nama */
        .profile-header {
            background: linear-gradient(135deg, #f0a88b, #e98e6b);
            padding: 2rem 2rem 1.8rem 2rem;
            text-align: center;
            color: white;
            position: relative;
        }

        .avatar {
            background: #fff6e8;
            width: 110px;
            height: 110px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1rem auto;
            box-shadow: 0 15px 25px rgba(0,0,0,0.2);
            border: 4px solid #ffefcf;
        }

        .avatar i {
            font-size: 4.5rem;
            color: #cb6e2e;
            text-shadow: 2px 2px 0 #ffcf9a;
        }

        .profile-header h1 {
            font-size: 2.4rem;
            letter-spacing: 1px;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
            margin-bottom: 0.25rem;
        }

        .school-badge {
            background: #ffefcfcc;
            backdrop-filter: blur(4px);
            display: inline-block;
            padding: 0.4rem 1.4rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            margin-top: 0.6rem;
            color: #914d1f;
        }

        /* quote area - moto peluang */
        .quote-section {
            background: #fffaf2;
            padding: 1.5rem 2rem;
            text-align: center;
            border-bottom: 2px dashed #ffcfaa;
        }

        .quote-text {
            font-size: 1.3rem;
            font-style: italic;
            font-weight: 500;
            color: #b45f2b;
            background: #fff1e2;
            display: inline-block;
            padding: 0.6rem 2rem;
            border-radius: 60px;
            box-shadow: inset 0 1px 4px #ffeee1, 0 5px 10px rgba(0,0,0,0.03);
        }

        .quote-text i {
            margin: 0 6px;
            color: #f19b4b;
        }

        /* konten biodata 2 kolom */
        .biodata-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.8rem;
            padding: 2rem 2rem 1.8rem;
        }

        .info-card {
            background: #ffffffdb;
            border-radius: 40px;
            padding: 1.4rem 1.8rem;
            box-shadow: 0 10px 18px rgba(134, 81, 36, 0.08);
            transition: 0.2s;
            border: 1px solid #ffedd9;
        }

        .info-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1.2rem;
            color: #a75521;
            display: flex;
            align-items: center;
            gap: 12px;
            border-left: 5px solid #f7b163;
            padding-left: 15px;
        }

        .info-item {
            display: flex;
            align-items: baseline;
            margin-bottom: 1rem;
            flex-wrap: wrap;
            gap: 8px;
            border-bottom: 1px dashed #ffe1bf;
            padding-bottom: 0.6rem;
        }

        .info-label {
            width: 100px;
            font-weight: 700;
            color: #b96f3b;
            font-size: 0.9rem;
        }

        .info-value {
            flex: 1;
            font-weight: 500;
            color: #4e2d18;
            font-size: 1rem;
        }

        .hobby-list {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 5px;
        }
        .hobby-badge {
            background: #fae6d4;
            border-radius: 50px;
            padding: 5px 14px;
            font-size: 0.85rem;
            font-weight: 500;
            color: #b25922;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }
        .hobby-badge i {
            font-size: 0.9rem;
            color: #df7e42;
        }

        /* tombol link proyek */
        .button-wrapper {
            padding: 0rem 2rem 2rem 2rem;
            text-align: center;
        }

        .project-btn {
            background: linear-gradient(95deg, #ffa559, #ff8c42);
            border: none;
            padding: 1rem 2.2rem;
            border-radius: 60px;
            font-size: 1.2rem;
            font-weight: bold;
            color: white;
            cursor: pointer;
            transition: all 0.25s ease;
            display: inline-flex;
            align-items: center;
            gap: 14px;
            box-shadow: 0 10px 15px -6px #c46f2e;
            text-decoration: none;
            font-family: inherit;
            letter-spacing: 1px;
        }

        .project-btn i {
            font-size: 1.5rem;
            transition: transform 0.2s;
        }

        .project-btn:hover {
            background: linear-gradient(95deg, #ff8c42, #ff7826);
            transform: translateY(-3px);
            box-shadow: 0 16px 22px -8px #b75d24;
        }

        .project-btn:active {
            transform: translateY(2px);
        }

        /* footer kecil */
        .footer-note {
            background: #fef1e4;
            text-align: center;
            padding: 0.9rem;
            font-size: 0.75rem;
            color: #bc7b48;
            border-top: 1px solid #ffdfbf;
        }

        /* Responsive */
        @media (max-width: 700px) {
            .biodata-container {
                grid-template-columns: 1fr;
                gap: 1rem;
                padding: 1.5rem;
            }
            .profile-header h1 {
                font-size: 1.8rem;
            }
            .quote-text {
                font-size: 1rem;
                padding: 0.4rem 1rem;
            }
            .project-btn {
                font-size: 1rem;
                padding: 0.8rem 1.8rem;
            }
            .info-label {
                width: 85px;
            }
        }

        /* animasi subtle */
        @keyframes fadeSlide {
            0% { opacity: 0; transform: translateY(18px);}
            100% { opacity: 1; transform: translateY(0);}
        }
        .profile-card {
            animation: fadeSlide 0.5s ease-out;
        }

        /* tambahan style untuk genre badge */
        .genre-badge {
            background: #f9ddc2;
            border-radius: 30px;
            padding: 4px 14px;
            font-size: 0.85rem;
            font-weight: 600;
            color: #a74817;
            display: inline-block;
            margin-right: 10px;
            margin-bottom: 6px;
        }
        .genre-badge i {
            margin-right: 6px;
        }
    </style>
</head>
<body>

<div class="profile-card">
    <!-- Header dengan avatar dan nama utama -->
    <div class="profile-header">
        <div class="avatar">
            <i class="fas fa-user-graduate"></i>
        </div>
        <h1>Tiara Afriyani</h1>
        <div class="school-badge">
            <i class="fas fa-school"></i> SMAN 15 JAKARTA
        </div>
    </div>

    <!-- Motto / kutipan favorit -->
    <div class="quote-section">
        <div class="quote-text">
            <i class="fas fa-quote-left"></i> 
            Peluang tidak datang begitu saja. Kamulah yang harus menciptakannya.
            <i class="fas fa-quote-right"></i>
        </div>
    </div>

    <!-- Biodata detail dalam dua kolom (jurusan IPS & hobi + genre petualang & kuliner) -->
    <div class="biodata-container">
        <!-- Kolom Kiri: Data Pribadi & Jurusan -->
        <div class="info-card">
            <h3><i class="fas fa-id-card"></i> Profil Diri</h3>
            <div class="info-item">
                <span class="info-label">Nama Lengkap</span>
                <span class="info-value">Tiara Afriyani</span>
            </div>
            <div class="info-item">
                <span class="info-label">Usia</span>
                <span class="info-value">17 Tahun</span>
            </div>
            <div class="info-item">
                <span class="info-label">Kelas</span>
                <span class="info-value">X5</span>
            </div>
            <div class="info-item">
                <span class="info-label">Sekolah</span>
                <span class="info-value">SMA Negeri 15 Jakarta</span>
            </div>
            <div class="info-item">
                <span class="info-label">Jurusan</span>
                <span class="info-value"><strong>IPS (Ilmu Pengetahuan Sosial)</strong> <i class="fas fa-globe-asia" style="color:#e68a2e;"></i></span>
            </div>
            <div class="info-item">
                <span class="info-label">Motto Hidup</span>
                <span class="info-value">“Peluang tidak datang begitu saja. Kamulah yang harus menciptakannya.”</span>
            </div>
        </div>

        <!-- Kolom Kanan: Hobi & Karakter + Genre Petualang & Kuliner -->
        <div class="info-card">
            <h3><i class="fas fa-heart"></i> Hobi & Minat</h3>
            <div class="info-item">
                <span class="info-label">📚 Hobi</span>
                <div class="info-value">
                    <div class="hobby-list">
                        <span class="hobby-badge"><i class="fas fa-book-open"></i> Membaca Novel</span>
                        <span class="hobby-badge"><i class="fas fa-film"></i> Nonton Film</span>
                        <span class="hobby-badge"><i class="fas fa-headphones"></i> Mendengarkan Musik</span>
                    </div>
                </div>
            </div>
            <div class="info-item">
                <span class="info-label">✨ Genre Favorit</span>
                <div class="info-value">
                    <span class="genre-badge"><i class="fas fa-compass"></i> Petualang</span>
                    <span class="genre-badge"><i class="fas fa-utensils"></i> Kuliner</span>
                    <div style="margin-top: 8px; font-size:0.85rem; color:#a8632f;">✨ Suka eksplorasi tempat baru & mencicipi hidangan khas ✨</div>
                </div>
            </div>
            <div class="info-item">
                <span class="info-label">Cita-cita</span>
                <span class="info-value">Pengusaha Kreatif & Food Explorer</span>
            </div>
            <div class="info-item">
                <span class="info-label">Kepribadian</span>
                <span class="info-value">Pantang menyerah, Visioner, Petualang, Empatik</span>
            </div>
        </div>
    </div>

    <!-- Tombol menuju link proyek -->
    <div class="button-wrapper">
        <a href="https://ats1922.github.io/Monopoli123/" target="_blank" rel="noopener noreferrer" class="project-btn">
            <i class="fas fa-gamepad"></i> Jelajahi Proyek Saya
            <i class="fas fa-arrow-right"></i>
        </a>
        <p style="margin-top: 14px; font-size: 0.75rem; color: #c2884b;">
            <i class="fas fa-external-link-alt"></i> Klik tombol di atas untuk langsung menuju website proyek Monopoli123
        </p>
    </div>

    <div class="footer-note">
        <i class="fas fa-heart" style="color: #f5a06e;"></i> Tiara Afriyani — SMAN 15 Jakarta, X5 IPS | Petualang & Pencinta Kuliner
    </div>
</div>

<script>
    // Interaksi ringan (konsol ramah)
    console.log("✨ Tiara Afriyani | Jurusan IPS | Hobi: Baca Novel, Nonton Film, Dengar Musik | Genre: Petualang & Kuliner ✨");
    const projectLink = document.querySelector('.project-btn');
    if(projectLink) {
        projectLink.addEventListener('click', () => {
            console.log("Mengunjungi proyek Monopoli123 — Terima kasih!");
        });
    }
</script>
</body>
</html>
