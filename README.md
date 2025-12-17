<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MEDIASET UNICA: Tutto il tuo mondo, in un'UNICA esperienza</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; background-color: #0f172a; color: #f1f5f9; } /* Dark Mode Base */
        .chart-container { position: relative; width: 100%; max-width: 600px; margin: 0 auto; height: 300px; max-height: 400px; }
        @media (min-width: 768px) { .chart-container { height: 350px; } }
        .card-hover:hover { transform: translateY(-5px); box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.5); border-color: #3b82f6; }
        .transition-all { transition-duration: 300ms; }
        /* Custom Scrollbar */
        .hide-scroll::-webkit-scrollbar { display: none; }
        .hide-scroll { -ms-overflow-style: none; scrollbar-width: none; }
        .hero-gradient { background: linear-gradient(to top, #0f172a 0%, transparent 100%); }
        .glass-panel { background: rgba(30, 41, 59, 0.7); backdrop-filter: blur(10px); border: 1px solid rgba(255, 255, 255, 0.1); }
        .neon-border { box-shadow: 0 0 5px #3b82f6, 0 0 10px #3b82f6; border-color: #60a5fa; }
        
        /* AI Section Specifics */
        .ai-gradient { background: linear-gradient(135deg, #1e1b4b 0%, #312e81 100%); }
        .shimmer { background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent); background-size: 200% 100%; animation: shimmer 2s infinite; }
        @keyframes shimmer { 0% { background-position: -200% 0; } 100% { background-position: 200% 0; } }
    </style>
</head>
<body class="bg-slate-900 text-slate-100 antialiased selection:bg-blue-500 selection:text-white">

    <!-- Navigation / Header -->
    <nav class="bg-slate-900/90 backdrop-blur-md border-b border-slate-800 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center gap-6">
                    <div class="flex items-center group cursor-pointer">
                        <!-- NEW SVG LOGO INTEGRATION -->
                        <svg class="h-14 w-auto rounded-lg shadow-lg hover:scale-105 transition-transform duration-200" viewBox="0 0 800 800" role="img" aria-label="Mediaset Unica">
                            <defs>
                                <radialGradient id="bg" cx="50%" cy="35%" r="80%">
                                    <stop offset="0%"  stop-color="#2a2656"/>
                                    <stop offset="55%" stop-color="#1e1a3c"/>
                                    <stop offset="100%" stop-color="#16122f"/>
                                </radialGradient>
                                <linearGradient id="gradBar" x1="0%" y1="0%" x2="100%" y2="0%">
                                    <stop offset="0%" stop-color="#4db7ff"/>
                                    <stop offset="55%" stop-color="#7b5cff"/>
                                    <stop offset="100%" stop-color="#b04bff"/>
                                </linearGradient>
                                <linearGradient id="gradUnica" x1="0%" y1="0%" x2="100%" y2="0%">
                                    <stop offset="0%" stop-color="#b04bff"/>
                                    <stop offset="55%" stop-color="#7b5cff"/>
                                    <stop offset="100%" stop-color="#4db7ff"/>
                                </linearGradient>
                                <filter id="softShadow" x="-30%" y="-30%" width="160%" height="160%">
                                    <feDropShadow dx="0" dy="6" stdDeviation="8" flood-color="#000" flood-opacity="0.35"/>
                                </filter>
                            </defs>
                            <rect x="0" y="0" width="800" height="800" fill="url(#bg)"/>
                            <text x="400" y="210" text-anchor="middle" font-family="system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif" font-size="64" letter-spacing="10" fill="#ffffff" opacity="0.95">MEDIASET</text>
                            <rect x="230" y="250" width="340" height="10" rx="5" fill="url(#gradBar)" opacity="0.95"/>
                            <g filter="url(#softShadow)" transform="translate(0, 10)">
                                <path d="M345 330 L345 470 Q345 490 363 480 L500 410 Q520 400 500 390 L363 320 Q345 310 345 330 Z" fill="#74e6cf"/>
                                <path d="M405 375 L405 445 L465 410 Z" fill="#1e1a3c" opacity="0.95"/>
                            </g>
                            <text x="400" y="640" text-anchor="middle" font-family="system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif" font-size="96" letter-spacing="14" fill="url(#gradUnica)">UNICA</text>
                        </svg>
                    </div>
                    <!-- Desktop Menu -->
                    <div class="hidden md:flex space-x-1 ml-4">
                        <a href="#hero" class="text-slate-300 hover:text-white px-3 py-2 text-sm font-medium">Home</a>
                        <a href="#ai-lab" class="text-purple-400 hover:text-purple-300 px-3 py-2 text-sm font-bold"><i class="fas fa-sparkles mr-1"></i> AI Lab</a>
                        <a href="#voting" class="text-slate-300 hover:text-blue-400 px-3 py-2 text-sm font-bold"><i class="fas fa-poll mr-1"></i> Vota i Generi</a>
                        <a href="#settimane" class="text-blue-400 hover:text-blue-300 px-3 py-2 text-sm font-bold"><i class="fas fa-calendar-week mr-1"></i> Settimane</a>
                    </div>
                </div>
                <div class="flex items-center space-x-4">
                    <button class="text-slate-400 hover:text-white"><i class="fas fa-search"></i></button>
                    <div class="w-8 h-8 rounded-full bg-gradient-to-br from-blue-500 to-indigo-600 flex items-center justify-center text-xs font-bold border border-slate-600 cursor-pointer shadow-lg shadow-blue-500/30">IO</div>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section: SETTIMANA CRIME Simulation -->
    <section id="hero" class="relative w-full h-[80vh] flex items-center justify-center overflow-hidden border-b border-slate-800">
        <!-- Background Mockup -->
        <div class="absolute inset-0 z-0">
            <div class="absolute inset-0 bg-slate-900"></div>
            <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1478720568477-152d9b164e63?ixlib=rb-1.2.1&auto=format&fit=crop&w=1920&q=80')] bg-cover bg-center opacity-40 mix-blend-overlay"></div>
            <div class="absolute inset-0 bg-gradient-to-t from-slate-900 via-slate-900/60 to-transparent"></div>
            <div class="absolute inset-0 bg-gradient-to-r from-slate-900 via-transparent to-transparent"></div>
        </div>

        <div class="relative z-10 max-w-7xl mx-auto px-4 w-full mt-10">
            <!-- Community Vote Badge -->
            <div class="inline-flex items-center px-4 py-1.5 rounded-full bg-slate-900/80 text-white text-xs font-bold tracking-wider mb-6 border border-blue-500/50 backdrop-blur-md shadow-lg shadow-blue-500/20">
                <i class="fas fa-check-circle text-blue-400 mr-2"></i> SCELTA DALLA COMMUNITY
            </div>
            
            <h1 class="text-5xl md:text-7xl font-extrabold text-white tracking-tight mb-4 max-w-4xl leading-tight drop-shadow-2xl">
                Indagini, Misteri e <br> <span class="text-transparent bg-clip-text bg-gradient-to-r from-red-500 to-blue-600">Verità Nascoste.</span>
            </h1>
            <p class="text-lg md:text-xl text-slate-300 max-w-2xl mb-8 font-light leading-relaxed drop-shadow-md border-l-4 border-red-600 pl-4">
                La <strong>Settimana Crime</strong> domina la classifica di questo mese. 7 giorni di contenuti curati, podcast e dossier esclusivi.
            </p>
            
            <div class="flex flex-wrap gap-4 mb-12">
                <button class="px-8 py-4 bg-white text-slate-900 font-bold rounded-lg hover:bg-slate-200 transition-colors flex items-center shadow-xl shadow-white/5 transform hover:scale-105 duration-200">
                    <i class="fas fa-play mr-2"></i> Guarda Trailer
                </button>
                <button class="px-8 py-4 bg-slate-800/60 hover:bg-slate-700/60 text-white font-medium rounded-lg backdrop-blur-sm border border-slate-600 transition-colors flex items-center">
                    <i class="fas fa-book-open mr-2"></i> Extra & Dossier
                </button>
            </div>
        </div>
    </section>

    <!-- NEW SECTION: GEMINI AI INTEGRATION -->
    <section id="ai-lab" class="py-16 ai-gradient border-b border-slate-700 relative overflow-hidden">
        <div class="absolute top-0 right-0 w-64 h-64 bg-purple-500/10 rounded-full blur-3xl"></div>
        <div class="absolute bottom-0 left-0 w-96 h-96 bg-blue-500/10 rounded-full blur-3xl"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="flex items-center justify-center mb-10">
                <span class="px-3 py-1 rounded-full bg-purple-500/20 text-purple-300 text-xs font-bold border border-purple-500/30 uppercase tracking-widest mr-3">
                    <i class="fas fa-sparkles mr-1"></i> Powered by Gemini
                </span>
                <h2 class="text-3xl font-bold text-white text-center">UNICA Lab AI</h2>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                
                <!-- FEATURE 1: MOOD MATCHER -->
                <div class="glass-panel p-8 rounded-2xl border-t border-purple-500/50 relative group">
                    <div class="absolute -top-6 left-6 w-12 h-12 bg-purple-600 rounded-lg flex items-center justify-center shadow-lg shadow-purple-600/40">
                        <i class="fas fa-brain text-white text-xl"></i>
                    </div>
                    <h3 class="mt-4 text-xl font-bold text-white mb-2">Mood Matcher</h3>
                    <p class="text-slate-300 text-sm mb-6">Non sai cosa guardare? Descrivi come ti senti o cosa desideri, e la nostra AI cercherà nel catalogo per te.</p>
                    
                    <div class="space-y-4">
                        <textarea id="moodInput" rows="2" class="w-full bg-slate-800/50 border border-slate-600 rounded-lg p-3 text-white placeholder-slate-400 focus:outline-none focus:border-purple-500 transition-colors" placeholder="Es: Voglio un film crime ma che faccia anche ridere, ambientato in Italia..."></textarea>
                        <button onclick="generateMoodRecommendation()" id="btnMood" class="w-full py-3 bg-gradient-to-r from-purple-600 to-indigo-600 hover:from-purple-500 hover:to-indigo-500 text-white font-bold rounded-lg transition-all shadow-lg flex justify-center items-center">
                            <span id="btnMoodText">Trova con AI</span>
                            <i id="btnMoodIcon" class="fas fa-magic ml-2"></i>
                        </button>
                    </div>

                    <!-- Result Area -->
                    <div id="moodResult" class="mt-6 hidden space-y-3">
                        <!-- Dynamic Content -->
                    </div>
                </div>

                <!-- FEATURE 2: TRIVIA GENERATOR -->
                <div class="glass-panel p-8 rounded-2xl border-t border-blue-500/50 relative group">
                    <div class="absolute -top-6 left-6 w-12 h-12 bg-blue-600 rounded-lg flex items-center justify-center shadow-lg shadow-blue-600/40">
                        <i class="fas fa-gamepad text-white text-xl"></i>
                    </div>
                    <div class="absolute top-4 right-4 text-xs font-mono text-blue-300">Tema: CRIME</div>
                    
                    <h3 class="mt-4 text-xl font-bold text-white mb-2">Trivia Generator</h3>
                    <p class="text-slate-300 text-sm mb-6">Mettiti alla prova con quiz generati infiniti sul tema della settimana. Sfida l'AI.</p>

                    <div id="triviaContainer" class="bg-slate-800/50 rounded-lg p-6 border border-slate-700 min-h-[200px] flex flex-col justify-center items-center text-center">
                        <div class="text-slate-400 mb-4 text-sm">Pronto per la sfida?</div>
                        <button onclick="generateTrivia()" id="btnTrivia" class="px-6 py-2 bg-slate-700 hover:bg-slate-600 text-white font-bold rounded-full transition-colors border border-slate-500">
                            <i class="fas fa-play mr-2"></i> Inizia Quiz
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Vision & Target Section -->
    <section id="vision" class="py-20 bg-slate-900 border-b border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <h2 class="text-3xl md:text-5xl font-extrabold text-white mb-6">
                    "Tutto il tuo mondo,<br>in un'<span class="text-blue-500 italic">UNICA</span> esperienza."
                </h2>
                <p class="text-slate-400 text-lg leading-relaxed">
                    Non un semplice archivio, ma una <strong>piattaforma viva</strong>. Un ecosistema dinamico che genera <strong>hype costante</strong> e unisce video, musica, letture e socialità.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="glass-panel p-8 rounded-2xl border-t-4 border-t-blue-500 relative overflow-hidden group">
                    <div class="absolute top-0 right-0 p-4 opacity-10 group-hover:opacity-20 transition-opacity"><i class="fas fa-sync-alt text-6xl text-white"></i></div>
                    <h3 class="text-xl font-bold text-white mb-3">Piattaforma in Movimento</h3>
                    <p class="text-slate-400 text-sm">Home dinamica che cambia pelle ogni settimana. Colori, layout e contenuti si adattano al genere votato. Niente staticità.</p>
                </div>
                <div class="glass-panel p-8 rounded-2xl border-t-4 border-t-purple-500 relative overflow-hidden group">
                     <div class="absolute top-0 right-0 p-4 opacity-10 group-hover:opacity-20 transition-opacity"><i class="fas fa-users text-6xl text-white"></i></div>
                    <h3 class="text-xl font-bold text-white mb-3">Social-Driven</h3>
                    <p class="text-slate-400 text-sm"> chat tematiche, reaction e meme. La community modella il palinsesto e decide cosa guardare.</p>
                </div>
                <div class="glass-panel p-8 rounded-2xl border-t-4 border-t-green-500 relative overflow-hidden group">
                     <div class="absolute top-0 right-0 p-4 opacity-10 group-hover:opacity-20 transition-opacity"><i class="fas fa-book text-6xl text-white"></i></div>
                    <h3 class="text-xl font-bold text-white mb-3">Esperienza Totale</h3>
                    <p class="text-slate-400 text-sm">Non solo video. Proposte di <strong>Libri</strong> e <strong>Musica</strong> collegate al tema della settimana per un'immersione completa.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- VOTING MECHANISM ENGINE -->
    <section id="voting" class="py-20 bg-slate-950 relative overflow-hidden">
        <div class="absolute top-0 left-0 w-full h-full bg-[url('https://www.transparenttextures.com/patterns/cubes.png')] opacity-5"></div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="flex flex-col md:flex-row gap-12 items-center">
                <!-- Text Description -->
                <div class="md:w-1/3">
                    <span class="text-blue-500 font-bold tracking-widest text-xs uppercase mb-2 block">Il Motore della Piattaforma</span>
                    <h2 class="text-3xl font-bold text-white mb-6">Tu decidi il Palinsesto.</h2>
                    <p class="text-slate-400 mb-6">
                        Ogni mese la community vota i generi preferiti. I vincitori occupano le settimane del mese successivo.
                    </p>
                    <ul class="space-y-4 text-sm text-slate-300">
                        <li class="flex items-center"><span class="w-6 h-6 rounded bg-yellow-500 text-slate-900 font-bold flex items-center justify-center text-xs mr-3">1</span> 1ª Posizione &rarr; 1ª Settimana</li>
                        <li class="flex items-center"><span class="w-6 h-6 rounded bg-slate-700 text-white font-bold flex items-center justify-center text-xs mr-3">2</span> 2ª Posizione &rarr; 2ª Settimana</li>
                    </ul>
                    <button class="mt-8 px-6 py-3 bg-blue-600 hover:bg-blue-500 text-white rounded-lg font-bold w-full transition-colors shadow-lg shadow-blue-600/20">
                        Vota per il Prossimo Mese <i class="fas fa-arrow-right ml-2"></i>
                    </button>
                </div>

                <!-- Visual Engine Representation -->
                <div class="md:w-2/3 w-full bg-slate-900 border border-slate-800 rounded-2xl p-6 shadow-2xl relative">
                    <h3 class="text-center text-white font-bold mb-6">Classifica Live: Generi Mese Prossimo</h3>
                    <div class="space-y-4">
                        <div class="relative">
                            <div class="flex justify-between text-xs text-white mb-1 font-bold">
                                <span>1. Anime & Manga</span>
                                <span>34% Voti</span>
                            </div>
                            <div class="w-full h-10 bg-slate-800 rounded-lg overflow-hidden relative border border-purple-500/50">
                                <div class="absolute top-0 left-0 h-full bg-gradient-to-r from-purple-600 to-indigo-600 w-[34%] animate-pulse"></div>
                                <div class="absolute inset-0 flex items-center px-4">
                                    <span class="text-xs font-bold text-white drop-shadow-md z-10 uppercase tracking-wider">Settimana 1: Anime</span>
                                </div>
                            </div>
                        </div>
                         <div class="relative">
                            <div class="flex justify-between text-xs text-slate-300 mb-1">
                                <span>2. K-Drama / Asia</span>
                                <span>28% Voti</span>
                            </div>
                            <div class="w-full h-8 bg-slate-800 rounded-lg overflow-hidden relative">
                                <div class="absolute top-0 left-0 h-full bg-slate-600 w-[28%]"></div>
                                 <div class="absolute inset-0 flex items-center px-4">
                                    <span class="text-[10px] font-bold text-slate-200 z-10 uppercase">Settimana 2</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Interactive "Settimane" Demo -->
    <section id="settimane" class="py-16 bg-slate-900 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-white">Live Demo: L'Esperienza Settimanale</h2>
                <p class="mt-4 text-slate-400 max-w-2xl mx-auto">
                    Ecco come appare la piattaforma durante la "Settimana Crime". Nota l'integrazione di Libri e Musica.
                </p>
            </div>

            <!-- Interface Simulator -->
            <div class="bg-slate-950 border border-slate-800 rounded-2xl overflow-hidden shadow-2xl">
                <!-- Simulator Header -->
                <div class="bg-slate-900 px-4 py-3 flex items-center justify-between border-b border-slate-800">
                    <div class="flex space-x-2">
                        <div class="w-3 h-3 rounded-full bg-red-500"></div>
                        <div class="w-3 h-3 rounded-full bg-yellow-500"></div>
                        <div class="w-3 h-3 rounded-full bg-green-500"></div>
                    </div>
                    <div class="text-xs text-slate-500 font-mono uppercase">Simulazione Interfaccia Desktop</div>
                </div>

                <div class="flex flex-col md:flex-row h-[700px]">
                    <!-- Sidebar Selector -->
                    <div class="w-full md:w-64 bg-slate-900/50 border-r border-slate-800 p-4 flex flex-col gap-2">
                         <div class="mb-4 text-xs font-bold text-slate-500 uppercase tracking-widest">Navigazione</div>
                        <button onclick="loadWeek('crime')" id="btn-crime" class="w-full text-left px-4 py-3 rounded-lg bg-red-900/20 text-red-400 border border-red-900/50 font-bold transition-all hover:bg-red-900/30">
                            <i class="fas fa-search mr-2"></i> Settimana Crime
                        </button>
                        <button onclick="loadWeek('anime')" id="btn-anime" class="w-full text-left px-4 py-3 rounded-lg text-slate-400 hover:bg-slate-800 transition-all">
                            <i class="fas fa-dragon mr-2"></i> Settimana Anime
                        </button>
                    </div>

                    <!-- Main Content Area -->
                    <div class="flex-1 overflow-y-auto bg-slate-950 relative custom-scrollbar" id="week-display">
                        <!-- Dynamic Content Injected Here -->
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Community & Quiz Section -->
    <section id="community" class="py-20 bg-gradient-to-b from-slate-900 to-slate-950 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                
                <!-- Quiz QR Code Card -->
                <div class="bg-white text-slate-900 rounded-3xl p-8 shadow-2xl flex flex-col items-center text-center relative overflow-hidden">
                    <div class="absolute top-0 left-0 w-full h-4 bg-gradient-to-r from-blue-500 to-purple-600"></div>
                    <h3 class="text-3xl font-extrabold mb-2">Che spettatore sei?</h3>
                    <p class="text-slate-600 mb-8 max-w-sm">Fai il test ufficiale, scopri il tuo profilo e personalizza il tuo feed UNICA.</p>
                    
                    <!-- REAL GENERATED QR CODE (Simulated via API for provided URL) -->
                    <div class="w-48 h-48 bg-white rounded-xl flex items-center justify-center mb-6 border-4 border-slate-900 p-1 relative group cursor-pointer shadow-lg">
                        <!-- QR Code image generated from API pointing to https://scanned.page/vlfnO8 -->
                        <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://scanned.page/vlfnO8&color=0f172a&bgcolor=ffffff" 
                             alt="QR Code Test Spettatore" 
                             class="w-full h-full object-contain">
                        
                        <!-- Logo Overlay (Mimics the Python script logic) -->
                        <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-10 h-10 bg-white rounded-md flex items-center justify-center shadow-sm border border-slate-100 p-1">
                             <div class="w-full h-full bg-gradient-to-br from-blue-600 to-indigo-800 rounded flex items-center justify-center">
                                 <i class="fas fa-play text-[8px] text-white"></i>
                             </div>
                        </div>

                        <div class="absolute inset-0 bg-white/90 z-20 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity rounded-lg">
                            <span class="font-bold text-slate-900 text-sm"><i class="fas fa-camera mr-2"></i>Scannerizza</span>
                        </div>
                    </div>
                    
                    <button class="px-6 py-2 bg-slate-900 text-white rounded-full font-bold hover:bg-slate-700 transition-colors">
                        Fai il Test Online
                    </button>
                </div>

                <!-- Telegram & Community Hub -->
                <div class="flex flex-col justify-center">
                    <span class="text-blue-500 font-bold tracking-widest text-xs uppercase mb-2">Social Hub</span>
                    <h2 class="text-3xl font-bold text-white mb-6">Entra nella Chat.</h2>
                    <p class="text-slate-400 mb-8">
                        Unisciti alle chat divise per genere. Commenta in diretta, partecipa ai sondaggi e invia i tuoi meme.
                    </p>
                    <div class="space-y-4">
                        <a href="#" class="block p-4 bg-slate-800 rounded-xl border border-slate-700 hover:border-blue-500 hover:bg-slate-750 transition-all group">
                            <div class="flex items-center justify-between">
                                <div class="flex items-center">
                                    <div class="w-10 h-10 rounded-full bg-blue-500/20 flex items-center justify-center text-blue-400 mr-4">
                                        <i class="fab fa-telegram-plane"></i>
                                    </div>
                                    <div>
                                        <h4 class="text-white font-bold group-hover:text-blue-400 transition-colors">UNICA Crime Files</h4>
                                        <p class="text-xs text-slate-500">Moderatori Ufficiali • 12k Membri</p>
                                    </div>
                                </div>
                                <i class="fas fa-chevron-right text-slate-600"></i>
                            </div>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="py-16 bg-slate-950 border-t border-slate-900">
        <div class="max-w-7xl mx-auto px-4 text-center mb-8">
            <h2 class="text-2xl font-bold text-white">Scegli il tuo Piano</h2>
        </div>
        <div class="max-w-5xl mx-auto px-4 grid grid-cols-1 md:grid-cols-3 gap-6">
            <div class="bg-slate-900 p-6 rounded-2xl border border-slate-800 text-center opacity-75 hover:opacity-100 transition-opacity">
                <h3 class="text-slate-300 font-bold">Free</h3>
                <p class="text-2xl text-white font-bold my-2">€0</p>
                <p class="text-xs text-slate-500">Con Pubblicità</p>
                <p class="text-xs text-slate-500">Catalogo limitato</p>
            </div>
            <div class="bg-slate-900 p-6 rounded-2xl border-2 border-blue-600 text-center transform scale-105 shadow-xl shadow-blue-900/20 relative">
                <div class="absolute top-0 left-1/2 transform -translate-x-1/2 -translate-y-1/2 bg-blue-600 text-[10px] px-3 py-1 rounded-full text-white font-bold uppercase">Consigliato</div>
                <h3 class="text-white font-bold">Cinema & Serie</h3>
                <p class="text-3xl text-blue-400 font-bold my-2">€7,99</p>
                <p class="text-xs text-slate-400">Tutto il catalogo</p>
                <p class="text-xs text-slate-500">per i clienti di Infinity + gratis per 3 mesi</p>
            </div>
            <div class="bg-slate-900 p-6 rounded-2xl border border-slate-800 text-center opacity-75 hover:opacity-100 transition-opacity">
                <h3 class="text-amber-400 font-bold">Premium</h3>
                <p class="text-2xl text-white font-bold my-2">€14,99</p>
                <p class="text-xs text-slate-500">4K + Eventi Esclusivi + AI Gemini</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-slate-950 border-t border-slate-900 py-12">
        <div class="max-w-7xl mx-auto px-4 text-center">
            <p class="text-slate-600 text-sm">© 2025 Mediaset S.p.A. - Documento Strategico</p>
        </div>
    </footer>

    <!-- JavaScript Logic -->
    <script>
        // --- API CONFIGURATION ---
        const apiKey = ""; // Runtime provided key
        const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;

        // --- GEMINI: MOOD MATCHER ---
        async function generateMoodRecommendation() {
            const input = document.getElementById('moodInput').value;
            const btnText = document.getElementById('btnMoodText');
            const btnIcon = document.getElementById('btnMoodIcon');
            const resultDiv = document.getElementById('moodResult');

            if (!input) return alert("Scrivi un mood per ricevere consigli!");

            // UI Loading State
            btnText.innerText = "Analisi in corso...";
            btnIcon.className = "fas fa-spinner fa-spin ml-2";
            resultDiv.classList.add('hidden');

            const prompt = `Sei l'AI di Mediaset Unica. L'utente dice: "${input}". 
            Consiglia 2 titoli (Serie TV o Film, esistenti o verosimili nel catalogo Mediaset/Crime) perfetti per questo mood. 
            Rispondi SOLO con un array JSON valido: [{"title": "Nome Titolo", "desc": "Motivo breve in una frase", "type": "Film" o "Serie"}]. 
            Non usare markdown.`;

            try {
                const response = await fetch(apiUrl, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ contents: [{ parts: [{ text: prompt }] }] })
                });
                const data = await response.json();
                const rawText = data.candidates[0].content.parts[0].text;
                const cleanJson = rawText.replace(/```json|```/g, '').trim();
                const recommendations = JSON.parse(cleanJson);

                // Render Results
                resultDiv.innerHTML = recommendations.map(rec => `
                    <div class="bg-slate-800 p-4 rounded-lg border border-slate-600 animate-fade-in flex items-start">
                        <div class="mr-4 mt-1 text-purple-400"><i class="fas ${rec.type === 'Serie' ? 'fa-tv' : 'fa-film'}"></i></div>
                        <div>
                            <h4 class="font-bold text-white">${rec.title}</h4>
                            <p class="text-xs text-slate-400 mt-1">${rec.desc}</p>
                        </div>
                    </div>
                `).join('');
                resultDiv.classList.remove('hidden');

            } catch (error) {
                console.error(error);
                resultDiv.innerHTML = `<div class="text-red-400 text-xs">Errore nell'analisi del mood. Riprova.</div>`;
                resultDiv.classList.remove('hidden');
            } finally {
                btnText.innerText = "Trova con AI";
                btnIcon.className = "fas fa-magic ml-2";
            }
        }

        // --- GEMINI: TRIVIA GENERATOR ---
        async function generateTrivia() {
            const container = document.getElementById('triviaContainer');
            
            // UI Loading
            container.innerHTML = `<div class="text-blue-300 text-sm"><i class="fas fa-circle-notch fa-spin mr-2"></i> Generazione nuova domanda...</div>`;

            const prompt = `Genera una domanda trivia difficile sul genere "Crime" o "Serie TV Poliziesche". 
            Fornisci 3 opzioni e l'indice della risposta corretta.
            Rispondi SOLO in JSON: {"q": "Testo domanda", "options": ["A", "B", "C"], "correct": 0}. Non usare markdown.`;

            try {
                const response = await fetch(apiUrl, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ contents: [{ parts: [{ text: prompt }] }] })
                });
                const data = await response.json();
                const rawText = data.candidates[0].content.parts[0].text;
                const cleanJson = rawText.replace(/```json|```/g, '').trim();
                const quiz = JSON.parse(cleanJson);

                // Render Question
                container.innerHTML = `
                    <div class="w-full animate-fade-in">
                        <h4 class="font-bold text-white mb-4 text-center text-lg">${quiz.q}</h4>
                        <div class="grid grid-cols-1 gap-2">
                            ${quiz.options.map((opt, idx) => `
                                <button onclick="checkAnswer(this, ${idx}, ${quiz.correct})" class="bg-slate-700 hover:bg-slate-600 text-slate-200 py-3 rounded-lg border border-slate-600 transition-all text-sm font-medium">
                                    ${opt}
                                </button>
                            `).join('')}
                        </div>
                        <button onclick="generateTrivia()" class="mt-4 text-xs text-slate-500 hover:text-white underline w-full text-center">Salta domanda</button>
                    </div>
                `;

            } catch (error) {
                container.innerHTML = `<div class="text-red-400 text-xs">Errore generazione quiz. <button onclick="generateTrivia()" class="underline">Riprova</button></div>`;
            }
        }

        function checkAnswer(btn, selected, correct) {
            const buttons = btn.parentElement.children;
            if (selected === correct) {
                btn.classList.remove('bg-slate-700', 'border-slate-600');
                btn.classList.add('bg-green-600', 'border-green-500', 'text-white');
                // Auto load next after 1.5s
                setTimeout(generateTrivia, 1500);
            } else {
                btn.classList.remove('bg-slate-700', 'border-slate-600');
                btn.classList.add('bg-red-600', 'border-red-500', 'text-white');
                // Show correct one
                buttons[correct].classList.add('bg-green-600/50', 'border-green-500/50');
            }
        }

        // --- EXISTING WEEK DATA & LOGIC ---
        const weeksData = {
            crime: {
                content: `
                    <div class="p-8 h-full flex flex-col animate-fade-in">
                        <div class="flex justify-between items-end mb-6">
                            <div>
                                <h3 class="text-3xl font-bold text-white">Speciale Crime</h3>
                                <p class="text-red-400 text-sm font-medium uppercase tracking-widest mt-1">Settimana 1 - Genere Votato</p>
                            </div>
                        </div>
                        <div class="w-full h-64 rounded-xl bg-gradient-to-r from-red-950 to-slate-900 border border-red-900/30 relative overflow-hidden group mb-8">
                             <div class="absolute right-0 top-0 h-full w-2/3 bg-[url('https://images.unsplash.com/photo-1555099962-4199c345e5dd?auto=format&fit=crop&q=80')] bg-cover bg-center opacity-30 mix-blend-overlay"></div>
                             <div class="relative z-10 p-8 h-full flex flex-col justify-center">
                                <span class="bg-red-600 text-white text-[10px] font-bold px-2 py-0.5 rounded w-max uppercase mb-2">Main Highlight</span>
                                <h4 class="text-4xl font-extrabold text-white mb-2">Caccia al Killer</h4>
                                <p class="text-sm text-slate-300 mb-6 max-w-sm">Il documentario true crime che ha diviso l'America arriva in esclusiva.</p>
                                <div class="flex gap-3">
                                    <button class="px-5 py-2 bg-white text-red-900 font-bold text-sm rounded hover:bg-slate-200"><i class="fas fa-play mr-1"></i> Guarda Ora</button>
                                </div>
                             </div>
                        </div>
                        <div class="mb-8">
                            <h5 class="text-xs font-bold text-slate-400 uppercase mb-4 tracking-widest border-b border-slate-800 pb-2">Esperienza Totale</h5>
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                                <div class="bg-slate-900 p-4 rounded-xl border border-slate-800 flex items-center hover:border-red-500/50 transition-colors cursor-pointer group">
                                    <div class="w-12 h-16 bg-slate-700 rounded shadow-lg mr-4 bg-[url('https://images.unsplash.com/photo-1544947950-fa07a98d237f?auto=format&fit=crop&q=60')] bg-cover"></div>
                                    <div>
                                        <span class="text-[10px] text-red-400 font-bold uppercase">Libro</span>
                                        <h6 class="text-white font-bold text-sm">A Sangue Freddo</h6>
                                    </div>
                                </div>
                                <div class="bg-slate-900 p-4 rounded-xl border border-slate-800 flex items-center hover:border-red-500/50 transition-colors cursor-pointer group">
                                    <div class="w-12 h-12 bg-green-500 rounded-lg shadow-lg mr-4 flex items-center justify-center text-black">
                                        <i class="fab fa-spotify text-2xl"></i>
                                    </div>
                                    <div>
                                        <span class="text-[10px] text-green-400 font-bold uppercase">Musica</span>
                                        <h6 class="text-white font-bold text-sm">Crime Vibes</h6>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                `
            },
            anime: {
                content: `
                    <div class="p-8 h-full flex flex-col animate-fade-in bg-slate-900/50">
                        <div class="flex flex-col items-center justify-center h-full text-center">
                             <div class="w-20 h-20 bg-purple-600/20 rounded-full flex items-center justify-center mb-4 animate-bounce">
                                <i class="fas fa-dragon text-4xl text-purple-500"></i>
                             </div>
                             <h3 class="text-2xl font-bold text-white mb-2">Prossimamente: Settimana Anime</h3>
                             <p class="text-slate-400 text-sm max-w-md">Votata dalla community per la prossima settimana.</p>
                        </div>
                    </div>
                `
            }
        };

        function loadWeek(key) {
            ['crime', 'anime'].forEach(k => {
                const btn = document.getElementById(`btn-${k}`);
                if (!btn) return;
                const color = k === 'crime' ? 'red' : 'purple';
                if (k === key) {
                    btn.className = `w-full text-left px-4 py-3 rounded-lg bg-${color}-900/20 text-${color}-400 border border-${color}-900/50 font-bold transition-all shadow-lg`;
                } else {
                    btn.className = "w-full text-left px-4 py-3 rounded-lg text-slate-400 hover:bg-slate-800 transition-all opacity-70 hover:opacity-100";
                }
            });
            document.getElementById('week-display').innerHTML = weeksData[key].content;
        }

        document.addEventListener('DOMContentLoaded', () => {
            loadWeek('crime'); 
        });
    </script>
    <style>
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        .animate-fade-in { animation: fadeIn 0.4s ease-out forwards; }
    </style>
</body>
</html>
