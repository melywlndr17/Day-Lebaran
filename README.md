<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Story Lebaran Saya</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            background-color: #faf1f1;
            color: #333;
        }

        .wrapper {
            display: flex;
            min-height: 100vh;
        }

        .sidebar {
            width: 250px;
            background-color: #60b0c4;
            color: white;
            padding: 20px;
            position: fixed;
            height: 100%;
            overflow-y: auto;
            z-index: 999;
        }

        .sidebar h2 {
            text-align: center;
            margin-bottom: 20px;
            border-bottom: 2px solid #fff;
            padding-bottom: 10px;
        }

        .sidebar ul {
            list-style: none;
        }

        .sidebar ul li {
            margin-bottom: 15px;
        }

        .sidebar ul li a {
            color: white;
            text-decoration: none;
            display: block;
            padding: 12px;
            border-radius: 5px;
            transition: background-color 0.3s;
            font-weight: bold;
        }

        .sidebar ul li a:hover {
            background-color: #334557;
        }
        
        .sidebar ul li a.active {
            background-color: #334557;
        }

        .container {
            margin-left: 250px;
            width: calc(100% - 250px);
            padding: 20px;
        }

        .content {
            background-color: rgb(204, 219, 215);
            border-radius: 10px;
            padding: 25px;
            margin-bottom: 30px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            display: block;
        }
        header {
            text-align: center;
            padding: 20px 0;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #6998ce, #cb6d80);
            border-radius: 8px;
            color: rgb(59, 51, 51);
        }
        h1, h2, h3 {
            color: #0e031d;
            margin-bottom: 15px;
        }
        header h1 {
            color: white;
        }
        p {
            line-height: 1.6;
            margin-bottom: 15px;
        }
        .welcome-text {
            font-size: 2.5rem;
            text-align: center;
            font-weight: bold;
            margin: 30px 0;
            padding: 15px;
            background: linear-gradient(135deg, #ea468d, #f7aeae, #73c8a9, #40e65c);
            background-size: 400% 400%;
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: colorChange 8s infinite linear;
            text-shadow: 2px 2px 3px rgba(230, 112, 112, 0.1);
        }

        @keyframes colorChange {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }

        .gallery-item {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 3px 4px rgba(0,0,0,0.1);
            transition: transform 0.3s;
            background-color: white;
        }

        .gallery-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 10px rgba(0,0,0,0.2);
        }

        .gallery-item img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            display: block;
            cursor: pointer;
        }

        .gallery-item video {
            width: 100%;
            height: 300px;
            object-fit: cover;
            display: block;
        }

        .caption {
            padding: 10px;
            background-color: white;
            text-align: center;
            font-style: italic;
        }

        footer {
            text-align: center;
            padding: 15px;
            margin-top: 10px;
            background-color: #4a9cb1;
            color: rgb(37, 29, 29);
            border-radius: 15px;
        }

        .profile {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }

        .profile img {
            width: 300px;
            height: 300px;
            border-radius: 70%;
            object-fit: cover;
            margin-right: 20px;
            border: 3px solid #98b6cf;
        }

        .profile-info {
            flex: 2;
        }

        /* Modal untuk memperbesar gambar */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            padding-top: 50px;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.9);
        }

        .modal-content {
            margin: auto;
            display: block;
            max-width: 90%;
            max-height: 90%;
        }

        .close {
            position: absolute;
            top: 15px;
            right: 35px;
            color: #f1f1f1;
            font-size: 40px;
            font-weight: bold;
            transition: 0.3s;
            z-index: 1001;
        }

        .close:hover,
        .close:focus {
            color: #bbb;
            text-decoration: none;
            cursor: pointer;
        }

        /* Responsive design */
        @media (max-width: 800px) {
            .wrapper {
                flex-direction: column;
            }
            
            .sidebar {
                width: 100%;
                height: auto;
                position: relative;
            }
            
            .container {
                margin-left: 0;
                width: 100%;
            }
    
            .gallery {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }
            
            .profile {
                flex-direction: column;
                text-align: center;
            }
            
            .profile img {
                margin-right: 0;
                margin-bottom: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="wrapper">
        <div class="sidebar">
            <h2>Day Lebaran</h2>
            <ul>
                <li><a href="#about">Me</a></li>
                <li><a href="#hari-pertama">Lebaran Hari Pertama</a></li>
                <li><a href="#hari-kedua">Lebaran Hari Kedua</a></li>
                <li><a href="#hari-ketiga">Lebaran Hari Ketiga</a></li>
                <li><a href="#hari-keempat">Lebaran Hari Keempat</a></li>
                <li><a href="#hari-kelima">Lebaran Hari Kelima</a></li>
                <li><a href="#hari-keenam">Lebaran Hari Keenam</a></li>
            </ul>
        </div>

        <div class="container">
            <h1 class="welcome-text">🌷🌷 Selamat Datang di Halaman Lebaran Saya 🌷🌷</h1>
            <div id="about" class="content">
                <h2>✍️</h2>
                <div class="profile">
                    <img src="foto mely4.jpg" alt="Foto Profil">
                    <div class="profile-info">
                        <p>Assalamu'alaikum, selamat datang di halaman lebaran saya Mely Wulandari, senang berbagi momen spesial lebaran saya bersama keluarga dan kerabat tercinta. Halaman ini berisi kumpulan momen indah selama perayaan Idul Fitri 1446 H yang ingin saya bagikan. Semoga lebaran kita diberkahi Allah SWT dengan kebahagiaan dan kesehatan bersama orang tercinta.</p>
                    </div>
                </div>
            </div>

            <div id="hari-pertama" class="content">
                <h2>Lebaran Hari Pertama</h2>
                <p>Takbir bergema, Shalat Ied di pagi hari menjadi pembuka perayaan Idul Fitri 1446 H. Berkumpul dengan keluarga besar, saling memaafkan, dan berbagi kebahagiaan menjadi momen yang tak terlupakan.</p>
                
                <div class="gallery">
                    <div class="gallery-item">
                        <img src="keluarga.jpg" alt="dokumentasi keluargaku, sebelum ke mesjid" class="gallery-img">
                        <div class="caption">Dokumentasi keluargaku, sebelum ke mesjid</div>
                    </div>
                    <div class="gallery-item">
                        <img src="foto mesjid1.jpg" alt="Suasana di mesjid" class="gallery-img">
                        <div class="caption">Suasana di mesjid</div>
                    </div>
                </div>
                <div class="gallery-item">
                    <img src="di mesjid(dila, julia, azmil).jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="mamalagimesjid.jpg" alt=""  class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb1.2.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb1.4.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb1.5.jpg"></div class="gallery-img">
                </div>
                <div class="gallery-item">
                    <img src="leb1.6.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb1.8.jpg" alt=""class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <video controls>
                        <source src="leb1.vidio.mp4" type="video/mp4" class="gallery-img">
                        Browser Anda tidak mendukung tag video.
                    </video>
                    <div class="caption">Tradisi kaum laki-laki mando'a ke rumah masyarakat yang berada disekitar.</div>
                </div>
            </div>
        </div>

        <div id="hari-kedua" class="content">
            <h2>Lebaran Hari Kedua</h2>
            <p>Lebaran hari kedua, kami pergi berkunjung kerumah mertuanya kakak pertama ku, yang tidak terlalu jauh dari rumah, beda kecamatan.Kami berangkat pukul 14.00 WIB, perjalanan kami di hadapi dengan mobil kami yang tiba-tiba mati, dan juga jalan yang lumayan macet, sehingga matinya mobil kami menamnbah kemacetan. Dan Alhamdulillah ada orang baik yang menawarkan dirinya untuk mendorong mobil kami kepingkir jalan, agar tidak mengganggu kemacetan. Tak lama kemudian datang lah seorang montil yang barusan dihubungi oleh abang ipar, setelah diperbaiki mobil kami pun hidup, lanjut kami jalan, dan kami sampe di rumah mertua kakak diwaktu magrib. .</p>
            
            <div class="gallery">
                <div class="gallery-item">
                    <img src="lebaran ke2.jpg" alt="" class="gallery-img">
                    <div class="caption">Dokumentasi dulu 😄</div>
                </div>
                <div class="gallery-item">
                    <img src="leb2.2.jpg" alt="" class="gallery-img">
                    <div class="caption">Ceritanya kami baru sampai di rumah mertuanya kakak, aku ngajak fotbar terlebih dahulu sebelum masuk ke dalam rumah, karena langit juga sudah mulai gelap😄👉</div>
                </div>
                <div class="gallery-item">
                    <img src="leb2.3.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb2.4.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb2.9.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb2.10.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <video controls>
                        <source src="leb2.vidio.mp4" type="video/mp4" class="gallery-img">
                        Browser Anda tidak mendukung tag video.
                    </video>
                    <div class="caption">Suasana Ramah Tamah</div>
                </div>
            </div>
        </div>

        <div id="hari-ketiga" class="content">
            <h2>Lebaran Hari Ketiga</h2>
            <p>Di hari ketiga, kami pergi menjalang. Yang merupakan adat istiadat dan tradisi di Minangkabau yang setiap lebarannya pergi manjalang kerumah kerabat family dan induak bako. Untuk hari pertama menjalang kami pergi ke 9 rumah yang ada di jorong kami dengan membawa rantang yang berisikan beras, dan kue-kue. Saya pergi bersama kakak perempuan yang nomor dua.</p>
            
            <div class="gallery">
                <div class="gallery-item">
                    <img src="leb3..jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb3. manjalang.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb3.4.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb3.5.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb3.6.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb3.7.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb3.8.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb3.9.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <video controls>
                        <source src="leb3.vidio.mp4" type="video/mp4" class="gallery-img">
                        Browser Anda tidak mendukung tag video.
                    </video>
                    <div class="caption">kocak khaira, belajar jadi konten kreator😄</div>
                </div>
                <div class="gallery-item">
                    <video controls>
                        <source src="leb3.vidio2.mp4" type="video/mp4" class="gallery-img">
                        Browser Anda tidak mendukung tag video.
                    </video>
                    <div class="caption"></div>
                </div>
               
             
            </div>
        </div>

        <div id="hari-keempat" class="content">
            <h2>Lebaran Hari Keempat</h2>
            <p>Lebaran hari ke empat masih dengan suasana pergi manjalang, dan kami pergi menjalang ke kampung orang tua papa, kegiatan manjalang kali ini lumayan seru, karena kampung papa ni dekat danau atas gais, 
            Maa Syaa Allah bangettt pemandangannya. 🫶🤗 </p>
            
            <div class="gallery">
                <div class="gallery-item">
                    <img src="profil.jpg" alt="" class="gallery-img">
                    <div class="caption">Dokumenasi adalah hal yang wajib😄</div>
                </div>
                <div class="gallery-item">
                    <img src="leb4.7.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb4.1.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb4.3.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb4.6.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb4.8.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb4.9.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb4. kunjungan.jpg" alt="" class="gallery-img">
                    <div class="caption">Datang yang berbarengan dimalam itu, kami yang baru pulang dari menjalang dan kakak perempuan beserta keluarga suami nya juga baru sampai di rumah untuk pergi beraya, suasana khidmat antara dua keluarga, obrolan datang dengan sendirinya mulai dari pembahasan kebun, kemacetan, lebaran, dan lainnya. </div>
                </div>
                <div class="gallery-item">
                    <video controls>
                        <source src="leb4.vidio.mp4" type="video/mp4" class="gallery-img">
                        Browser Anda tidak mendukung tag video.
                    </video>
                    <div class="caption">Vidio perjalanan menuju tempat bako, perjalanan double dengan menikmati keindahan alam.</div>
                </div>
            </div>
        </div>

        <div id="hari-kelima" class="content">
            <h2>Lebaran Hari Kelima</h2>
            <p>Dihari kelima kami pergi kerumah sepupu pergi beraya, disini kami disuguhi dengan Soto Ayam penggugah selera, banyak tawa dari pertemuan kami saat itu, menyaksikan kerandoman kami kalau sudah berkumpul, tingkah hanin sepupu kecil kami dan membuat tawa kami semakin menjadi-jadi. ✍️😄 </p>
            <div class="gallery">
                <div class="gallery-item">
                    <img src="leb5.1.jpg"  alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb5.2.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
            <div class="gallery-item">
                <video controls>
                    <source src="leb5. hanin.mp4" type="video/mp4"  class="gallery-img">
                    Browser Anda tidak mendukung tag video.
                </video>
                <div class="caption"></div>
            </div>
        </div>
        </div>
        <div id="hari-keenam" class="content">
            <h2>Lebaran Hari Keenam</h2>
            <p>Kami bantu ibu Maurek bawang gais, ceritanya kami mulai jam 11.00 WIB sampai jam 21.30 WIB kami pulang nya sudah malam gais, bawang nya itu mau dibawa ibu kepasar pagi minggu gais, jadi kalo kami ga bantu ibu sape selesai ibu bakal kerjainnya sampe larut malam, yaudah gapapa kami bantuin ibu aja sampe kelar 🤗🫶.</p>
            
            <div class="gallery">
                <div class="gallery-item">
                    <img src="leb6.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb6.1.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb6.2.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
                <div class="gallery-item">
                    <img src="leb6.3.jpg" alt="" class="gallery-img">
                    <div class="caption"></div>
                </div>
            </div>
            <div class="gallery-item">
                <video controls>
                    <source src="leb6.vidi.mp4" type="video/mp4"  class="gallery-img">
                    Browser Anda tidak mendukung tag video.
                </video>
                <div class="caption"></div>
            </div>
        </div>
            </div>

            <footer class="footer">
                <p>Desain by Mely Wulandari >>> email: mellywulandari22@gmail.com >> Instagram: melywlndr17 > contac person: 085271683937 </p>
            </footer>
        </div>
    </div>

    <!-- Modal untuk memperbesar gambar -->
    <div id="imageModal" class="modal">
        <span class="close">&times;</span>
        <img class="modal-content" id="imgModal">
    </div>

    <script>
        // Smooth scroll untuk navigasi
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                // Hapus class active dari semua link
                document.querySelectorAll('.sidebar a').forEach(link => {
                    link.classList.remove('active');
                });
                
                // Tambahkan class active ke link yang diklik
                this.classList.add('active');
                
                // Scroll smooth ke target
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    window.scrollTo({
                        top: target.offsetTop - 20,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Menampilkan bagian yang aktif saat halaman dimuat
        window.addEventListener('DOMContentLoaded', (event) => {
            // Set link about sebagai active secara default
            document.querySelector('a[href="#about"]').classList.add('active');
        });
        
        // Kode untuk memperbesar gambar saat diklik
        const modal = document.getElementById("imageModal");
        const modalImg = document.getElementById("imgModal");
        const closeBtn = document.getElementsByClassName("close")[0];
        
        // Tambahkan event listener ke semua gambar
        document.addEventListener('DOMContentLoaded', function() {
            const images = document.querySelectorAll('.gallery-img');
            images.forEach(img => {
                img.onclick = function() {
                    modal.style.display = "block";
                    modalImg.src = this.src;
                }
            });
        });
        
        // Tutup modal saat tombol close diklik
        closeBtn.onclick = function() {
            modal.style.display = "none";
        }
        
        // Tutup modal jika user klik di luar gambar
        window.onclick = function(event) {
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }
        
        // Mendeteksi section yang sedang dilihat untuk highlight menu
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('.content');
            let currentSection = "";
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= (sectionTop - 100)) {
                    currentSection = section.getAttribute('id');
                }
            });
            
            // Update active class di sidebar
            document.querySelectorAll('.sidebar a').forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === `#${currentSection}`) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
