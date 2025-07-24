<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CinemaPlus - Film Terbaru 2025</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        :root {
            --primary: #E50914;
            --dark: #141414;
            --light: #f5f5f1;
            --secondary: #221f1f;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--dark);
            color: var(--light);
        }

        /* Header Styles */
        header {
            background: linear-gradient(to bottom, rgba(0,0,0,0.7) 0%, rgba(0,0,0,0) 100%);
            padding: 1rem 5%;
            position: fixed;
            width: 100%;
            z-index: 100;
            transition: all 0.3s ease;
        }

        header.scrolled {
            background-color: var(--dark);
        }

        .logo {
            color: var(--primary);
            font-weight: bold;
            font-size: 1.8rem;
        }

        .search-bar {
            background-color: rgba(255,255,255,0.1);
            border: 1px solid rgba(255,255,255,0.2);
            padding: 0.5rem 1rem;
            border-radius: 4px;
            width: 300px;
            color: white;
        }

        /* Hero Section */
        .hero {
            height: 80vh;
            background: linear-gradient(to right, rgba(0,0,0,0.9) 0%, rgba(0,0,0,0.1) 100%), url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ac05c98f-8bcc-4ffc-9f5b-181b014f09aa.png') no-repeat center center/cover;
            display: flex;
            align-items: center;
            padding: 0 5%;
        }

        .hero-content {
            max-width: 600px;
        }

        .hero-title {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hero-description {
            margin-bottom: 1.5rem;
            line-height: 1.6;
        }

        .btn {
            padding: 0.7rem 1.5rem;
            border-radius: 4px;
            font-weight: bold;
            cursor: pointer;
            margin-right: 1rem;
            transition: all 0.3s ease;
        }

        .btn-primary {
            background-color: var(--primary);
            color: white;
            border: none;
        }

        .btn-secondary {
            background-color: rgba(255,255,255,0.2);
            color: white;
            border: none;
        }

        .btn:hover {
            opacity: 0.8;
            transform: translateY(-3px);
        }

        /* Movies Section */
        section {
            padding: 3rem 5%;
        }

        .section-title {
            margin-bottom: 2rem;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 50%;
            height: 3px;
            background-color: var(--primary);
        }

        .movies-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 2rem;
        }

        .movie-card {
            background-color: var(--secondary);
            border-radius: 8px;
            overflow: hidden;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .movie-card:hover {
            transform: scale(1.05);
        }

        .movie-poster {
            width: 100%;
            height: 280px;
            object-fit: cover;
        }

        .movie-info {
            padding: 1rem;
        }

        .movie-title {
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .movie-meta {
            display: flex;
            justify-content: space-between;
            color: #777;
            font-size: 0.9rem;
        }

        /* Categories */
        .category-tabs {
            display: flex;
            gap: 1rem;
            margin-bottom: 2rem;
            flex-wrap: wrap;
        }

        .category-tab {
            padding: 0.5rem 1.5rem;
            background-color: var(--secondary);
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .category-tab.active, .category-tab:hover {
            background-color: var(--primary);
        }

        /* Footer */
        footer {
            background-color: var(--secondary);
            padding: 3rem 5%;
            text-align: center;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
            flex-wrap: wrap;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin: 1rem 0;
        }

        .social-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255,255,255,0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }

        .social-icon:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero {
                height: 60vh;
            }
            
            .hero-title {
                font-size: 2rem;
            }
            
            .movies-grid {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
            
            .search-bar {
                width: 200px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="flex justify-between items-center">
            <div class="logo">Cinema<span class="text-red-500">Plus</span></div>
            <nav class="hidden md:flex gap-6">
                <a href="#" class="hover:text-red-500 transition">Beranda</a>
                <a href="#" class="hover:text-red-500 transition">Film</a>
                <a href="#" class="hover:text-red-500 transition">Series</a>
                <a href="#" class="hover:text-red-500 transition">Anime</a>
            </nav>
            <div class="flex items-center gap-4">
                <input type="text" class="search-bar" placeholder="Cari film, series...">
                <button class="btn-primary">Masuk</button>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1 class="hero-title">Avengers: Secret Wars</h1>
            <p class="hero-description">Film terakhir dari Saga Multiverse Marvel ini akan menyatukan kembali para pahlawan dari seluruh alam semesta untuk menghadapi ancaman terbesar yang pernah ada. Dengan karakter-karakter baru dan kembalinya beberapa legenda.</p>
            <div class="flex">
                <button class="btn btn-primary"><i class="fas fa-play mr-2"></i>Nonton Sekarang</button>
                <button class="btn btn-secondary"><i class="fas fa-info-circle mr-2"></i>Info Lainnya</button>
            </div>
        </div>
    </section>

    <!-- Main Content -->
    <main>
        <!-- New Releases -->
        <section>
            <h2 class="section-title">Film Terbaru 2025</h2>
            <div class="movies-grid">
                <!-- Movie 1 -->
                <div class="movie-card">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/d9c723a3-a300-4e84-94ba-0cda5c3f829a.png" alt="Poster film Avengers: Secret Wars menampilkan karakter Marvel dalam pose epik" class="movie-poster">
                    <div class="movie-info">
                        <h3 class="movie-title">Avengers: Secret Wars</h3>
                        <div class="movie-meta">
                            <span>2025</span>
                            <span><i class="fas fa-star text-yellow-400"></i> 9.1</span>
                        </div>
                    </div>
                </div>
                <!-- Movie 2 -->
                <div class="movie-card">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/adf4c1af-0930-40fa-a792-16a55a5b64f2.png" alt="Poster film Superman Legacy dengan Superman terbang di atas kota metropolis" class="movie-poster">
                    <div class="movie-info">
                        <h3 class="movie-title">Superman: Legacy</h3>
                        <div class="movie-meta">
                            <span>2025</span>
                            <span><i class="fas fa-star text-yellow-400"></i> 8.7</span>
                        </div>
                    </div>
                </div>
                <!-- Movie 3 -->
                <div class="movie-card">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/6df757bb-64e7-4e5b-acd1-af157fe9b138.png" alt="Poster film Jurassic World 4 dengan dinosaurus di habitat modern" class="movie-poster">
                    <div class="movie-info">
                        <h3 class="movie-title">Jurassic World 4</h3>
                        <div class="movie-meta">
                            <span>2025</span>
                            <span><i class="fas fa-star text-yellow-400"></i> 8.3</span>
                        </div>
                    </div>
                </div>
                <!-- Movie 4 -->
                <div class="movie-card">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/26836d62-cca0-411c-b21d-a04286630312.png" alt="Poster film No Time to Die dengan Daniel Craig sebagai James Bond berdiri dengan pose aksi" class="movie-poster">
                    <div class="movie-info">
                        <h3 class="movie-title">No Time to Die</h3>
                        <div class="movie-meta">
                            <span>2021</span>
                            <span><i class="fas fa-star text-yellow-400"></i> 7.3</span>
                        </div>
                    </div>
                </div>
                <!-- Movie 5 -->
                <div class="movie-card">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/53f7fe29-092d-4219-a01d-b1559686832e.png" alt="Poster film Shang-Chi dengan karakter utama melakukan gerakan seni bela diri dengan latar belakang kota dan pegunungan" class="movie-poster">
                    <div class="movie-info">
                        <h3 class="movie-title">Shang-Chi</h3>
                        <div class="movie-meta">
                            <span>2021</span>
                            <span><i class="fas fa-star text-yellow-400"></i> 7.4</span>
                        </div>
                    </div>
                </div>
                <!-- Movie 6 -->
                <div class="movie-card">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/6eb438f8-0934-4df0-99f6-9cc0b57f6b71.png" alt="Poster film Black Widow menampilkan Scarlett Johansson sebagai Natasha Romanoff dalam pose aksi dengan efek visual merah dan hitam" class="movie-poster">
                    <div class="movie-info">
                        <h3 class="movie-title">Black Widow</h3>
                        <div class="movie-meta">
                            <span>2021</span>
                            <span><i class="fas fa-star text-yellow-400"></i> 6.7</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Categories -->
        <section>
            <h2 class="section-title">Kategori Film</h2>
            <div class="category-tabs">
                <div class="category-tab active">Semua</div>
                <div class="category-tab">Aksi</div>
                <div class="category-tab">Petualangan</div>
                <div class="category-tab">Komedi</div>
                <div class="category-tab">Drama</div>
                <div class="category-tab">Horor</div>
                <div class="category-tab">Romantis</div>
                <div class="category-tab">Sci-Fi</div>
            </div>
            <div class="movies-grid">
                <!-- Additional movies filtered by category would appear here -->
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <div class="logo">Cinema<span style="color: var(--primary)">Plus</span></div>
        <div class="footer-links">
            <a href="#">Tentang Kami</a>
            <a href="#">Kebijakan Privasi</a>
            <a href="#">Syarat & Ketentuan</a>
            <a href="#">Bantuan</a>
            <a href="#">Kontak</a>
        </div>
        <div class="social-icons">
            <a href="#" class="social-icon"><i class="fab fa-facebook-f"></i></a>
            <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
            <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
            <a href="#" class="social-icon"><i class="fab fa-youtube"></i></a>
        </div>
        <p class="text-gray-500 mt-4">© 2023 CinemaPlus. All Rights Reserved.</p>
    </footer>

    <script>
        // Sticky Header
        window.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Category Tabs
        document.querySelectorAll('.category-tab').forEach(tab => {
            tab.addEventListener('click', function() {
                document.querySelector('.category-tab.active').classList.remove('active');
                this.classList.add('active');
                // Here you would normally filter movies by category
            });
        });

        // Movie Card Hover Effect
        document.querySelectorAll('.movie-card').forEach(card => {
            card.addEventListener('mouseenter', function() {
                this.style.boxShadow = '0 10px 20px rgba(229, 9, 20, 0.3)';
            });
            card.addEventListener('mouseleave', function() {
                this.style.boxShadow = 'none';
            });
        });
    </script>
</body>
</html>
