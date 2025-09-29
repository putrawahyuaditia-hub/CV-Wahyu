<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bio Data - wahyu</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.15);
            overflow: hidden;
            animation: slideUp 0.8s ease-out;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        header {
            background: linear-gradient(135deg, #49461b 0%, #486913 100%);
            color: white;
            text-align: center;
            padding: 50px 20px;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: pulse 4s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.1); opacity: 0.8; }
        }

        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 6px solid white;
            margin-bottom: 25px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            transition: all 0.4s ease;
            position: relative;
            z-index: 1;
        }

        .profile-img:hover {
            transform: scale(1.1) rotate(5deg);
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
        }

        h1 {
            font-size: 2.8em;
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
            position: relative;
            z-index: 1;
        }

        .subtitle {
            font-size: 1.3em;
            opacity: 0.95;
            position: relative;
            z-index: 1;
        }

        .social-links {
            margin-top: 25px;
            display: flex;
            justify-content: center;
            gap: 20px;
            position: relative;
            z-index: 1;
        }

        .social-links a {
            color: white;
            font-size: 1.5em;
            transition: all 0.3s ease;
            display: inline-block;
        }

        .social-links a:hover {
            transform: translateY(-5px) scale(1.2);
            color: #ffd700;
        }

        .content {
            padding: 50px;
        }

        .section {
            margin-bottom: 50px;
            animation: fadeIn 1s ease-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        h2 {
            color: #667eea;
            margin-bottom: 25px;
            font-size: 2em;
            border-bottom: 3px solid #667eea;
            padding-bottom: 10px;
            display: inline-block;
            position: relative;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 0;
            height: 3px;
            background: #764ba2;
            transition: width 0.5s ease;
        }

        h2:hover::after {
            width: 100%;
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-bottom: 30px;
        }

        .info-item {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 20px;
            border-radius: 15px;
            transition: all 0.3s ease;
            border: 1px solid transparent;
            position: relative;
            overflow: hidden;
        }

        .info-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(102, 126, 234, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .info-item:hover::before {
            left: 100%;
        }

        .info-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            border-color: #667eea;
        }

        .info-label {
            font-weight: bold;
            color: #667eea;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .info-label i {
            font-size: 1.1em;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
        }

        .skill-tag {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 12px 24px;
            border-radius: 25px;
            font-size: 1em;
            font-weight: 500;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .skill-tag::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(255,255,255,0.3);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            transition: width 0.6s, height 0.6s;
        }

        .skill-tag:hover::before {
            width: 300px;
            height: 300px;
        }

        .skill-tag:hover {
            transform: scale(1.1) translateY(-3px);
            box-shadow: 0 8px 20px rgba(102, 126, 234, 0.4);
        }

        .timeline {
            position: relative;
            padding-left: 30px;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 3px;
            background: linear-gradient(to bottom, #667eea, #764ba2);
        }

        .timeline-item {
            position: relative;
            margin-bottom: 30px;
            background: #f8f9fa;
            padding: 25px;
            border-radius: 15px;
            transition: all 0.3s ease;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -36px;
            top: 25px;
            width: 15px;
            height: 15px;
            background: #667eea;
            border-radius: 50%;
            border: 3px solid white;
            box-shadow: 0 0 0 3px #667eea;
        }

        .timeline-item:hover {
            transform: translateX(10px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            background: white;
        }

        .timeline-title {
            font-weight: bold;
            color: #333;
            font-size: 1.2em;
            margin-bottom: 8px;
        }

        .timeline-subtitle {
            color: #667eea;
            font-style: italic;
            margin-bottom: 5px;
        }

        .timeline-date {
            color: #666;
            font-size: 0.9em;
            margin-bottom: 10px;
        }

        .contact-info {
            text-align: center;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 40px;
            border-radius: 20px;
            box-shadow: inset 0 2px 10px rgba(0,0,0,0.05);
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .contact-item {
            background: white;
            padding: 20px;
            border-radius: 15px;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .contact-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            border-color: #667eea;
        }

        .contact-item a {
            color: #667eea;
            text-decoration: none;
            font-weight: 500;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            transition: color 0.3s ease;
        }

        .contact-item a:hover {
            color: #764ba2;
        }

        .contact-item i {
            font-size: 1.3em;
        }

        .download-btn {
            display: inline-block;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px 40px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            margin-top: 30px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
        }

        .download-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.5);
        }

        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 30px;
            font-size: 0.95em;
        }

        .footer-links {
            margin-top: 15px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .footer-links a {
            color: #ecf0f1;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: #667eea;
        }

        @media (max-width: 768px) {
            .container {
                margin: 10px;
                border-radius: 15px;
            }

            h1 {
                font-size: 2.2em;
            }

            .content {
                padding: 30px 20px;
            }

            .info-grid {
                grid-template-columns: 1fr;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            .social-links {
                gap: 15px;
            }
        }

        /* Animasi untuk skill tags saat dihover */
        @keyframes skillPulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        .skill-tag:hover {
            animation: skillPulse 0.6s ease-in-out;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <img src="foto-wahyu.jpeg" alt="wahyu aditia" class="profile-img">
            <h1>wahyu aditia putra</h1>
            <p class="subtitle">in engineering we trust, smart guy will always be the top tier of our type</p>
           
        </header>

        <div class="content">
            <section class="section">
                <h2><i class="fas fa-user"></i> Informasi Personal</h2>
                <div class="info-grid">
                    <div class="info-item">
                        <div class="info-label">
                            <i class="fas fa-id-card"></i> Nama Lengkap
                        </div>
                        <div>wahyu aditia putra</div>
                    </div>
                    <div class="info-item">
                        <div class="info-label">
                            <i class="fas fa-birthday-cake"></i> Tempat, Tanggal Lahir
                        </div>
                        <div>Surabaya, 23 februari 2006</div>
                    </div>
                    <div class="info-item">
                        <div class="info-label">
                            <i class="fas fa-map-marker-alt"></i> Alamat
                        </div>
                        <div>tambak gringsing baru</div>
                    </div>
                    <div class="info-item">
                        <div class="info-label">
                            <i class="fas fa-heart"></i> Status
                        </div>
                        <div>solo</div>
                    </div>
                </div>
            </section>

            <section class="section">
                <h2><i class="fas fa-info-circle"></i> Tentang Saya</h2>
                <p style="text-align: justify; font-size: 1.1em; line-height: 1.8;">
                    saya adalah mahasiswa itats yg baru masuk kuliah sebelum kuliah saya sekolah di smk rajasa Surabaya
                    saya masuk itats karena rekomendasi dari orang tua saya yg alumni itats 2005
                </p>
            </section>

            <section class="section">
                <h2><i class="fas fa-code"></i> Keahlian</h2>
                <div class="skills">
                    <span class="skill-tag">HTML</span>
                    <span class="skill-tag">CSS</span>
                    <span class="skill-tag">PYTON</span>
                </div>
            </section>

            <section class="section">
                <h2><i class="fas fa-briefcase"></i> Pengalaman Kerja</h2>
                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-title">pengalaman magang</div>
                        <div class="timeline-subtitle">dinas pendidikan provinsi jatim</div>
                        <div class="timeline-date">2024 - 2025</div>
                    </div>
                  
                </div>
            </section>

            <section class="section">
                <h2><i class="fas fa-graduation-cap"></i> Pendidikan</h2>
                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-title">S1 Teknik Informatika</div>
                        <div class="timeline-subtitle">institut teknologi adhi tama Surabaya</div>
                        <div class="timeline-date">2025</div>
                    </div>
                </div>
            </section>

      

        <footer>
            <p>&copy; 2025 wahyu aditia putra. All rights reserved.</p>
            <div class="footer-links">
                <a href="#">Privacy Policy</a>
                <a href="#">Terms of Service</a>
                <a href="#">Sitemap</a>
            </div>
        </footer>
    </div>

    <script>
        // Animasi saat scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(30px)';
            section.style.transition = 'all 0.6s ease-out';
            observer.observe(section);
        });

        // Efek typing untuk subtitle
        const subtitle = document.querySelector('.subtitle');
        const text = subtitle.textContent;
        subtitle.textContent = '';
        let i = 0;

        function typeWriter() {
            if (i < text.length) {
                subtitle.textContent += text.charAt(i);
                i++;
                setTimeout(typeWriter, 50);
            }
        }

        setTimeout(typeWriter, 1000);

        // Smooth scroll untuk anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
