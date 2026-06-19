<!DOCTYPE html>
<html lang="fr text-right">
<head>
        <link rel="icon" href="favicon.png.jpeg">
        <meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link rel="icon" type="image/x-icon" href="favicon.ico">
<link rel="apple-touch-icon" href="favicon-512.png">

<title>TAGORA NFC - Smart NFC Stickers & Cards Morocco</title>
    <!-- Tailwind CSS CDN -->
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Fonts Import -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Orbitron:wght@600;700;800;900&display=swap" rel="stylesheet">
    <!-- Lucide Icons CDN -->
    <script src="https://unpkg.com/lucide@latest"></script>
    
    <!-- Tailwind Configuration -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ["Inter", "ui-sans-serif", "system-ui", "-apple-system", "sans-serif"],
                        orbitron: ["Orbitron", "sans-serif"]
                    },
                    colors: {
                        brand: {
                            cyan: "#18c8ff",
                            blue: "#0077ff",
                            dark: "#02050b",
                            card: "rgba(255, 255, 255, 0.05)"
                        }
                    }
                }
            }
        }
    </script>

    <!-- Custom Styling & Animations -->
    <style>
        /* Grille futuriste 3D animée en arrière-plan */
        .retro-grid {
            position: absolute;
            inset: 0;
            background-image: 
                linear-gradient(rgba(24, 200, 255, 0.04) 1px, transparent 1px),
                linear-gradient(90deg, rgba(24, 200, 255, 0.04) 1px, transparent 1px);
            background-size: 50px 50px;
            transform: perspective(600px) rotateX(60deg) translateY(-120px) translateZ(0);
            transform-origin: top;
            animation: gridMove 18s linear infinite;
            z-index: 1;
            pointer-events: none;
        }

        @keyframes gridMove {
            0% { background-position: 0 0; }
            100% { background-position: 0 50px; }
        }

        /* Effets de halo néon */
        .glow-cyan {
            box-shadow: 0 0 25px rgba(24, 200, 255, 0.2);
        }
        .glow-cyan-strong {
            box-shadow: 0 0 35px rgba(24, 200, 255, 0.5);
        }
        .glow-blue {
            box-shadow: 0 0 25px rgba(0, 119, 255, 0.25);
        }

        /* Panneaux effet verre dépoli */
        .glass-panel {
            background: rgba(10, 18, 36, 0.65);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(24, 200, 255, 0.12);
        }

        .glass-panel-hover {
            transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .glass-panel-hover:hover {
            background: rgba(10, 18, 36, 0.85);
            border-color: rgba(24, 200, 255, 0.35);
            box-shadow: 0 0 30px rgba(24, 200, 255, 0.15);
            transform: translateY(-4px);
        }

        /* Barre de défilement personnalisée */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #02050b;
        }
        ::-webkit-scrollbar-thumb {
            background: rgba(24, 200, 255, 0.25);
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: rgba(24, 200, 255, 0.45);
        }

        /* Alignements de langues */
        .rtl {
            direction: rtl;
        }
        .ltr {
            direction: ltr;
        }


        /* Splash screen TAGORA NFC */
        #tagora-splash-screen {
            position: fixed;
            inset: 0;
            z-index: 99999;
            background: #050505;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            transition: opacity .7s ease, visibility .7s ease;
        }
        #tagora-splash-screen.hide-splash {
            opacity: 0;
            visibility: hidden;
            pointer-events: none;
        }
        .tagora-splash-box {
            transform: translateY(35px);
            animation: tagoraIntro .9s ease forwards;
        }
        .tagora-splash-title {
            font-family: Orbitron, Inter, sans-serif;
            font-size: clamp(46px, 11vw, 76px);
            line-height: .9;
            font-weight: 900;
            letter-spacing: -2px;
            color: white;
            text-transform: uppercase;
            text-shadow: 0 0 22px rgba(255,255,255,.12);
        }
        .tagora-splash-title span {
            display: block;
            color: #18c8ff;
            margin-top: 10px;
            text-shadow: 0 0 28px rgba(24,200,255,.55);
        }
        .tagora-splash-subtitle {
            margin-top: 30px;
            color: rgba(255,255,255,.42);
            font-size: 13px;
            letter-spacing: 7px;
            font-weight: 700;
            text-transform: uppercase;
        }
        .tagora-splash-bar {
            width: min(360px, 68vw);
            height: 5px;
            margin: 34px auto 0;
            background: rgba(255,255,255,.10);
            border-radius: 50px;
            overflow: hidden;
        }
        .tagora-splash-bar::before {
            content: '';
            display: block;
            width: 100%;
            height: 100%;
            border-radius: 50px;
            background: linear-gradient(90deg, #0077ff, #18c8ff, #ffffff);
            transform-origin: left;
            animation: tagoraLoad 2.2s ease forwards;
        }
        @keyframes tagoraLoad {
            from { transform: scaleX(0); }
            to { transform: scaleX(1); }
        }
        @keyframes tagoraIntro {
            to { transform: translateY(0); }
        }

    </style>
</head>
<body class="bg-brand-dark overflow-x-hidden text-white font-sans relative">
    <!-- DAKHLA / Splash Screen TAGORA NFC -->
    <div id="tagora-splash-screen">
        <div class="tagora-splash-box">
            <div class="tagora-splash-title">TAGORA<span>NFC</span></div>
            <div class="tagora-splash-subtitle">Smart NFC Technology</div>
            <div class="tagora-splash-bar"></div>
        </div>
    </div>


    <!-- Grille futuriste animée -->
    <div class="retro-grid"></div>

    <!-- Halos de lumière décoratifs -->
    <div class="absolute top-1/4 left-[10%] w-96 h-96 rounded-full bg-cyan-700/10 blur-[130px] pointer-events-none z-0"></div>
    <div class="absolute top-2/3 right-[10%] w-[450px] h-[450px] rounded-full bg-blue-700/10 blur-[130px] pointer-events-none z-0"></div>

    <!-- BARRE DE NAVIGATION (FIXE) -->
    <nav class="fixed top-0 inset-x-0 h-20 bg-neutral-950/85 backdrop-blur-md border-b border-brand-cyan/15 z-50 transition-all duration-300">
        <div class="max-w-7xl mx-auto h-full px-4 md:px-8 flex items-center justify-between">
            
            <!-- Logo principal -->
            <div class="flex items-center gap-3 cursor-pointer" onclick="scrollToSection('home-section')">
                <div class="flex flex-col">
                    <span class="font-orbitron font-black text-lg md:text-xl tracking-widest text-white">
                        TAGORA<span class="text-brand-cyan">.NFC</span>
                    </span>
                    <span class="text-[9px] text-zinc-500 uppercase tracking-widest font-mono font-bold">Smart Tech Morocco</span>
                </div>
            </div>

            <!-- Liens de navigation (Bureau) -->
            <div class="hidden lg:flex items-center gap-8 text-sm font-semibold tracking-wide text-zinc-300">
                <button onclick="scrollToSection('home-section')" class="hover:text-brand-cyan transition-colors">Accueil</button>
                <button onclick="scrollToSection('products-section')" class="hover:text-brand-cyan transition-colors">Nos Produits</button>
                <button onclick="scrollToSection('simulator-section')" class="hover:text-brand-cyan transition-colors">Simulateur Tap</button>
                <button onclick="scrollToSection('why-tagora')" class="hover:text-brand-cyan transition-colors font-bold bg-brand-cyan/5 px-3 py-1 rounded-md border border-brand-cyan/10">Pourquoi Nous ?</button>
                <button onclick="scrollToSection('faq-section')" class="hover:text-brand-cyan transition-colors">FAQ</button>
            </div>

            <!-- Sélections d'actions rapides -->
            <div class="hidden sm:flex items-center gap-4">
                <!-- Sélecteur de langue -->
                <div class="flex bg-zinc-900 border border-zinc-800 rounded-full p-1 text-xs font-bold">
                    <button id="lang-btn-fr" onclick="changeLanguage('fr')" class="px-3 py-1.5 rounded-full transition bg-brand-cyan text-black">
                        Français
                    </button>
                    <button id="lang-btn-ar" onclick="changeLanguage('ar')" class="px-3 py-1.5 rounded-full transition text-zinc-400 hover:text-white">
                        عربي
                    </button>
                </div>

                <button onclick="scrollToSection('order-section')" class="bg-gradient-to-r from-brand-blue to-brand-cyan text-black font-black px-5 py-2.5 rounded-full text-xs uppercase tracking-wider transition-transform hover:scale-[1.03] active:scale-[0.98] glow-blue">
                    Commander / اطلب الآن
                </button>
            </div>

            <!-- Boutons de contrôle pour mobiles -->
            <div class="lg:hidden flex items-center gap-3">
                <button onclick="toggleMobileLanguage()" class="px-2.5 py-1 rounded bg-zinc-900 border border-zinc-800 text-[11px] font-black text-brand-cyan uppercase tracking-wider">
                    <span id="mobile-lang-label">عربي</span>
                </button>
                <button onclick="toggleMobileMenu()" class="p-1 rounded bg-zinc-900 border border-zinc-800 text-zinc-300">
                    <i data-lucide="menu" id="mobile-menu-icon" class="w-6 h-6"></i>
                </button>
            </div>

        </div>
    </nav>

    <!-- MENU MOBILE UNIQUE -->
    <div id="mobile-drawer" class="hidden fixed top-20 left-0 right-0 z-40 bg-zinc-950 border-b border-brand-cyan/20 p-6 flex flex-col gap-4 text-center text-base shadow-2xl glass-panel">
        <button onclick="scrollToSection('home-section'); toggleMobileMenu()" class="py-2 hover:text-brand-cyan font-bold transition">Accueil / الرئيسية</button>
        <button onclick="scrollToSection('products-section'); toggleMobileMenu()" class="py-2 hover:text-brand-cyan font-bold transition">Nos Produits / منتجاتنا</button>
        <button onclick="scrollToSection('simulator-section'); toggleMobileMenu()" class="py-2 hover:text-brand-cyan font-bold transition">Simulateur Tap / معايشة حية</button>
        <button onclick="scrollToSection('why-tagora'); toggleMobileMenu()" class="py-2 hover:text-brand-cyan font-bold transition">Pourquoi Nous / لماذا طاجور</button>
        <button onclick="scrollToSection('faq-section'); toggleMobileMenu()" class="py-2 hover:text-brand-cyan font-bold transition">FAQ / الأسئلة الشائعة</button>
        <button onclick="scrollToSection('order-section'); toggleMobileMenu()" class="mt-2 bg-gradient-to-r from-brand-blue to-brand-cyan text-black font-black p-3 rounded-xl uppercase text-xs tracking-wider">
            Passer une Commande
        </button>
    </div>

    <!-- SECTION PRINCIPALE (HERO) -->
    <section id="home-section" class="pt-32 pb-16 md:py-40 px-4 md:px-8 max-w-7xl mx-auto relative z-10">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
            
            <!-- Bloc de texte gauche -->
            <div class="lg:col-span-6 space-y-6 text-center lg:text-left">
                
                <div class="inline-flex items-center gap-2 bg-brand-cyan/10 border border-brand-cyan/20 px-4 py-1.5 rounded-full text-xs text-brand-cyan font-black uppercase tracking-widest leading-none">
                    <i data-lucide="clock" class="w-3.5 h-3.5 text-brand-cyan"></i>
                    <span id="hero-badge">Maroc Livraison Gratuite - الدفع عند الاستلام</span>
                </div>

                <h1 class="text-4xl sm:text-5xl md:text-6xl font-black font-orbitron tracking-tighter leading-[0.95] uppercase">
                    TAP, CONNECT <br>
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-brand-cyan via-blue-400 to-indigo-500 font-extrabold">
                        & IMPRESS.
                    </span>
                </h1>

                <!-- Paragraphe Français -->
                <div id="intro-fr" class="space-y-4 font-sans text-stone-300">
                    <p class="text-lg md:text-xl leading-relaxed font-semibold">
                        Mettez en avant vos réseaux sociaux et récoltez des avis Google Reviews 5 étoiles en moins de 3 secondes grâce à nos Stickers & Cartes NFC intelligents !
                    </p>
                    <p class="text-sm text-zinc-400 leading-relaxed max-w-xl">
                        Un simple tap du téléphone d’un client suffit pour ouvrir instantanément votre compte Instagram, TikTok, page d’examen Google ou envoyer un WhatsApp. Convient pour voitures, vitrines et accueils.
                    </p>
                </div>

                <!-- Paragraphe Arabe -->
                <div id="intro-ar" class="hidden space-y-4 font-sans text-stone-300 text-right rtl">
                    <p class="text-lg md:text-xl leading-relaxed font-bold">
                        متابعون جدد وتقييمات قوقل 5 نجوم لعملك بكبسة زر واحدة من هاتف زبونك!
                    </p>
                    <p class="text-sm text-zinc-400 leading-relaxed max-w-xl ml-auto">
                        قرب هاتف الزبون للستيكر الذكي ليفتح حسابه فورياً على صفحة التقييمات، حساب انستقرام أو تيك توك الخاص بمشروعك. سهل، مبتكر، ومناسب تماماً لسيارات الأجرة، واجهات المقاهي والشركات.
                    </p>
                </div>

                <!-- Statistiques rapides -->
                <div class="grid grid-cols-3 gap-3 pt-2 text-center max-w-md mx-auto lg:mx-0">
                    <div class="bg-zinc-900/40 border border-zinc-800 p-3 rounded-xl">
                        <b class="block text-2xl font-orbitron text-brand-cyan">1Tap</b>
                        <span class="text-[10px] text-zinc-400 uppercase tracking-widest font-semibold block mt-0.5">Connexion</span>
                    </div>
                    <div class="bg-zinc-900/40 border border-zinc-800 p-3 rounded-xl">
                        <b class="block text-2xl font-orbitron text-brand-cyan">100%</b>
                        <span class="text-[10px] text-zinc-400 uppercase tracking-widest font-semibold block mt-0.5">Sans App</span>
                    </div>
                    <div class="bg-zinc-900/40 border border-zinc-800 p-3 rounded-xl">
                        <b class="block text-2xl font-orbitron text-brand-cyan">24H</b>
                        <span class="text-[10px] text-zinc-400 uppercase tracking-widest font-semibold block mt-0.5">Livraison</span>
                    </div>
                </div>

                <!-- Actions d'achat rapides -->
                <div class="flex flex-wrap items-center justify-center lg:justify-start gap-4 pt-3">
                    <button onclick="scrollToSection('products-section')" class="bg-brand-cyan hover:bg-brand-cyan/90 text-black font-black px-8 py-4 rounded-full text-sm uppercase tracking-wider transition-transform hover:scale-102 flex items-center gap-2 shadow-lg shadow-brand-cyan/20">
                        <i data-lucide="shopping-bag" class="w-4 h-4 stroke-[2.5]"></i>
                        <span>Acheter / اطلب الآن</span>
                    </button>
                    
                </div>

                <div class="text-xs text-zinc-500 font-medium flex items-center justify-center lg:justify-start gap-1.5 pt-1">
                    <span class="inline-block w-2.5 h-2.5 rounded-full bg-emerald-500 animate-ping"></span>
                    <span id="hero-shipping-text">🇲🇦 Livraison express gratuite sur Casablanca, Rabat, Marrakech et tout le Maroc !</span>
                </div>

            </div>

            </div>

        </div>
    </section
                        
                        <!-- Étape de chargement de puce NFC -->
                        <div id="screen-state-loading" class="hidden absolute inset-0 flex flex-col items-center justify-center bg-black text-center px-4">
                            <div class="font-orbitron font-black text-4xl leading-none tracking-tight text-white">TAGORA</div>
                            <div class="font-orbitron font-black text-4xl leading-none tracking-tight text-brand-cyan mt-2 drop-shadow-[0_0_18px_rgba(24,200,255,0.65)]">NFC</div>
                            <span class="text-zinc-500 text-[10px] mt-6 font-mono uppercase tracking-[0.35em]">Smart NFC Technology</span>
                            <div class="w-44 h-1 bg-zinc-800 rounded-full overflow-hidden mt-8">
                                <div class="h-full w-2/3 bg-gradient-to-r from-brand-blue via-brand-cyan to-white rounded-full"></div>
                            </div>
                        </div>

                        <!-- Application finale simulée (Instagram, Google ...) -->
                        <div id="screen-state-app" class="hidden absolute inset-0 h-full w-full bg-zinc-950 text-white"></div>

                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- SECTION CATALOGUE DE PRODUITS -->
    <section id="products-section" class="py-20 px-4 md:px-8 max-w-7xl mx-auto relative z-10">
        
        <div class="text-center max-w-2xl mx-auto mb-16">
            <span class="text-xs text-brand-cyan md:text-sm font-black font-orbitron uppercase tracking-widest">Achat Unique - Sans Aucun Abonnement</span>
            <h2 class="text-3xl md:text-5xl font-black font-orbitron tracking-tight text-white uppercase mt-1">
                NOS PRODUITS <span class="text-brand-cyan">TAGORA</span>
            </h2>
            <p class="text-zinc-400 text-sm md:text-base mt-2">
                Des stickers robustes et des cartes de haute qualité fabriqués sur mesure pour booster votre présence locale au Maroc.
            </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
            
            <!-- Produit 1 : Tagore Sticker -->
            <div class="glass-panel glass-panel-hover rounded-3xl overflow-hidden border border-zinc-800 relative flex flex-col justify-between">
                <div class="absolute top-4 left-4 z-20 bg-brand-cyan text-black px-3 py-1 rounded-full text-xs font-black font-orbitron shadow-lg uppercase tracking-wide">
                    Le Plus Populaire / الأكثر طلباً
                </div>

                <!-- Zone Image illustrative -->
                <div class="relative aspect-video w-full bg-zinc-950 overflow-hidden border-b border-zinc-900">
            <img src="c:\Users\hp\Downloads\WhatsApp Image 2026-06-19 at 04.19.14.jpeg" alt="">
                </div>
                <div class="p-6 md:p-8 flex-1 flex flex-col justify-between space-y-6">
                    <div>
                        <h3 class="text-2xl font-black font-orbitron text-zinc-100">Tagore Sticker NFC</h3>
                        <p class="text-xs text-zinc-400 font-medium leading-relaxed mt-2">
                            Le compagnon parfait pour votre voiture, taxi, vitrine ou comptoir d'accueil. Partagez vos pages d'avis ou profils réseaux en 1 seconde.
                        </p>

                        <div class="border-t border-zinc-900/65 pt-4 mt-4 text-xs">
                            <h5 class="font-bold text-zinc-300 uppercase tracking-widest mb-2 flex items-center gap-1">
                                <i data-lucide="sparkles" class="w-3.5 h-3.5 text-brand-cyan"></i>
                                <span>Caractéristiques / المميزات :</span>
                            </h5>
                            <ul class="space-y-1.5 text-zinc-400 font-sans">
                                <li class="flex items-center gap-2"><i data-lucide="check" class="w-3.5 h-3.5 text-brand-cyan shrink-0"></i> <span>Résistant au soleil et à l’eau</span></li>
                                <li class="flex items-center gap-2"><i data-lucide="check" class="w-3.5 h-3.5 text-brand-cyan shrink-0"></i> <span>Aucune batterie requise, fonctionne à vie</span></li>
                                <li class="flex items-center gap-2"><i data-lucide="check" class="w-3.5 h-3.5 text-brand-cyan shrink-0"></i> <span>Installation facile (Adhésif fort 3M)</span></li>
                            </ul>
                        </div>
                    </div>

                    <div class="border-t border-zinc-800 pt-5 flex items-center justify-between">
                        <div>
                            <span class="block text-[10px] text-zinc-500 uppercase tracking-wider">Unité / سعر الحبة</span>
                            <div class="flex items-baseline gap-2 mt-1">
                                <span class="text-brand-cyan text-3xl font-black font-orbitron shrink-0">149 DH</span>
                                <span class="text-zinc-600 line-through text-xs">199 DH</span>
                            </div>
                        </div>
                            
                            <i data-lucide="arrow-right" class="w-4 h-4"></i>
                        </button>
                    </div>
                </div>
            </div>

            <!-- Produit 2 : Carte Infinities -->      
</button>
</button>
            <div class="glass-panel glass-panel-hover rounded-3xl overflow-hidden border border-zinc-800 relative flex flex-col justify-between">
                <div class="absolute top-4 left-4 z-20 bg-brand-cyan text-black px-3 py-1 rounded-full text-xs font-black font-orbitron shadow-lg uppercase tracking-wide">
                    Professionnels & Business
                </div>

                <div class="relative aspect-video w-full bg-zinc-950 overflow-hidden border-b border-zinc-900">
                    <img 
                    <div class="absolute inset-0 bg-gradient-to-t from-zinc-950 via-transparent to-transparent pointer-events-none"></div>
                </div>

                <div class="p-6 md:p-8 flex-1 flex flex-col justify-between space-y-6">
                    <div>
                        <h3 class="text-2xl font-black font-orbitron text-zinc-100">Google Reviews NFC Card </h3>
                        <p class="text-xs text-zinc-400 font-medium leading-relaxed mt-2">
                            La carte ultime pour les restaurants, cafés, cabinets dentaires, agences et salons. Invitez vos clients à laisser un avis 5 étoiles à la caisse.
                        </p>

                        <div class="border-t border-zinc-900/65 pt-4 mt-4 text-xs">
                            <h5 class="font-bold text-zinc-300 uppercase tracking-widest mb-2 flex items-center gap-1">
                                <i data-lucide="sparkles" class="w-3.5 h-3.5 text-brand-cyan"></i>
                                <span>Caractéristiques / المميزات :</span>
                            </h5>
                            <ul class="space-y-1.5 text-zinc-400 font-sans">
                                <li class="flex items-center gap-2"><i data-lucide="check" class="w-3.5 h-3.5 text-brand-cyan shrink-0"></i> <span>Finition mate noire de haute qualité</span></li>
                                <li class="flex items-center gap-2"><i data-lucide="check" class="w-3.5 h-3.5 text-brand-cyan shrink-0"></i> <span>QR code au dos imprimé haute précision</span></li>
                                <li class="flex items-center gap-2"><i data-lucide="check" class="w-3.5 h-3.5 text-brand-cyan shrink-0"></i> <span>Ré-écriture possible de votre lien</span></li>
                            </ul>
                        </div>
                    </div>

                    <div class="border-t border-zinc-800 pt-5 flex items-center justify-between">
                        <div>
                            <span class="block text-[10px] text-zinc-500 uppercase tracking-wider">Unité / سعر الحبة</span>
                            <div class="flex items-baseline gap-2 mt-1">
                                <span class="text-brand-cyan text-3xl font-black font-orbitron shrink-0">249 DH</span>
                                <span class="text-zinc-600 line-through text-xs">349 DH</span>
                            </div>
                        </div>
                         

</button>
                            <i data-lucide="arrow-right" class="w-4 h-4"></i>
                        </button>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- FORMULAIRE DE COMMANDE EXCLUSIF / CONFIGURATEUR INTELLIGENT -->
    <section id="order-section" class="py-20 px-4 md:px-8 max-w-7xl mx-auto relative z-10">
        <div class="glass-panel rounded-3xl p-6 md:p-8 max-w-5xl mx-auto shadow-2xl relative overflow-hidden">
            
            <div class="absolute top-0 right-0 w-64 h-64 bg-cyan-500/5 rounded-full blur-3xl pointer-events-none"></div>
            <div class="absolute bottom-0 left-0 w-64 h-64 bg-blue-500/5 rounded-full blur-3xl pointer-events-none"></div>

            <div class="text-center mb-8 border-b border-zinc-800 pb-6">
                <div class="flex justify-center items-center gap-1.5 text-xs text-brand-cyan md:text-sm font-bold uppercase tracking-widest mb-2 font-orbitron">
                    <i data-lucide="sparkles" class="w-4 h-4"></i>
                    <span>Commande Rapide - Livraison Gratuite</span>
                </div>
                <h3 class="text-3xl md:text-4xl font-black font-orbitron tracking-tight text-white uppercase">
                    FORMULAIRE DE <span class="text-brand-cyan">COMMANDE</span>
                </h3>
                <p class="text-zinc-400 text-sm mt-1">إملأ الاستمارة لطلب المنتج مباشرة عبر تطبيق واتساب (الدفع عند الاستلام)</p>
            </div>

            <form id="order-wizard-form" onsubmit="handleOrderSubmission(event)" class="grid grid-cols-1 lg:grid-cols-12 gap-8">
                
                <!-- Partie Gauche de configuration -->
                <div class="lg:col-span-7 space-y-6">
                    
                    <!-- Choix du produit -->
                    <div>
                        <label class="block text-xs font-bold text-zinc-300 uppercase tracking-widest mb-3 flex justify-between">
                            <span>1. Choisir le Produit / اختر المنتج</span>
                            <span class="text-brand-cyan font-semibold">Garantie 1 An</span>
                        </label>
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                            
                            <button type="button" id="chk-prod-tagore" onclick="selectWizardProduct('tagore')" class="p-4 rounded-2xl text-left border-2 transition-all relative overflow-hidden flex flex-col justify-between h-34 border-brand-cyan bg-brand-cyan/10 font-bold scale-[1.02] cursor-pointer">
                                <span class="absolute top-2 right-2 bg-brand-cyan text-black rounded-full p-0.5" id="chk-prod-tagore-check">
                                    <i data-lucide="check" class="w-3.5 h-3.5 stroke-[3]"></i>
                                </span>
                                <div>
                                    <span class="text-[10px] text-zinc-500 font-mono tracking-widest uppercase block mb-1">TAGORA NFC</span>
                                    <h4 class="text-white text-lg font-bold font-orbitron text-left">Tagore Sticker</h4>
                                    <p class="text-xs text-zinc-400 font-sans mt-1 text-left">ستيكر طاجور الذكي NFC الممتاز للسيارات والطاولات</p>
                                </div>
                                <div class="flex items-baseline gap-2 mt-2">
                                    <span class="text-brand-cyan text-lg font-black font-orbitron">149 DH</span>
                                    <span class="text-zinc-600 text-xs line-through">199 DH</span>
                                </div>
                            </button>

                            <button type="button" id="chk-prod-infinities" onclick="selectWizardProduct('infinities')" class="p-4 rounded-2xl text-left border-2 transition-all relative overflow-hidden flex flex-col justify-between h-34 border-zinc-800 bg-zinc-900/60 hover:border-zinc-700 cursor-pointer">
                                <span class="absolute top-2 right-2 bg-brand-cyan text-black rounded-full p-0.5 hidden" id="chk-prod-infinities-check">
                                    <i data-lucide="check" class="w-3.5 h-3.5 stroke-[3]"></i>
                                </span>
                                <div>
                                    <span class="text-[10px] text-zinc-500 font-mono tracking-widest uppercase block mb-1">TAGORA NFC</span>
                                    <h4 class="text-white text-lg font-bold font-orbitron text-left">Infinities Card</h4>
                                    <p class="text-xs text-zinc-400 font-sans mt-1 text-left">البطاقة الفاخرة لزيادة تقييمات قوقل ومضاعفة زملائك</p>
                                </div>
                                <div class="flex items-baseline gap-2 mt-2">
                                    <span class="text-brand-cyan text-lg font-black font-orbitron">249 DH</span>
                                    <span class="text-zinc-600 text-xs line-through">349 DH</span>
                                </div>
                            </button>

                        </div>
                    </div>
                    <!-- Saisie de l'identifiant pour la programmation -->
                    <div>                               
                    
                    </span>

                    <!-- Quantité -->
                    <div>
                        <label class="block text-xs font-bold text-zinc-300 uppercase tracking-widest mb-3">
                            3. Quantité / الكمية
                        </label>
                        <div class="flex items-center gap-4 bg-zinc-900/70 py-2.5 px-4 rounded-xl border border-zinc-800 w-fit">
                            <button type="button" onclick="adjustCheckoutQuantity(-1)" class="w-10 h-10 rounded-lg bg-zinc-800 text-white font-bold text-lg hover:bg-zinc-700 transition flex items-center justify-center border border-zinc-700 cursor-pointer">-</button>
                            <span id="checkout-quantity-label" class="text-white text-xl font-black font-orbitron w-12 text-center font-mono">1</span>
                            <button type="button" onclick="adjustCheckoutQuantity(1)" class="w-10 h-10 rounded-lg bg-zinc-800 text-white font-bold text-lg hover:bg-zinc-700 transition flex items-center justify-center border border-zinc-700 cursor-pointer">+</button>
                            
                            <div id="checkout-promo-badge" class="hidden flex items-center gap-1.5 px-3 py-1 bg-emerald-500/10 border border-emerald-500/20 text-emerald-400 text-xs font-bold rounded-lg uppercase tracking-wider animate-pulse ml-2 font-sans">
                                <i data-lucide="percent" class="w-3.5 h-3.5"></i>
                                <span>Remise activée ! / تم الخصم</span>
                            </div>
                        </div>
                    </div>

                </div>

                <!-- Partie Droite - Remplissage des coordonnées de livraison -->
                <div class="lg:col-span-5 space-y-6">
                    
                    <div class="space-y-4">
                        <h4 class="text-zinc-200 text-sm font-semibold tracking-wide uppercase border-b border-zinc-800 pb-2">
                            Coordonnées de Livraison / معلومات التوصيل
                        </h4>
                        
                        <!-- Nom Complet -->
                        <div class="space-y-1.5">
                            <label class="text-[11px] font-bold text-zinc-400 uppercase tracking-wider flex items-center gap-1.5">
                                <i data-lucide="user" class="w-3.5 h-3.5 text-brand-cyan"></i>
                                <span>Nom complet / الإسم الكامل *</span>
                            </label>
                            <input type="text" id="billing-name" required placeholder="Ex: Ahmed Benjelloun" class="w-full bg-zinc-900 border border-zinc-800 text-white text-sm rounded-xl p-3 focus:border-brand-cyan focus:outline-none transition shadow-inner font-sans">
                        </div>

                        <!-- Téléphone / WhatsApp -->
                        <div class="space-y-1.5">
                            <label class="text-[11px] font-bold text-zinc-400 uppercase tracking-wider flex items-center gap-1.5">
                                <i data-lucide="phone" class="w-3.5 h-3.5 text-brand-cyan"></i>
                                <span>Numéro WhatsApp / رقم الهاتف *</span>
                            </label>
                            <input type="tel" id="billing-phone" required placeholder="Ex: 0612345678" class="w-full bg-zinc-900 border border-zinc-800 text-white text-sm rounded-xl p-3 focus:border-brand-cyan focus:outline-none transition shadow-inner font-mono">
                        </div>

                        <!-- Ville recherchable Maroc -->
                        <div class="space-y-1.5 relative">
                            <label class="text-[11px] font-bold text-zinc-400 uppercase tracking-wider flex items-center gap-1.5">
                                <i data-lucide="map-pin" class="w-3.5 h-3.5 text-brand-cyan"></i>
                                <span>Ville / المدينة *</span>
                            </label>
                            <div onclick="toggleCityDropdown()" id="city-selector-trigger" class="flex items-center justify-between bg-zinc-900 border border-zinc-800 rounded-xl p-3 cursor-pointer select-none shadow-inner">
                                <span class="text-zinc-500 font-sans text-sm" id="city-selector-text">Sélectionnez la ville / اختر مدينتك</span>
                                <i data-lucide="chevron-down" class="w-4 h-4 text-zinc-500 transition-transform"></i>
                            </div>

                            <!-- Menu déroulant -->
                            <div id="city-dropdown-list" class="hidden absolute top-full left-0 right-0 mt-1 bg-zinc-950 border border-zinc-800 rounded-xl shadow-2xl z-40 max-h-56 overflow-y-auto p-2 space-y-1">
                                <input type="text" id="city-search" oninput="filterCities(this.value)" placeholder="Tapez le nom de la ville... / ابحث..." class="w-full bg-zinc-900 border border-zinc-800 text-white text-xs rounded-lg p-2.5 focus:border-brand-cyan focus:outline-none font-sans">
                                
                                <div class="divide-y divide-zinc-900/40" id="cities-options-wrapper"></div>
                            </div>
                        </div>

                        <!-- Notes supplémentaires -->
                        <div class="space-y-1.5">
                            <label class="text-[11px] font-bold text-zinc-400 uppercase tracking-wider flex items-center gap-1.5">
                                <i data-lucide="message-square" class="w-3.5 h-3.5 text-brand-cyan"></i>
                                <span>Notes (Optionnel)</span>
                            </label>
                            <textarea id="billing-notes" rows="2" placeholder="Ex: Livraison l'après-midi, ou logo spécial..." class="w-full bg-zinc-900 border border-zinc-800 text-white text-sm rounded-xl p-3 focus:border-brand-cyan focus:outline-none transition shadow-inner font-sans resize-none"></textarea>
                        </div>
                    </div>

                    <!-- Détails administratifs de la facture finale -->
                    <div class="bg-zinc-900/80 rounded-2xl border border-zinc-800 p-5 space-y-4">
                        <h4 class="text-white font-orbitron font-bold text-sm uppercase tracking-wider border-b border-zinc-800 pb-2">
                            Résumé de la Facture / تفاصيل الدفع
                        </h4>
                        
                        <div class="space-y-2 text-xs md:text-sm font-sans">
                            <div class="flex justify-between text-zinc-400">
                                <span id="bill-product-name">Sticker Tagore (x1)</span>
                                <span id="bill-base-price" class="font-mono">149 DH</span>
                            </div>
                            
                            

                            <div class="flex justify-between text-zinc-400">
                                <span>Livraison Express / الشحن</span>
                                <span class="text-emerald-400 font-bold uppercase tracking-wider">Gratuit (مجاني)</span>
                            </div>
                        </div>

                        <div class="border-t border-zinc-800 pt-3 flex justify-between items-baseline">
                            <span class="text-zinc-100 font-bold text-base font-orbitron">TOTAL / المجموع :</span>
                            <div class="text-right">
                                <div id="bill-final-price" class="text-brand-cyan text-3xl font-black font-orbitron leading-none font-mono">149 DH</div>
                                <div class="text-zinc-500 text-[10px] mt-1 font-sans">Paiement Cash à la livraison seulement</div>
                            </div>
                        </div>

                        <!-- Bouton vert de commande WhatsApp -->
            <button type="button" onclick="sendWhatsApp()"
class="w-full bg-gradient-to-r from-emerald-500 to-green-500 hover:from-emerald-600 hover:to-green-600 text-white font-bold p-4 rounded-xl"><i data-lucide="shopping-cart" class="w-5 h-5 animate-pulse"></i>
    <span>COMMANDER SUR WHATSAPP</span>
    <span class="font-orbitron font-extrabold text-[11px] bg-white/20 px-2 py-0.5 rounded-full font-mono">إتمام الطلب</span>
</button>
<script>
function sendWhatsApp() {

    let message =
`السلام عليكم،

أريد طلب Tagora NFC

💰 الثمن: 149 DH`;

    window.open(
        "https://api.whatsapp.com/send/?phone=212715374284&text=Salam+TAGORA%2C+bghit+ndir+commande+stiker+NFC+%EF%BF%BD&type=phone_number&app_absent=0" +
       
        encodeURIComponent(message),
        "_blank"
    );
}
</script>
                        <p class="text-center text-zinc-500 text-[10px] leading-relaxed">
                            * بعد نقر الزر، ستفتح نافذة الدردشة واتساب لرسالة تأكيد طلبكم وعنوانكم. الشحن السريع في غضون 24-48 ساعة.
                        </p>
                    </div>

                </div>

            </form>
        </div>
    </section>

    <!-- EXPANSIONS AVIS CLIENTS -->
    <section class="py-20 bg-zinc-950/40 px-4 md:px-8 max-w-7xl mx-auto relative z-10 border-t border-zinc-900">
        
        <div class="text-center max-w-2xl mx-auto mb-16">
            <span class="text-xs text-brand-cyan md:text-sm font-black font-orbitron uppercase tracking-widest flex items-center justify-center gap-1">
                <i data-lucide="award" class="w-4 h-4"></i>
                <span>Success Stories</span>
            </span>
            <h2 class="text-3xl md:text-5xl font-black font-orbitron tracking-tight text-white uppercase mt-1">
                Avis de nos <span class="text-brand-cyan">Clients</span>
            </h2>
            <p class="text-zinc-400 text-sm mt-2">Plus de 1,200 professionnels, commerces et entreprises au Maroc font confiance à TAGORA.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-5xl mx-auto">
            
            <div class="p-6 bg-zinc-900/40 border border-zinc-800 rounded-2xl space-y-4">
                <div class="flex gap-1 text-amber-400 text-xs">★★★★★</div>
                <p class="text-xs text-zinc-300 font-sans leading-relaxed">
                    "Nous avons placé la carte Google Reviews Infinities à côté du terminal de paiement de notre restaurant. Les clients adorent le concept, nous avons obtenu plus de 120 avis positifs en un seul mois !"
                </p>
                <div class="border-t border-zinc-800/80 pt-3 flex items-center gap-3">
                    <div class="w-8 h-8 rounded-full bg-zinc-800 flex items-center justify-center text-xs font-bold text-brand-cyan">KM</div>
                    <div>
                        <span class="block text-xs font-bold text-white">Karim M.</span>
                        <span class="text-[10px] text-zinc-500 font-medium">Gérant de Restaurant, Casablanca</span>
                    </div>
                </div>
            </div>

            <div class="p-6 bg-zinc-900/40 border border-zinc-800 rounded-2xl space-y-4">
                <div class="flex gap-1 text-amber-400 text-xs">★★★★★</div>
                <p class="text-xs text-zinc-300 font-sans leading-relaxed">
                    "La qualité du sticker Tagore est exceptionnelle. Installé sur la vitre latérale de mon taxi d'hôtel, les touristes n'ont qu'à taper leur smartphone pour suivre mon compte Instagram officiel directement !"
                </p>
                <div class="border-t border-zinc-800/80 pt-3 flex items-center gap-3">
                    <div class="w-8 h-8 rounded-full bg-zinc-800 flex items-center justify-center text-xs font-bold text-brand-cyan">YE</div>
                    <div>
                        <span class="block text-xs font-bold text-white">Yassine E.</span>
                        <span class="text-[10px] text-zinc-500 font-medium">Transporteur Touristique, Marrakech</span>
                    </div>
                </div>
            </div>

            <div class="p-6 bg-zinc-900/40 border border-zinc-800 rounded-2xl space-y-4">
                <div class="flex gap-1 text-amber-400 text-xs">★★★★★</div>
                <p class="text-xs text-zinc-300 font-sans leading-relaxed">
                    "J'utilise la carte NFC Infinities dans mon cabinet dentaire. Cela rend le processus tellement ludique et discret pour demander des avis à mes patients. Une visibilité locale multipliée par cinq !"
                </p>
                <div class="border-t border-zinc-800/80 pt-3 flex items-center gap-3">
                    <div class="w-8 h-8 rounded-full bg-zinc-800 flex items-center justify-center text-xs font-bold text-brand-cyan">DL</div>
                    <div>
                        <span class="block text-xs font-bold text-white">Dr. Leila B.</span>
                        <span class="text-[10px] text-zinc-500 font-medium">Cab. Dentaire, Rabat</span>
                    </div>
                </div>
            </div>

        </div>
    </section>



    <!-- PIED DE PAGE -->
    <footer class="border-t border-zinc-900 bg-zinc-950 py-12 px-4 md:px-8 relative z-10 text-center text-zinc-500 text-xs space-y-4 font-sans">
        <div class="flex justify-center items-center gap-3">
            <div class="w-8 h-8 rounded-full border border-brand-cyan/30 bg-black flex items-center justify-center glow-cyan shadow-inner">
         <i data-lucide="zap" class="w-4 h-4 text-brand-cyan"></i>
            </div>                      
            <span class="font-orbitron font-black text-sm tracking-widest text-zinc-300">
                TAGORA<span class="text-brand-cyan">.NFC</span>
            </span>
        </div>
        <p class="max-w-md mx-auto leading-relaxed">
            Stickers & Cartes NFC intelligents de qualité supérieure au Maroc. Augmentez la visibilité de votre entreprise en toute simplicité.
        </p>
        <p class="text-[10px] text-zinc-650 font-mono">
            TAGORA NFC © <span id="current-year">2026</span> - Tous droits réservés. Service client : +212 715-374284
        </p>
    </footer>

    <!-- BALLON FLOTTANT DE SUPPORT WHATSAPP -->
    <a href="https://wa.me/212715374284?text=Salam%20TAGORA%2C%20bghit%20ndir%20commande%20stiker%20NFC%20%F0%9F%9A%80" target="_blank" rel="noopener noreferrer" class="fixed bottom-6 right-6 z-50 w-16 h-16 rounded-full bg-emerald-500 text-white flex items-center justify-center shadow-2xl hover:scale-110 active:scale-95 transition-all duration-300 glow-blue animate-bounce">
        <div class="absolute inset-0 rounded-full bg-emerald-500 animate-ping opacity-25"></div>
        <i data-lucide="message-circle" class="w-8 h-8 fill-white text-emerald-500 stroke-[2.2]"></i>
    </a>

    <!-- ENGINE JAVASCRIPT ET ALGORITHMES DE L'APPLICATION -->
    <script>
        // Année courante
        document.getElementById("current-year").innerText = new Date().getFullYear();

        // Variables d'état
        let currentLanguage = 'fr';
        let isMobileMenuOpen = false;

        // Base de Données des produits
        const PRODUCTS = {
            tagore: { id: 'tagore', name: 'Tagore Sticker', price: 149 },
            infinities: { id: 'infinities', name: 'Infinities Card', price: 249 }
        };

        // Base de Données des réseaux
        const PLATFORMS = {
            google: { id: 'google', name: 'Google Reviews', prefix: 'https://g.page/r/', placeholder: 'Ex: g.page/r/your-shop' },
            instagram: { id: 'instagram', name: 'Instagram', prefix: 'https://instagram.com/', placeholder: 'Ex: tagoranfc' },
            tiktok: { id: 'tiktok', name: 'TikTok', prefix: 'https://tiktok.com/@', placeholder: 'Ex: tagoranfc' },
            whatsapp: { id: 'whatsapp', name: 'WhatsApp', prefix: 'https://wa.me/', placeholder: 'Ex: 212715374284' },
            custom: { id: 'custom', name: 'Custom Link', prefix: 'https://', placeholder: 'Ex: www.monsite.ma' }
        };

        // Base de Données des villes Marocaines
        const CITIES = [
            { name: 'Casablanca', arabic: 'الدار البيضاء' },
            { name: 'Rabat', arabic: 'الرباط' },
            { name: 'Marrakech', arabic: 'مراكش' },
            { name: 'Tanger', arabic: 'طنجة' },
            { name: 'Agadir', arabic: 'أكادير' },
            { name: 'Fès', arabic: 'فاس' },
            { name: 'Meknès', arabic: 'مكناس' },
            { name: 'Oujda', arabic: 'وجدة' },
            { name: 'Kénitra', arabic: 'القنيطرة' },
            { name: 'Tétouan', arabic: 'تطوان' },
            { name: 'Temara', arabic: 'تمارة' },
            { name: 'Salé', arabic: 'سلا' },
            { name: 'Mohammedia', arabic: 'المحمدية' },
            { name: 'Nador', arabic: 'الناظور' },
            { name: 'El Jadida', arabic: 'الجديدة' },
            { name: 'Safi', arabic: 'آسفي' },
            { name: 'Beni Mellal', arabic: 'بني ملال' },
            { name: 'Laâyoune', arabic: 'العيون' },
            { name: 'Dakhla', arabic: 'الداخلة' }
        ];

        // État simulateur
        let simPlatform = 'google';
        let simHandleValue = 'votre_boutique';
        let simIsTapped = false;
        let simProgressTimer = null;

        // État formulaire
        let checkoutProduct = 'tagore';
        let checkoutPlatform = 'google';
        let checkoutQuantity = 1;
        let checkoutSelectedCity = '';
        let isDropdownOpen = false;

        // Changement de la langue du site
        function changeLanguage(lang) {
            currentLanguage = lang;
            const btnFr = document.getElementById('lang-btn-fr');
            const btnAr = document.getElementById('lang-btn-ar');
            
            if (lang === 'ar') {
                btnAr.className = "px-3 py-1.5 rounded-full transition bg-brand-cyan text-black font-bold";
                btnFr.className = "px-3 py-1.5 rounded-full transition text-zinc-400 hover:text-white";
                document.getElementById('intro-fr').classList.add('hidden');
                document.getElementById('intro-ar').classList.remove('hidden');
                document.getElementById('mobile-lang-label').innerText = "FR";
            } else {
                btnFr.className = "px-3 py-1.5 rounded-full transition bg-brand-cyan text-black font-bold";
                btnAr.className = "px-3 py-1.5 rounded-full transition text-zinc-400 hover:text-white";
                document.getElementById('intro-ar').classList.add('hidden');
                document.getElementById('intro-fr').classList.remove('hidden');
                document.getElementById('mobile-lang-label').innerText = "عربي";
            }
        }

        function toggleMobileLanguage() {
            changeLanguage(currentLanguage === 'fr' ? 'ar' : 'fr');
        }

        // Navigation fluide vers une section
        function scrollToSection(id) {
            const section = document.getElementById(id);
            if (section) {
                const navOffset = 80;
                const elementPosition = section.getBoundingClientRect().top + window.scrollY;
                const offsetPosition = elementPosition - navOffset;
                window.scrollTo({ top: offsetPosition, behavior: 'smooth' });
            }
        }

        function toggleMobileMenu() {
            isMobileMenuOpen = !isMobileMenuOpen;
            const mobileMenu = document.getElementById('mobile-drawer');
            const menuIcon = document.getElementById('mobile-menu-icon');
            if (isMobileMenuOpen) {
                mobileMenu.classList.remove('hidden');
                menuIcon.setAttribute('data-lucide', 'x');
            } else {
                mobileMenu.classList.add('hidden');
                menuIcon.setAttribute('data-lucide', 'menu');
            }
            lucide.createIcons();
        }

        function toggleFaqAccordion(index) {
            const itemBody = document.getElementById(`faq-body-${index}`);
            const itemIcon = document.getElementById(`faq-toggle-icon-${index}`);
            
            if (itemBody.classList.contains('hidden')) {
                itemBody.classList.remove('hidden');
                itemIcon.innerText = "×";
            } else {
                itemBody.classList.add('hidden');
                itemIcon.innerText = "+";
            }
        }

        /* SIMULATEUR NFC TAP */
        function selectSimulatorPlatform(platId) {
            simPlatform = platId;
            simIsTapped = false;
            
            const parent = document.getElementById('platform-selectors-container');
            const buttons = parent.getElementsByTagName('button');
            for (let btn of buttons) {
                btn.className = "p-2 rounded-xl flex flex-col items-center gap-1 transition text-zinc-400 border-2 border-transparent bg-zinc-950/40";
            }

            const activeBtn = document.getElementById(`sim-btn-${platId}`);
            if (activeBtn) {
                const color = platId === 'google' ? 'border-amber-500' :
                              platId === 'instagram' ? 'border-pink-500' :
                              platId === 'tiktok' ? 'border-teal-500' :
                              platId === 'whatsapp' ? 'border-green-500' : 'border-cyan-500';
                activeBtn.className = `p-2 rounded-xl flex flex-col items-center gap-1 transition text-white border-2 ${color} bg-zinc-900 scale-102 font-bold`;
            }

            const prefixLabel = document.getElementById('simulator-prefix');
            const targetPlat = PLATFORMS[platId];
            prefixLabel.innerText = targetPlat.prefix;
            
            const inputField = document.getElementById('simulator-input');
            inputField.style.paddingLeft = (targetPlat.prefix.length * 8.5 + 20) + "px";
            inputField.placeholder = targetPlat.placeholder;
            
            resetSimulatedNfcTap();
        }

        function updateSimulatorInput(val) {
            simHandleValue = val;
            resetSimulatedNfcTap();
        }

        function startSimulatedNfcTap() {
            simIsTapped = true;
            document.getElementById('trigger-simulate-btn').classList.add('hidden');
            document.getElementById('reset-simulate-btn').classList.remove('hidden');
            document.getElementById('sim-middle-signals').classList.remove('hidden');
            document.getElementById('screen-state-standby').classList.add('hidden');
            document.getElementById('screen-state-loading').classList.remove('hidden');
            
            document.getElementById('visual-tag-element').classList.add('border-brand-cyan', 'scale-[1.03]');
            document.getElementById('visual-tag-pulse-border').classList.add('border-brand-cyan');
            document.getElementById('simulator-tag-icon').classList.add('text-brand-cyan-slow', 'animate-ping');

            let progress = 0;
            const bar = document.getElementById('sim-pulse-bar');
            const counter = document.getElementById('sim-progress-counter');
            
            clearInterval(simProgressTimer);
            simProgressTimer = setInterval(() => {
                progress += 5;
                if (progress > 100) {
                    progress = 100;
                    clearInterval(simProgressTimer);
                    renderSimulatedPhoneApp();
                }
                bar.style.width = progress + "%";
                counter.innerText = progress + "%";
            }, 50);
        }

        function resetSimulatedNfcTap() {
            simIsTapped = false;
            clearInterval(simProgressTimer);
            document.getElementById('trigger-simulate-btn').classList.remove('hidden');
            document.getElementById('reset-simulate-btn').classList.add('hidden');
            document.getElementById('sim-middle-signals').classList.add('hidden');
            document.getElementById('screen-state-standby').classList.remove('hidden');
            document.getElementById('screen-state-loading').classList.add('hidden');
            document.getElementById('screen-state-app').classList.add('hidden');
            document.getElementById('visual-tag-element').classList.remove('border-brand-cyan', 'scale-[1.03]');
            document.getElementById('visual-tag-pulse-border').classList.remove('border-brand-cyan');
            document.getElementById('simulator-tag-icon').classList.remove('text-brand-cyan', 'animate-ping');
        }

        function renderSimulatedPhoneApp() {
            document.getElementById('screen-state-loading').classList.add('hidden');
            const appScreen = document.getElementById('screen-state-app');
            appScreen.classList.remove('hidden');
            appScreen.innerHTML = ''; 

            const displayName = simHandleValue || 'votre_boutique';
            let contentHTML = '';

            if (simPlatform === 'google') {
                contentHTML = `
                    <div class="flex flex-col items-center justify-center h-full p-4 text-center bg-zinc-950">
                        <p class="text-red-500 font-extrabold text-lg mb-2">Google</p>
                        <div class="bg-zinc-900 border border-zinc-800 p-4 rounded-2xl w-full">
                            <span class="block font-bold text-sm text-zinc-100">${displayName}</span>
                            <div class="flex gap-1 justify-center my-2 text-amber-400">★★★★★</div>
                            <span class="text-[10px] text-brand-cyan block">Excellent - 5/5</span>
                            <div class="w-full bg-blue-600 py-2 rounded-xl text-[10px] uppercase font-bold mt-3">Rédiger un avis</div>
                        </div>
                    </div>
                `;
            } else if (simPlatform === 'instagram') {
                contentHTML = `
                    <div class="flex flex-col items-center justify-center h-full p-4 text-center bg-zinc-950 font-sans">
                        <div class="w-16 h-16 rounded-full bg-gradient-to-tr from-yellow-500 to-purple-600 p-0.5 mb-2">
                            <div class="w-full h-full bg-black rounded-full flex items-center justify-center font-bold">@</div>
                        </div>
                        <span class="font-bold text-xs text-zinc-100">@${displayName}</span>
                        <div class="flex gap-2 text-[10px] text-zinc-400 my-2"><span><b>25K</b> abonnés</span></div>
                        <button class="bg-blue-600 text-white font-bold px-6 py-1.5 rounded-lg text-xs mt-2">S'abonner</button>
                    </div>
                `;
            } else if (simPlatform === 'tiktok') {
                contentHTML = `
                    <div class="flex flex-col items-center justify-center h-full p-4 text-center bg-black">
                        <div class="w-14 h-14 rounded-full bg-zinc-800 border-2 border-brand-cyan mb-2"></div>
                        <h4 class="font-bold text-xs text-white">@${displayName}</h4>
                        <button class="bg-[#fe2c55] text-white py-1.5 px-6 rounded-md font-bold text-[10px] mt-2">Suivre la page</button>
                    </div>
                `;
            } else if (simPlatform === 'whatsapp') {
                contentHTML = `
                    <div class="flex flex-col items-center justify-center h-full p-4 text-center bg-[#075e54]">
                        <span class="text-2xl mb-2">💬</span>
                        <h4 class="font-bold text-sm text-white">${displayName}</h4>
                        <div class="bg-[#25d366] text-white py-2 px-4 rounded-xl text-[10px] font-bold mt-4">Discuter</div>
                    </div>
                `;
            } else {
                contentHTML = `
                    <div class="flex flex-col items-center justify-center h-full p-4 text-center bg-zinc-950">
                        <span class="text-2xl mb-2">🌐</span>
                        <span class="text-[10px] text-brand-cyan truncate block max-w-[120px]">${displayName}</span>
                        <div class="bg-gradient-to-r from-cyan-500 to-blue-500 text-white py-1.5 px-4 rounded-lg text-[9px] font-bold mt-4">Visiter le site</div>
                    </div>
                `;
            }
            appScreen.innerHTML = contentHTML;
        }

        /* FORMULAIRE DE COMMANDE CALCULATOR & LOGIC */
        function selectProductForCheckout(prodId) {
            checkoutProduct = prodId;
            selectWizardProduct(prodId);
            scrollToSection('order-section');
        }

        function selectWizardProduct(prodId) {
            checkoutProduct = prodId;
            const btnTagore = document.getElementById('chk-prod-tagore');
            const checkTagore = document.getElementById('chk-prod-tagore-check');
            const btnInfinities = document.getElementById('chk-prod-infinities');
            const checkInfinities = document.getElementById('chk-prod-infinities-check');

            if (prodId === 'tagore') {
                btnTagore.className = "p-4 rounded-2xl text-left border-2 transition-all relative overflow-hidden flex flex-col justify-between h-34 border-brand-cyan bg-brand-cyan/10 font-bold scale-[1.02] cursor-pointer";
                checkTagore.classList.remove('hidden');
                btnInfinities.className = "p-4 rounded-2xl text-left border-2 transition-all relative overflow-hidden flex flex-col justify-between h-34 border-zinc-800 bg-zinc-900/60 hover:border-zinc-700 cursor-pointer";
                checkInfinities.classList.add('hidden');
            } else {
                btnInfinities.className = "p-4 rounded-2xl text-left border-2 transition-all relative overflow-hidden flex flex-col justify-between h-34 border-brand-cyan bg-brand-cyan/10 font-bold scale-[1.02] cursor-pointer";
                checkInfinities.classList.remove('hidden');
                btnTagore.className = "p-4 rounded-2xl text-left border-2 transition-all relative overflow-hidden flex flex-col justify-between h-34 border-zinc-800 bg-zinc-900/60 hover:border-zinc-700 cursor-pointer";
                checkTagore.classList.add('hidden');
            }
            recalculateCheckoutInvoice();
        }

        function selectCheckoutPlatform(platId) {
            checkoutPlatform = platId;
            const wrapper = document.getElementById('platform-checkout-selectors');
            const buttons = wrapper.getElementsByTagName('button');

            for (let btn of buttons) {
                btn.className = "py-3 px-2 rounded-xl text-center border transition-all flex flex-col items-center justify-center gap-1.5 border-zinc-800 bg-zinc-900/50 text-zinc-400 hover:border-zinc-700 cursor-pointer";
            }

            const activeBtn = document.getElementById(`chk-plat-${platId}`);
            if (activeBtn) {
                activeBtn.className = "py-3 px-2 rounded-xl text-center border transition-all flex flex-col items-center justify-center gap-1.5 border-brand-cyan bg-brand-cyan/5 text-white font-bold scale-[1.03] cursor-pointer";
            }

            const plat = PLATFORMS[platId];
            document.getElementById('chk-prefix-indicator').innerText = "Prefix: " + plat.prefix;
            document.getElementById('wizard-link-prefix').innerText = plat.prefix;
            
            const linkInput = document.getElementById('wizard-link-input');
            linkInput.placeholder = plat.placeholder;
            linkInput.style.paddingLeft = (plat.prefix.length * 7.5 + 20) + "px";
        }

        function adjustCheckoutQuantity(change) {
            checkoutQuantity = Math.max(1, checkoutQuantity + change);
            document.getElementById('checkout-quantity-label').innerText = checkoutQuantity;
            
            const promoBadge = document.getElementById('checkout-promo-badge');
            if (checkoutQuantity > 1) {
                promoBadge.classList.remove('hidden');
                promoBadge.classList.add('flex');
            } else {
                promoBadge.classList.add('hidden');
                promoBadge.classList.remove('flex');
            }
            recalculateCheckoutInvoice();
        }

        function recalculateCheckoutInvoice() {
            const prod = PRODUCTS[checkoutProduct];
            let baseTotal = prod.price * checkoutQuantity;
            let finalPaidPrice = baseTotal;
            let activePromoDiscount = 0;

            if (checkoutProduct === 'tagore') {
                if (checkoutQuantity === 2) finalPaidPrice = 249;
                else if (checkoutQuantity >= 3) finalPaidPrice = 349 + (checkoutQuantity - 3) * 110;
            } else { 
                if (checkoutQuantity === 2) finalPaidPrice = 399;
                else if (checkoutQuantity >= 3) finalPaidPrice = 549 + (checkoutQuantity - 3) * 180;
            }

            activePromoDiscount = baseTotal - finalPaidPrice;

            document.getElementById('bill-product-name').innerText = `${prod.name} (x${checkoutQuantity})`;
            document.getElementById('bill-base-price').innerText = `${baseTotal} DH`;

            const discountRow = document.getElementById('bill-promo-discount-row');
            if (activePromoDiscount > 0) {
                discountRow.classList.remove('hidden');
                document.getElementById('bill-discount-price').innerText = `-${activePromoDiscount} DH`;
            } else {
                discountRow.classList.add('hidden');
            }

            document.getElementById('bill-final-price').innerText = `${finalPaidPrice} DH`;
        }

        /* FILTRAGE DES VILLES DU MAROC */
        function toggleCityDropdown() {
            isDropdownOpen = !isDropdownOpen;
            const menu = document.getElementById('city-dropdown-list');
            if (isDropdownOpen) menu.classList.remove('hidden');
            else menu.classList.add('hidden');
        }

        function generateCitiesOptionsList(cityArray) {
            const wrapper = document.getElementById('cities-options-wrapper');
            wrapper.innerHTML = '';
            cityArray.forEach(city => {
                const opt = document.createElement('div');
                opt.className = "p-2.5 hover:bg-brand-cyan/10 hover:text-white rounded-lg text-xs font-semibold text-zinc-300 transition cursor-pointer flex justify-between items-center";
                opt.innerHTML = `<span>${city.name}</span><span class="text-zinc-500 font-mono text-[10px]">${city.arabic}</span>`;
                opt.onclick = () => selectCheckoutCity(city.name);
                wrapper.appendChild(opt);
            });
        }

        function filterCities(query) {
            const filtered = CITIES.filter(c => c.name.toLowerCase().includes(query.toLowerCase()) || c.arabic.includes(query));
            generateCitiesOptionsList(filtered);
        }

        function selectCheckoutCity(cityName) {
            checkoutSelectedCity = cityName;
            const selectedMatch = CITIES.find(c => c.name === cityName);
            document.getElementById('city-selector-text').innerText = `${selectedMatch.name} - ${selectedMatch.arabic}`;
            document.getElementById('city-selector-trigger').classList.remove('text-zinc-500');
            document.getElementById('city-selector-trigger').classList.add('text-white');
            isDropdownOpen = false;
            document.getElementById('city-dropdown-list').classList.add('hidden');
        }

        /* EXÉCUTION DE LA COMMANDE PAR WHATSAPP */
        function handleOrderSubmission(event) {
            event.preventDefault();

            const inputName = document.getElementById('billing-name').value;
            const inputPhone = document.getElementById('billing-phone').value;
            const inputNotes = document.getElementById('billing-notes').value;
            const inputLink = document.getElementById('wizard-link-input').value;

            if (!inputName || !inputPhone || !checkoutSelectedCity) {
                alert("Veuillez remplir l'id, le nom, la ville et le téléphone réglementaire.");
                return;
            }

            const activeProd = PRODUCTS[checkoutProduct];
            const activePlat = PLATFORMS[checkoutPlatform];
            const formattedLink = inputLink ? `${activePlat.prefix}${inputLink}` : 'À configurer via WhatsApp';

            let rawBasePrice = activeProd.price * checkoutQuantity;
            let finalPrice = rawBasePrice;
            if (checkoutProduct === 'tagore') {
                if (checkoutQuantity === 2) finalPrice = 249;
                else if (checkoutQuantity >= 3) finalPrice = 349 + (checkoutQuantity - 3) * 110;
            } else {
                if (checkoutQuantity === 2) finalPrice = 399;
                else if (checkoutQuantity >= 3) finalPrice = 549 + (checkoutQuantity - 3) * 180;
            }

            // Génération du modèle de texte de commande pour WhatsApp
            const messageText = `Salam TAGORA, bghit ndir commande list:\n\n` +
                `👤 *Nom / الإسم:* ${inputName}\n` +
                `📞 *Tél / الهاتف:* ${inputPhone}\n` +
                `📍 *Ville / المدينة:* ${checkoutSelectedCity}\n\n` +
                `--- *DÉTAILS COMMANDE / تفاصيل الطلب* ---\n` +
                `📦 *Produit / المنتج:* Tagora ${activeProd.name} NFC\n` +
                `🔢 *Quantité / الكمية:* ${checkoutQuantity}x\n` +
                `🔗 *Lien d'activation / الرابط:* ${activePlat.name} (${formattedLink})\n` +
                `💬 *Notes / ملاحظات:* ${inputNotes || '-'}\n\n` +
                `💰 *Total / الدفع:* *${finalPrice} DH* (شحن مجاني وسريع)\n\n` +
                `Merci d'activer ma commande dans les plus brefs délais ! ⚡🚀`;

            const encodedText = encodeURIComponent(messageText);
            const whatsappUrl = `https://wa.me/212715374284?text=${encodedText}`;
            window.open(whatsappUrl, '_blank');
        }

        // Configuration initiale du document lors du chargement
        window.addEventListener('DOMContentLoaded', () => {
            const splashScreen = document.getElementById('tagora-splash-screen');
            if (splashScreen) {
                setTimeout(() => splashScreen.classList.add('hide-splash'), 2300);
            }

            generateCitiesOptionsList(CITIES);
            selectSimulatorPlatform('google');
            recalculateCheckoutInvoice();
            lucide.createIcons();
        });
    </script>
</body>
</html>
