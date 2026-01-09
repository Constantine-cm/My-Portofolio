<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portofolio & CV Profesional</title>
    
    <!-- Google Fonts: Inter (Standar Profesional Modern) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- Font Awesome untuk Ikon -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Konfigurasi Tailwind Custom -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        primary: '#0f172a', // Slate 900
                        secondary: '#334155', // Slate 700
                        accent: '#2563eb', // Blue 600
                        light: '#f8fafc', // Slate 50
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Styles untuk detail kecil */
        .glass-nav {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(0,0,0,0.05);
        }
        
        .fade-in-section {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
            will-change: opacity, visibility;
        }
        
        .fade-in-section.is-visible {
            opacity: 1;
            transform: none;
        }

        /* Timeline connector line */
        .timeline-line::before {
            content: '';
            position: absolute;
            top: 0;
            bottom: 0;
            left: 15px;
            width: 2px;
            background: #e2e8f0;
            z-index: 0;
        }
    </style>
</head>
<body class="bg-light text-secondary font-sans antialiased selection:bg-accent selection:text-white">

    <!-- Navigation -->
    <nav class="fixed w-full z-50 glass-nav transition-all duration-300" id="navbar">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-primary tracking-tight">
                [Christian Bo<span class="text-accent">Constantine</span>]
            </a>
            
            <!-- Desktop Menu -->
            <div class="hidden md:flex space-x-8 text-sm font-medium">
                <a href="#about" class="hover:text-accent transition-colors">Tentang</a>
                <a href="#experience" class="hover:text-accent transition-colors">Pengalaman</a>
                <a href="#portfolio" class="hover:text-accent transition-colors">Portofolio</a>
                <a href="#skills" class="hover:text-accent transition-colors">Keahlian</a>
                <a href="#contact" class="px-5 py-2 bg-primary text-white rounded-full hover:bg-accent transition-colors">Hubungi Saya</a>
            </div>

            <!-- Mobile Menu Button -->
            <button class="md:hidden text-2xl text-primary focus:outline-none" onclick="toggleMenu()">
                <i class="fas fa-bars"></i>
            </button>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-t border-gray-100 absolute w-full shadow-lg">
            <div class="flex flex-col px-6 py-4 space-y-4">
                <a href="#about" class="block hover:text-accent" onclick="toggleMenu()">Tentang</a>
                <a href="#experience" class="block hover:text-accent" onclick="toggleMenu()">Pengalaman</a>
                <a href="#portfolio" class="block hover:text-accent" onclick="toggleMenu()">Portofolio</a>
                <a href="#skills" class="block hover:text-accent" onclick="toggleMenu()">Keahlian</a>
                <a href="#contact" class="block font-bold text-accent" onclick="toggleMenu()">Hubungi Saya</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="about" class="pt-32 pb-20 md:pt-40 md:pb-32 container mx-auto px-6 fade-in-section">
        <div class="flex flex-col-reverse md:flex-row items-center gap-12">
            <div class="md:w-1/2 text-center md:text-left">
                <p class="text-accent font-semibold mb-2 tracking-wide uppercase text-sm">Halo, nama saya</p>
                <h1 class="text-4xl md:text-6xl font-extrabold text-primary mb-6 leading-tight">
                    [CHRISTIAN BO CONSTANTINE]
                </h1>
                <h2 class="text-xl md:text-2xl text-secondary mb-6 font-light">
                    Seorang <span class="text-primary font-semibold">[Mahasiswa Teknik Biomedis]</span> yang berfokus pada hasil dan inovasi.
                </h2>
                <p class="text-slate-500 mb-8 leading-relaxed max-w-lg mx-auto md:mx-0">
                    [Tulis ringkasan singkat tentang diri Anda di sini. Contoh: Saya memiliki pengalaman lebih dari 5 tahun dalam mengelola proyek digital dan menciptakan solusi desain yang user-friendly.]
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
                    <a href="#portfolio" class="px-8 py-3 bg-primary text-white rounded-lg font-medium hover:bg-accent transition-all shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                        Lihat Karya
                    </a>
                    <a href="#" class="px-8 py-3 border border-slate-300 bg-white text-primary rounded-lg font-medium hover:border-primary hover:bg-slate-50 transition-all">
                        Unduh CV <i class="fas fa-download ml-2"></i>
                    </a>
                </div>
                
                <div class="mt-10 flex gap-6 justify-center md:justify-start text-2xl text-slate-400">
                    <a href="#" class="hover:text-primary transition-colors"><i class="fab fa-linkedin"></i></a>
                    <a href="#" class="hover:text-primary transition-colors"><i class="fab fa-github"></i></a>
                    <a href="#" class="hover:text-primary transition-colors"><i class="fab fa-instagram"></i></a>
                    <a href="#" class="hover:text-primary transition-colors"><i class="fas fa-envelope"></i></a>
                </div>
            </div>
            
            <div class="md:w-1/2 flex justify-center relative">
                <!-- Decorative Elements -->
                <div class="absolute w-72 h-72 bg-blue-100 rounded-full blur-3xl -z-10 top-0 right-10 opacity-70"></div>
                
                <!-- Profile Image Container -->
                <div class="relative group">
                    <div class="absolute inset-0 bg-accent rounded-2xl rotate-6 group-hover:rotate-3 transition-transform duration-300 opacity-20"></div>
                    <img 
                        src="https://placehold.co/400x500/e2e8f0/1e293b?text=Foto+Anda" 
                        alt="Profile Picture" 
                        class="relative rounded-2xl shadow-2xl w-72 md:w-80 object-cover z-10 border-4 border-white"
                        onerror="this.src='https://via.placeholder.com/400x500?text=Foto+Profil'"
                    >
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="py-20 bg-white">
        <div class="container mx-auto px-6 fade-in-section">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-primary mb-4">Pengalaman Kerja</h2>
                <div class="w-16 h-1 bg-accent mx-auto rounded"></div>
            </div>

            <div class="max-w-3xl mx-auto relative timeline-line">
                
                <!-- Experience Item 1 -->
                <div class="relative pl-12 pb-12 group">
                    <div class="absolute left-0 top-1 w-8 h-8 bg-white border-4 border-accent rounded-full z-10"></div>
                    <div class="bg-slate-50 p-6 rounded-xl border border-slate-100 shadow-sm hover:shadow-md transition-shadow">
                        <span class="text-sm text-accent font-bold tracking-wider mb-2 block">[Tahun Mulai] - [Sekarang/Tahun Selesai]</span>
                        <h3 class="text-xl font-bold text-primary mb-1">[Jabatan Pekerjaan]</h3>
                        <h4 class="text-md text-slate-600 font-medium mb-3">[Nama Perusahaan] - [Lokasi]</h4>
                        <p class="text-slate-500 text-sm leading-relaxed">
                            [Deskripsikan tanggung jawab utama dan pencapaian Anda di sini. Gunakan kalimat aktif.]
                            <ul class="list-disc list-inside mt-2 text-slate-500 text-sm space-y-1">
                                <li>Berhasil meningkatkan efisiensi sebesar X%.</li>
                                <li>Memimpin tim yang terdiri dari X orang.</li>
                            </ul>
                        </p>
                    </div>
                </div>

                <!-- Experience Item 2 -->
                <div class="relative pl-12 pb-12 group">
                    <div class="absolute left-0 top-1 w-8 h-8 bg-white border-4 border-slate-300 group-hover:border-accent rounded-full z-10 transition-colors"></div>
                    <div class="bg-slate-50 p-6 rounded-xl border border-slate-100 shadow-sm hover:shadow-md transition-shadow">
                        <span class="text-sm text-slate-500 font-bold tracking-wider mb-2 block">[Tahun Mulai] - [Tahun Selesai]</span>
                        <h3 class="text-xl font-bold text-primary mb-1">[Jabatan Pekerjaan Sebelumnya]</h3>
                        <h4 class="text-md text-slate-600 font-medium mb-3">[Nama Perusahaan]</h4>
                        <p class="text-slate-500 text-sm leading-relaxed">
                            [Deskripsi singkat pekerjaan. Fokus pada skill yang relevan dengan target karir Anda saat ini.]
                        </p>
                    </div>
                </div>

                <!-- Education Item -->
                <div class="relative pl-12 pb-4 group">
                    <div class="absolute left-0 top-1 w-8 h-8 bg-primary rounded-full z-10 flex items-center justify-center text-white text-xs">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <div class="bg-white p-6 rounded-xl border border-slate-200 shadow-sm">
                        <span class="text-sm text-slate-500 font-bold tracking-wider mb-2 block">[Tahun Lulus]</span>
                        <h3 class="text-xl font-bold text-primary mb-1">[Gelar / Jurusan]</h3>
                        <h4 class="text-md text-slate-600 font-medium">[Nama Universitas / Institusi]</h4>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-20 bg-slate-50">
        <div class="container mx-auto px-6 fade-in-section">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-primary mb-4">Keahlian & Tools</h2>
                <p class="text-slate-500 max-w-xl mx-auto">Teknologi dan kemampuan yang saya kuasai untuk membantu bisnis berkembang.</p>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-4 gap-6 max-w-4xl mx-auto">
                <!-- Skill 1 -->
                <div class="bg-white p-6 rounded-xl shadow-sm hover:shadow-lg transition-all text-center group cursor-default">
                    <div class="text-4xl text-blue-500 mb-3 group-hover:scale-110 transition-transform">
                        <i class="fab fa-html5"></i>
                    </div>
                    <h3 class="font-bold text-primary">HTML & CSS</h3>
                </div>
                <!-- Skill 2 -->
                <div class="bg-white p-6 rounded-xl shadow-sm hover:shadow-lg transition-all text-center group cursor-default">
                    <div class="text-4xl text-yellow-500 mb-3 group-hover:scale-110 transition-transform">
                        <i class="fab fa-js"></i>
                    </div>
                    <h3 class="font-bold text-primary">JavaScript</h3>
                </div>
                <!-- Skill 3 -->
                <div class="bg-white p-6 rounded-xl shadow-sm hover:shadow-lg transition-all text-center group cursor-default">
                    <div class="text-4xl text-cyan-500 mb-3 group-hover:scale-110 transition-transform">
                        <i class="fab fa-react"></i>
                    </div>
                    <h3 class="font-bold text-primary">React / Vue</h3>
                </div>
                <!-- Skill 4 -->
                <div class="bg-white p-6 rounded-xl shadow-sm hover:shadow-lg transition-all text-center group cursor-default">
                    <div class="text-4xl text-orange-500 mb-3 group-hover:scale-110 transition-transform">
                        <i class="fas fa-bullhorn"></i>
                    </div>
                    <h3 class="font-bold text-primary">Digital Marketing</h3>
                </div>
                <!-- Skill 5 -->
                <div class="bg-white p-6 rounded-xl shadow-sm hover:shadow-lg transition-all text-center group cursor-default">
                    <div class="text-4xl text-purple-500 mb-3 group-hover:scale-110 transition-transform">
                        <i class="fas fa-paint-brush"></i>
                    </div>
                    <h3 class="font-bold text-primary">UI/UX Design</h3>
                </div>
                <!-- Skill 6 -->
                <div class="bg-white p-6 rounded-xl shadow-sm hover:shadow-lg transition-all text-center group cursor-default">
                    <div class="text-4xl text-green-600 mb-3 group-hover:scale-110 transition-transform">
                        <i class="fas fa-file-excel"></i>
                    </div>
                    <h3 class="font-bold text-primary">Data Analysis</h3>
                </div>
                <!-- Skill 7 -->
                <div class="bg-white p-6 rounded-xl shadow-sm hover:shadow-lg transition-all text-center group cursor-default">
                    <div class="text-4xl text-pink-500 mb-3 group-hover:scale-110 transition-transform">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3 class="font-bold text-primary">Leadership</h3>
                </div>
                <!-- Skill 8 -->
                <div class="bg-white p-6 rounded-xl shadow-sm hover:shadow-lg transition-all text-center group cursor-default">
                    <div class="text-4xl text-indigo-500 mb-3 group-hover:scale-110 transition-transform">
                        <i class="fas fa-language"></i>
                    </div>
                    <h3 class="font-bold text-primary">English (Fluent)</h3>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio" class="py-20 bg-white">
        <div class="container mx-auto px-6 fade-in-section">
            <div class="flex flex-col md:flex-row justify-between items-end mb-12">
                <div>
                    <h2 class="text-3xl font-bold text-primary mb-2">Portofolio Pilihan</h2>
                    <p class="text-slate-500">Beberapa proyek yang telah saya kerjakan.</p>
                </div>
                <a href="#" class="text-accent font-semibold hover:text-primary mt-4 md:mt-0 transition-colors">Lihat Semua Proyek <i class="fas fa-arrow-right ml-1"></i></a>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                
                <!-- Project 1 -->
                <div class="group bg-white rounded-xl overflow-hidden shadow-lg border border-slate-100 hover:shadow-xl transition-all duration-300">
                    <div class="relative overflow-hidden h-48">
                        <img src="https://placehold.co/600x400/1e293b/FFF?text=Proyek+1" alt="Project 1" class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-primary bg-opacity-0 group-hover:bg-opacity-40 transition-all duration-300 flex items-center justify-center">
                            <a href="#" class="opacity-0 group-hover:opacity-100 bg-white text-primary px-6 py-2 rounded-full font-bold transform translate-y-4 group-hover:translate-y-0 transition-all duration-300">Detail</a>
                        </div>
                    </div>
                    <div class="p-6">
                        <span class="text-xs font-bold text-accent uppercase tracking-wider">Kategori</span>
                        <h3 class="text-xl font-bold text-primary mt-2 mb-2">[Nama Proyek Pertama]</h3>
                        <p class="text-slate-500 text-sm mb-4 line-clamp-2">Deskripsi singkat mengenai proyek ini. Jelaskan masalah yang diselesaikan dan hasil yang dicapai.</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded">Strategy</span>
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded">Design</span>
                        </div>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="group bg-white rounded-xl overflow-hidden shadow-lg border border-slate-100 hover:shadow-xl transition-all duration-300">
                    <div class="relative overflow-hidden h-48">
                        <img src="https://placehold.co/600x400/2563eb/FFF?text=Proyek+2" alt="Project 2" class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-primary bg-opacity-0 group-hover:bg-opacity-40 transition-all duration-300 flex items-center justify-center">
                            <a href="#" class="opacity-0 group-hover:opacity-100 bg-white text-primary px-6 py-2 rounded-full font-bold transform translate-y-4 group-hover:translate-y-0 transition-all duration-300">Detail</a>
                        </div>
                    </div>
                    <div class="p-6">
                        <span class="text-xs font-bold text-accent uppercase tracking-wider">Web Development</span>
                        <h3 class="text-xl font-bold text-primary mt-2 mb-2">[Nama Proyek Kedua]</h3>
                        <p class="text-slate-500 text-sm mb-4 line-clamp-2">Website e-commerce yang meningkatkan penjualan sebesar 20% dalam 3 bulan.</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded">HTML/CSS</span>
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded">React</span>
                        </div>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="group bg-white rounded-xl overflow-hidden shadow-lg border border-slate-100 hover:shadow-xl transition-all duration-300">
                    <div class="relative overflow-hidden h-48">
                        <img src="https://placehold.co/600x400/334155/FFF?text=Proyek+3" alt="Project 3" class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-primary bg-opacity-0 group-hover:bg-opacity-40 transition-all duration-300 flex items-center justify-center">
                            <a href="#" class="opacity-0 group-hover:opacity-100 bg-white text-primary px-6 py-2 rounded-full font-bold transform translate-y-4 group-hover:translate-y-0 transition-all duration-300">Detail</a>
                        </div>
                    </div>
                    <div class="p-6">
                        <span class="text-xs font-bold text-accent uppercase tracking-wider">Mobile App</span>
                        <h3 class="text-xl font-bold text-primary mt-2 mb-2">[Nama Proyek Ketiga]</h3>
                        <p class="text-slate-500 text-sm mb-4 line-clamp-2">Aplikasi manajemen tugas untuk produktivitas tim jarak jauh.</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded">Flutter</span>
                            <span class="px-2 py-1 bg-slate-100 text-slate-600 text-xs rounded">Firebase</span>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-primary text-white">
        <div class="container mx-auto px-6 text-center fade-in-section">
            <h2 class="text-3xl font-bold mb-6">Mari Bekerja Sama</h2>
            <p class="text-slate-400 max-w-2xl mx-auto mb-10">
                Apakah Anda memiliki proyek yang menarik atau tawaran pekerjaan? Saya selalu terbuka untuk mendiskusikan ide baru dan kesempatan kolaborasi.
            </p>
            
            <a href="mailto:emailanda@contoh.com" class="inline-block px-8 py-4 bg-accent text-white font-bold rounded-lg shadow-lg hover:bg-blue-600 transition-all transform hover:-translate-y-1 mb-12">
                Kirim Email ke Saya
            </a>

            <div class="border-t border-slate-700 pt-10 mt-10 grid grid-cols-1 md:grid-cols-3 gap-8 text-center md:text-left">
                <div>
                    <h4 class="font-bold text-lg mb-4 text-white">Kontak</h4>
                    <p class="text-slate-400 text-sm mb-2"><i class="fas fa-envelope mr-2"></i> emailanda@domain.com</p>
                    <p class="text-slate-400 text-sm"><i class="fas fa-phone mr-2"></i> +62 812 3456 7890</p>
                </div>
                <div>
                    <h4 class="font-bold text-lg mb-4 text-white">Lokasi</h4>
                    <p class="text-slate-400 text-sm">Jakarta, Indonesia</p>
                    <p class="text-slate-400 text-sm mt-2">Tersedia untuk Remote / WFH</p>
                </div>
                <div>
                    <h4 class="font-bold text-lg mb-4 text-white">Sosial</h4>
                    <div class="flex space-x-4">
                        <a href="#" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center hover:bg-accent transition-colors"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center hover:bg-accent transition-colors"><i class="fab fa-github"></i></a>
                        <a href="#" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center hover:bg-accent transition-colors"><i class="fab fa-twitter"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="mt-16 text-slate-600 text-sm">
                &copy; 2024 [Nama Anda]. All rights reserved.
            </div>
        </div>
    </section>

    <!-- JavaScript untuk Interaktivitas -->
    <script>
        // 1. Mobile Menu Toggle
        function toggleMenu() {
            const menu = document.getElementById('mobile-menu');
            if (menu.classList.contains('hidden')) {
                menu.classList.remove('hidden');
            } else {
                menu.classList.add('hidden');
            }
        }

        // 2. Intersection Observer untuk Animasi Fade-In
        document.addEventListener('DOMContentLoaded', () => {
            const observerOptions = {
                threshold: 0.1,
                rootMargin: "0px 0px -50px 0px"
            };

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('is-visible');
                        observer.unobserve(entry.target); // Hanya animasi sekali
                    }
                });
            }, observerOptions);

            const sections = document.querySelectorAll('.fade-in-section');
            sections.forEach(section => {
                observer.observe(section);
            });
        });

        // 3. Navbar Effect on Scroll
        window.addEventListener('scroll', () => {
            const nav = document.getElementById('navbar');
            if (window.scrollY > 50) {
                nav.classList.add('shadow-sm');
                nav.style.background = 'rgba(255, 255, 255, 0.95)';
            } else {
                nav.classList.remove('shadow-sm');
                nav.style.background = 'rgba(255, 255, 255, 0.9)';
            }
        });
    </script>
</body>
</html>
