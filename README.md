<!DOCTYPE html>
<html lang="id" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NOKOSHUB - Platform Nomor Virtual WhatsApp & OTP #1 Terbagus Sedunia</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <!-- Chart.js for Admin Analytics -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Canvas Confetti -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#eefbff',
                            100: '#d8f6ff',
                            400: '#38bdf8',
                            500: '#0284c7',
                            600: '#0284c7',
                            900: '#0c4a6e',
                        },
                        wa: {
                            light: '#25D366',
                            dark: '#075E54',
                            deep: '#128C7E'
                        },
                        darkBg: '#060913',
                        cardBg: '#0d1322',
                        glassBg: 'rgba(13, 19, 34, 0.85)'
                    },
                    fontFamily: {
                        orbitron: ['Orbitron', 'sans-serif'],
                        sans: ['Plus Jakarta Sans', 'sans-serif']
                    }
                }
            }
        }
    </script>

    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;900&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap');

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: #060913;
            color: #f1f5f9;
            user-select: none;
            -webkit-tap-highlight-color: transparent;
            overflow-x: hidden;
        }

        .neon-glow-cyan {
            box-shadow: 0 0 25px rgba(56, 189, 248, 0.25);
        }

        .neon-glow-green {
            box-shadow: 0 0 25px rgba(37, 211, 102, 0.3);
        }

        .glass-panel {
            background: rgba(13, 19, 34, 0.88);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(56, 189, 248, 0.15);
        }

        .glass-card {
            background: rgba(18, 26, 47, 0.7);
            border: 1px solid rgba(255, 255, 255, 0.07);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .glass-card:hover {
            border-color: rgba(56, 189, 248, 0.4);
            transform: translateY(-4px);
            box-shadow: 0 12px 30px -5px rgba(2, 132, 199, 0.3);
        }

        .gradient-text-cyan {
            background: linear-gradient(135deg, #38bdf8 0%, #25d366 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        @keyframes marquee {
            0% { transform: translateX(100%); }
            100% { transform: translateX(-100%); }
        }
        .animate-marquee {
            display: inline-block;
            white-space: nowrap;
            animation: marquee 32s linear infinite;
        }
        .animate-marquee:hover { animation-play-state: paused; }

        ::-webkit-scrollbar { width: 6px; height: 6px; }
        ::-webkit-scrollbar-track { background: #060913; }
        ::-webkit-scrollbar-thumb { background: #1e293b; border-radius: 4px; border: 1px solid rgba(56, 189, 248, 0.2); }
        ::-webkit-scrollbar-thumb:hover { background: #0284c7; }
    </style>
</head>
<body class="min-h-screen flex flex-col justify-between">

    <!-- TOP GLOBAL HEADER NAVBAR -->
    <header class="sticky top-0 z-40 glass-panel border-b border-brand-500/20 px-3 md:px-8 py-3.5">
        <div class="max-w-7xl mx-auto flex justify-between items-center gap-3">
            
            <!-- Brand Logo -->
            <div class="flex items-center gap-3 cursor-pointer" onclick="navigateTo('lobby')">
                <div class="w-10 h-10 md:w-11 md:h-11 rounded-2xl bg-gradient-to-tr from-brand-600 via-wa-deep to-wa-light p-0.5 shadow-lg shadow-wa-light/20">
                    <div class="w-full h-full bg-darkBg rounded-[14px] flex items-center justify-center">
                        <i class="fa-brands fa-whatsapp text-wa-light text-2xl"></i>
                    </div>
                </div>
                <div>
                    <div class="flex items-center gap-2">
                        <h1 class="font-orbitron font-black text-lg md:text-2xl gradient-text-cyan tracking-wider leading-none">NOKOSHUB</h1>
                        <span class="hidden sm:inline-flex items-center px-2 py-0.5 rounded-full text-[9px] font-extrabold bg-emerald-500/10 text-emerald-400 border border-emerald-500/30">
                            <span class="w-1.5 h-1.5 rounded-full bg-emerald-400 mr-1 animate-pulse"></span> ONLINE 24/7
                        </span>
                    </div>
                    <span class="text-[9px] text-gray-400 font-bold tracking-widest uppercase block">NOMOR VIRTUAL WA #1 WORLDWIDE</span>
                </div>
            </div>

            <!-- Header Right Section (Balance & Auth Controls) -->
            <div class="flex items-center gap-2 sm:gap-4">
                
                <!-- Authenticated User Balance Container -->
                <div id="navUserBalanceBox" class="flex items-center gap-2.5 bg-gray-950/90 border border-brand-500/40 rounded-xl px-3 py-1.5 shadow-inner">
                    <div class="w-7 h-7 rounded-lg bg-emerald-500/10 border border-emerald-500/30 flex items-center justify-center text-emerald-400 text-xs">
                        <i class="fa-solid fa-wallet"></i>
                    </div>
                    <div class="flex flex-col">
                        <span class="text-[9px] text-gray-400 font-bold uppercase leading-none">Saldo Nokos</span>
                        <span class="font-orbitron font-black text-xs md:text-sm text-emerald-400 leading-tight" id="userBalanceDisplay">Rp 50.000</span>
                    </div>
                </div>

                <!-- Deposit Button -->
                <button onclick="openModal('depositModal')" class="bg-gradient-to-r from-emerald-500 to-teal-600 hover:brightness-110 text-black font-black px-3.5 py-2 rounded-xl text-xs flex items-center gap-1.5 shadow-lg shadow-emerald-500/20 transition">
                    <i class="fa-solid fa-qrcode text-sm"></i> <span class="hidden sm:inline">DEPOSIT QRIS</span>
                </button>

                <!-- Auth Buttons Toggle -->
                <div id="authButtonsContainer">
                    <button onclick="openModal('authModal')" id="btnLoginRegister" class="bg-gradient-to-r from-brand-500 to-sky-400 hover:brightness-110 text-black font-black px-4 py-2 rounded-xl text-xs font-orbitron uppercase shadow-lg shadow-brand-500/20">
                        LOGIN / DAFTAR
                    </button>
                    
                    <button onclick="logoutUser()" id="btnLogout" class="hidden bg-gray-900 border border-red-500/40 hover:bg-red-500/20 text-red-400 font-bold px-3 py-2 rounded-xl text-xs transition">
                        <i class="fa-solid fa-right-from-bracket"></i>
                    </button>
                </div>

            </div>
        </div>
    </header>

    <!-- LIVE ORDERS TICKER & AUDIO CONTROL -->
    <div class="bg-gray-950/95 border-b border-gray-800/80 py-1.5 px-4 flex items-center justify-between text-xs text-gray-300">
        <div class="flex items-center gap-2 overflow-hidden w-full">
            <span class="flex items-center gap-1 bg-wa-light/10 text-wa-light text-[9px] font-extrabold px-2.5 py-0.5 rounded-md uppercase tracking-wider border border-wa-light/30 whitespace-nowrap">
                <i class="fa-solid fa-bolt animate-pulse"></i> LIVE ORDER
            </span>
            <div class="overflow-hidden w-full relative">
                <div class="animate-marquee font-medium space-x-8 text-[11px]" id="liveTickerOrders">
                    <span>📱 <b class="text-white">Robi_99</b> baru saja membeli <b class="text-emerald-400">Nomor WA Indonesia (+62)</b> - Rp 3.500</span>
                    <span>🇺🇸 <b class="text-white">Budi_Sultan</b> sukses verifikasi OTP <b class="text-cyan-400">Nomor WA USA (+1)</b></span>
                    <span>⚡ <b class="text-white">Siska_Gacor</b> Deposit QRIS Instant <b class="text-yellow-400">Rp 100.000</b> (Berhasil)</span>
                    <span>🇲🇾 <b class="text-white">Ahmad_KL</b> membeli <b class="text-emerald-400">Nomor WA Malaysia (+60)</b> - Rp 5.500</span>
                </div>
            </div>
        </div>
        <button onclick="toggleAudio()" class="ml-4 text-gray-400 hover:text-brand-400 text-xs flex items-center gap-1 whitespace-nowrap">
            <i class="fa-solid fa-volume-high" id="audioIcon"></i> <span class="hidden md:inline">Audio FX</span>
        </button>
    </div>

    <!-- MAIN BODY CONTENT -->
    <main class="max-w-7xl mx-auto flex-1 w-full px-3 md:px-8 py-6 space-y-8">

        <!-- HERO BANNER HUB -->
        <div class="relative overflow-hidden rounded-3xl glass-panel p-6 md:p-10 border border-brand-500/30 shadow-2xl">
            <div class="absolute -right-20 -bottom-20 w-96 h-96 bg-brand-500/10 rounded-full blur-3xl pointer-events-none"></div>
            <div class="absolute -left-20 -top-20 w-80 h-80 bg-wa-light/10 rounded-full blur-3xl pointer-events-none"></div>

            <div class="relative z-10 max-w-3xl space-y-4">
                <div class="inline-flex items-center gap-2 bg-gradient-to-r from-emerald-500/20 to-brand-500/20 border border-emerald-500/40 text-emerald-300 text-[10px] font-black px-3.5 py-1 rounded-full uppercase tracking-wider">
                    <i class="fa-solid fa-shield-halved text-emerald-400"></i> DUKUNGAN OTP WA TERCEPAT & TERLENGKAP DI DUNIA
                </div>
                
                <h2 class="text-3xl md:text-5xl font-orbitron font-black text-white leading-tight">
                    Beli Nomor Virtual WA <span class="gradient-text-cyan">Semua Negara</span>
                </h2>
                
                <p class="text-xs md:text-sm text-gray-300 leading-relaxed">
                    Dapatkan nomor virtual WhatsApp aktif dari 30+ negara di seluruh dunia secara instan. Tanpa perlu kartu perdana fisik, OTP masuk otomatis dalam hitungan detik. Garansi saldo kembali jika SMS tidak masuk!
                </p>

                <!-- Platform Quick Stats -->
                <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 pt-2">
                    <div class="glass-card p-3 rounded-2xl border border-gray-800 text-center">
                        <span class="text-[10px] text-gray-400 font-bold block uppercase">Negara Tersedia</span>
                        <span class="font-orbitron font-black text-base text-brand-400">30+ Negara</span>
                    </div>
                    <div class="glass-card p-3 rounded-2xl border border-gray-800 text-center">
                        <span class="text-[10px] text-gray-400 font-bold block uppercase">Kecepatan OTP</span>
                        <span class="font-orbitron font-black text-base text-emerald-400">&lt; 10 Detik</span>
                    </div>
                    <div class="glass-card p-3 rounded-2xl border border-gray-800 text-center">
                        <span class="text-[10px] text-gray-400 font-bold block uppercase">Metode Deposit</span>
                        <span class="font-orbitron font-black text-base text-yellow-400">QRIS All Bank</span>
                    </div>
                    <div class="glass-card p-3 rounded-2xl border border-gray-800 text-center">
                        <span class="text-[10px] text-gray-400 font-bold block uppercase">Tingkat Sukses</span>
                        <span class="font-orbitron font-black text-base text-wa-light">99.8%</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- ACTIVE ORDERS / RECENT OTP PANEL (IF ANY) -->
        <div id="activeOrdersContainer" class="hidden space-y-4">
            <div class="flex items-center justify-between">
                <h3 class="font-orbitron font-bold text-lg text-white flex items-center gap-2">
                    <i class="fa-solid fa-spinner animate-spin text-brand-400"></i> Nomor WA Aktif & Menunggu OTP
                </h3>
            </div>
            <div id="activeOrdersList" class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <!-- Active Numbers Dynamically Rendered Here -->
            </div>
        </div>

        <!-- STORE CONTROLS: SEARCH & CATEGORY FILTERS -->
        <div class="space-y-4">
            <div class="flex flex-col md:flex-row items-center justify-between gap-4">
                
                <!-- Filter Tabs -->
                <div class="flex items-center gap-2 overflow-x-auto w-full md:w-auto pb-2 md:pb-0">
                    <button onclick="filterCategory('all')" class="cat-btn active bg-brand-500 text-black font-black px-4 py-2 rounded-xl text-xs whitespace-nowrap shadow-md">Semua Negara</button>
                    <button onclick="filterCategory('popular')" class="cat-btn glass-card text-gray-300 font-bold px-4 py-2 rounded-xl text-xs whitespace-nowrap hover:text-brand-400">🔥 Populer</button>
                    <button onclick="filterCategory('murah')" class="cat-btn glass-card text-gray-300 font-bold px-4 py-2 rounded-xl text-xs whitespace-nowrap hover:text-brand-400">💰 Paling Murah</button>
                    <button onclick="filterCategory('asia')" class="cat-btn glass-card text-gray-300 font-bold px-4 py-2 rounded-xl text-xs whitespace-nowrap hover:text-brand-400">🌏 Asia</button>
                    <button onclick="filterCategory('eropa')" class="cat-btn glass-card text-gray-300 font-bold px-4 py-2 rounded-xl text-xs whitespace-nowrap hover:text-brand-400">🇪🇺 Eropa</button>
                    <button onclick="filterCategory('amerika')" class="cat-btn glass-card text-gray-300 font-bold px-4 py-2 rounded-xl text-xs whitespace-nowrap hover:text-brand-400">🌎 Amerika</button>
                </div>

                <!-- Search Input -->
                <div class="relative w-full md:w-72">
                    <i class="fa-solid fa-magnifying-glass absolute left-3.5 top-3 text-gray-500 text-xs"></i>
                    <input type="text" id="countrySearchInput" onkeyup="searchCountry()" placeholder="Cari negara (cth: Indonesia, USA...)" class="w-full bg-gray-950/90 border border-gray-800 rounded-xl pl-9 pr-4 py-2 text-xs text-white placeholder-gray-500 focus:outline-none focus:border-brand-500">
                </div>
            </div>

            <!-- VIRTUAL NUMBER STORE GRID -->
            <div id="countryGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4">
                <!-- Country Cards Rendered via JS -->
            </div>
        </div>

        <!-- USER ORDER HISTORY TABLE SECTION -->
        <div class="glass-panel rounded-3xl p-5 md:p-6 border border-gray-800 space-y-4 shadow-xl">
            <div class="flex items-center justify-between border-b border-gray-800 pb-3">
                <div>
                    <h3 class="font-orbitron font-bold text-base md:text-lg text-white">Riwayat Transaksi & Order</h3>
                    <p class="text-xs text-gray-400">Daftar pemesanan nomor virtual WA dan status verifikasi OTP</p>
                </div>
                <button onclick="renderOrderHistory()" class="text-xs text-brand-400 hover:underline flex items-center gap-1 font-bold">
                    <i class="fa-solid fa-rotate"></i> Refresh
                </button>
            </div>

            <div class="overflow-x-auto">
                <table class="w-full text-left text-xs">
                    <thead>
                        <tr class="border-b border-gray-800 text-gray-400">
                            <th class="p-3">ID Order</th>
                            <th class="p-3">Negara</th>
                            <th class="p-3">Nomor Virtual</th>
                            <th class="p-3">Harga</th>
                            <th class="p-3">Kode OTP</th>
                            <th class="p-3">Status</th>
                        </tr>
                    </thead>
                    <tbody id="orderHistoryTableBody" class="divide-y divide-gray-800/60 text-gray-300">
                        <!-- Dynamic Rows -->
                    </tbody>
                </table>
            </div>
        </div>

        <!-- FAQ ACCORDION SECTION -->
        <div class="glass-panel rounded-3xl p-6 border border-gray-800 space-y-4">
            <h3 class="font-orbitron font-bold text-lg text-white text-center">Pertanyaan Sering Diajukan (FAQ)</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div class="glass-card p-4 rounded-2xl space-y-1">
                    <h4 class="font-bold text-xs text-brand-400">Bagaimana jika OTP WhatsApp tidak kunjung masuk?</h4>
                    <p class="text-[11px] text-gray-300">Jika dalam waktu 5 menit OTP tidak diterima, Anda dapat menekan tombol Batal/Refund. Saldo Anda akan otomatis dikembalikan 100% tanpa potongan!</p>
                </div>
                <div class="glass-card p-4 rounded-2xl space-y-1">
                    <h4 class="font-bold text-xs text-brand-400">Berapa lama batas waktu nomor virtual berlaku?</h4>
                    <p class="text-[11px] text-gray-300">Nomor virtual aktif selama 15-20 menit sejak dibeli untuk menerima kode verifikasi OTP WhatsApp.</p>
                </div>
                <div class="glass-card p-4 rounded-2xl space-y-1">
                    <h4 class="font-bold text-xs text-brand-400">Apakah deposit QRIS diproses otomatis?</h4>
                    <p class="text-[11px] text-gray-300">Ya, sistem QRIS kami terhubung ke Gateway Otomatis 24/7. Saldo akan langsung masuk ke akun Anda dalam hitungan detik setelah pembayaran.</p>
                </div>
                <div class="glass-card p-4 rounded-2xl space-y-1">
                    <h4 class="font-bold text-xs text-brand-400">Apakah nomor yang dibeli bisa dipakai ulang?</h4>
                    <p class="text-[11px] text-gray-300">Nomor bersifat sekali pakai khusus untuk verifikasi pendaftaran akun WhatsApp baru atau ganti nomor.</p>
                </div>
            </div>
        </div>

    </main>

    <!-- FOOTER SECTION -->
    <footer class="bg-gray-950 border-t border-gray-800 py-6 px-4 text-center text-xs text-gray-500 space-y-2 mt-8">
        <div class="flex items-center justify-center gap-2">
            <i class="fa-brands fa-whatsapp text-emerald-400 text-lg"></i>
            <span class="font-orbitron font-bold text-white">NOKOSHUB GLOBAL ENGINE</span>
        </div>
        <p>© 2026 NOKOSHUB - Platform Penyedia Nomor Virtual WhatsApp Terbagus & Terpercaya di Indonesia.</p>
    </footer>

    <!-- FLOATING MASTER ADMIN CONTROL BUTTON -->
    <button onclick="toggleAdminModal()" class="fixed bottom-20 md:bottom-8 right-6 z-40 bg-gradient-to-r from-purple-900 to-indigo-900 hover:brightness-125 border-2 border-purple-400 text-purple-200 px-4 py-3 rounded-2xl shadow-2xl flex items-center gap-3 font-extrabold text-xs transition transform hover:scale-105">
        <i class="fa-solid fa-user-gear text-lg text-brand-400 animate-pulse"></i>
        <span>PANEL MASTER ADMIN</span>
    </button>

    <!-- MOBILE BOTTOM NAVIGATION -->
    <nav class="fixed botto
