
<html lang="pt-BR" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MHD Industrial | Fundição por Levitação Magnética & Manufatura Avançada</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        sci: {
                            950: '#020617',
                            900: '#090d16',
                            800: '#111827',
                            700: '#1f2937',
                            cyan: '#06b6d4',
                            emerald: '#10b981',
                            amber: '#f59e0b',
                            rose: '#f43f5e',
                            purple: '#8b5cf6'
                        }
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; }
        .font-mono { font-family: 'JetBrains Mono', monospace; }
        .glass-panel {
            background: rgba(15, 23, 42, 0.75);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(6, 182, 212, 0.2);
        }
        .glow-cyan {
            box-shadow: 0 0 25px rgba(6, 182, 212, 0.25);
        }
        .glow-amber {
            box-shadow: 0 0 25px rgba(245, 158, 11, 0.3);
        }
        ::-webkit-scrollbar {
            width: 6px;
            height: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #020617;
        }
        ::-webkit-scrollbar-thumb {
            background: #1e293b;
            border-radius: 3px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #06b6d4;
        }
    </style>
</head>
<body class="bg-sci-950 text-slate-100 min-h-screen flex flex-col overflow-x-hidden">

    <!-- Header / Navbar -->
    <header class="glass-panel border-b border-cyan-500/20 px-6 py-4 flex flex-wrap items-center justify-between gap-4 sticky top-0 z-50">
        <div class="flex items-center space-x-3">
            <div class="relative flex items-center justify-center w-10 h-10 rounded-xl bg-cyan-950 border border-cyan-500/50 glow-cyan">
                <svg class="w-6 h-6 text-cyan-400 animate-pulse" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z"/>
                </svg>
            </div>
            <div>
                <h1 class="text-lg font-bold tracking-wider text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-amber-400">MHD HEAVY INDUSTRY FOUNDRY</h1>
                <p class="text-xs text-slate-400 font-mono">Fundição por Levitação Magnética & Plasma Controlado</p>
            </div>
        </div>

        <!-- System Status Pills -->
        <div class="flex items-center gap-3 text-xs font-mono flex-wrap">
            <div class="flex items-center gap-2 px-3 py-1.5 rounded-full bg-slate-900 border border-slate-700">
                <span id="mhd-status-dot" class="w-2.5 h-2.5 rounded-full bg-emerald-500 animate-ping"></span>
                <span>Reator MHD: <strong id="mhd-status-text" class="text-emerald-400">ESTÁVEL (14.2 Tesla)</strong></span>
            </div>
            <div class="flex items-center gap-2 px-3 py-1.5 rounded-full bg-slate-900 border border-slate-700">
                <span class="w-2.5 h-2.5 rounded-full bg-cyan-500"></span>
                <span>Contato com Paredes: <strong class="text-cyan-400">0.000% (Zero Contaminação)</strong></span>
            </div>
            <div class="flex items-center gap-2 px-3 py-1.5 rounded-full bg-slate-900 border border-slate-700">
                <span class="w-2.5 h-2.5 rounded-full bg-purple-500"></span>
                <span>Pureza da Liga: <strong class="text-purple-400">99.9999%</strong></span>
            </div>
        </div>
    </header>

    <!-- Main Workspace -->
    <main class="flex-1 grid grid-cols-1 lg:grid-cols-12 gap-6 p-6 max-w-[1700px] mx-auto w-full">
        
        <!-- Left Sidebar: Alloy Recipes & MHD Controls -->
        <section class="lg:col-span-3 flex flex-col gap-6">
            
            <!-- Alloy Recipe Selection -->
            <div class="glass-panel rounded-2xl p-5 shadow-xl">
                <h2 class="text-sm font-semibold tracking-wide text-cyan-400 uppercase mb-4 flex items-center gap-2">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z"/></svg>
                    Receitas de Ligas Hipercondutoras
                </h2>
                <div class="space-y-3">
                    <button onclick="setAlloy('superconductor')" id="alloy-superconductor" class="w-full text-left p-3 rounded-xl border border-cyan-500/40 bg-cyan-500/10 transition-all hover:bg-cyan-500/20 flex items-center justify-between group">
                        <div>
                            <div class="font-semibold text-sm text-cyan-300">Titanium-Graphene Hipercondutor</div>
                            <div class="text-xs text-slate-400">Zero resistência elétrica a temperatura ambiente</div>
                        </div>
                        <span class="w-2 h-2 rounded-full bg-cyan-400"></span>
                    </button>
                    <button onclick="setAlloy('tungsten')" id="alloy-tungsten" class="w-full text-left p-3 rounded-xl border border-slate-700 bg-slate-900/60 transition-all hover:border-amber-500/40 flex items-center justify-between group">
                        <div>
                            <div class="font-semibold text-sm text-slate-200 group-hover:text-amber-300">Tungstênio-Plasma Quântico</div>
                            <div class="text-xs text-slate-400">Resistência térmica extrema para reatores de fusão</div>
                        </div>
                        <span class="w-2 h-2 rounded-full bg-slate-600" id="dot-tungsten"></span>
                    </button>
                    <button onclick="setAlloy('exotic')" id="alloy-exotic" class="w-full text-left p-3 rounded-xl border border-slate-700 bg-slate-900/60 transition-all hover:border-purple-500/40 flex items-center justify-between group">
                        <div>
                            <div class="font-semibold text-sm text-slate-200 group-hover:text-purple-300">Elemento X-9 Estelar</div>
                            <div class="text-xs text-slate-400">Matéria ultra-leve e densidade modulada</div>
                        </div>
                        <span class="w-2 h-2 rounded-full bg-slate-600" id="dot-exotic"></span>
                    </button>
                </div>
            </div>

            <!-- MHD Reactor Control Unit -->
            <div class="glass-panel rounded-2xl p-5 shadow-xl border-cyan-500/30">
                <div class="flex items-center justify-between mb-4">
                    <h2 class="text-sm font-semibold tracking-wide text-cyan-400 uppercase flex items-center gap-2">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/></svg>
                        Parâmetros MHD
                    </h2>
                    <span id="mhd-badge" class="px-2.5 py-0.5 rounded text-xs font-mono font-bold bg-cyan-500/20 text-cyan-300 border border-cyan-500/40">ATIVO</span>
                </div>
                
                <div class="space-y-4">
                    <div class="flex items-center justify-between bg-slate-900/80 p-3 rounded-xl border border-slate-800">
                        <div>
                            <div class="text-xs font-medium text-slate-300">Levitação Magnética Pura</div>
                            <div class="text-[10px] text-slate-400 font-mono">Isolamento total de paredes</div>
                        </div>
                        <label class="relative inline-flex items-center cursor-pointer">
                            <input type="checkbox" id="mhdToggle" checked onchange="toggleMHD()" class="sr-only peer">
                            <div class="w-11 h-6 bg-slate-700 peer-focus:outline-none rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-cyan-500"></div>
                        </label>
                    </div>

                    <div>
                        <div class="flex justify-between text-xs mb-1 font-mono">
                            <span class="text-slate-400">Intensidade do Campo Magnético (Tesla)</span>
                            <span id="tesla-val" class="text-cyan-400">14.2 T</span>
                        </div>
                        <input type="range" id="magneticIntensity" min="5" max="30" value="14" oninput="updateTesla(this.value)" class="w-full h-2 bg-slate-800 rounded-lg appearance-none cursor-pointer accent-cyan-400">
                    </div>

                    <div>
                        <div class="flex justify-between text-xs mb-1 font-mono">
                            <span class="text-slate-400">Temperatura do Plasma (Kelvin)</span>
                            <span class="text-amber-400">6,500 K</span>
                        </div>
                        <input type="range" min="3000" max="15000" step="500" value="6500" class="w-full h-2 bg-slate-800 rounded-lg appearance-none cursor-pointer accent-amber-400">
                    </div>
                </div>
            </div>

            <!-- Action Triggers -->
            <div class="glass-panel rounded-2xl p-5 shadow-xl flex flex-col gap-3">
                <h2 class="text-sm font-semibold tracking-wide text-cyan-400 uppercase mb-1">Comandos de Fundição</h2>
                <button onclick="triggerAlloyInject()" class="w-full py-3 px-4 rounded-xl bg-gradient-to-r from-cyan-600 to-amber-600 hover:from-cyan-500 hover:to-amber-500 text-white font-semibold text-sm shadow-lg shadow-cyan-900/30 transition-all flex items-center justify-center gap-2">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"/></svg>
                    Injetar Elementos Raros na Gosma
                </button>
                <button onclick="solidifyAlloy()" class="w-full py-2.5 px-4 rounded-xl bg-slate-900 hover:bg-slate-800 border border-slate-700 text-slate-300 font-medium text-xs transition-all flex items-center justify-center gap-2">
                    <svg class="w-4 h-4 text-emerald-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                    Resfriamento por Indução & Forjamento Final
                </button>
            </div>

        </section>

        <!-- Center: Canvas 2D Simulation Viewport -->
        <section class="lg:col-span-6 flex flex-col gap-6">
            <div class="glass-panel rounded-2xl p-4 shadow-2xl relative flex flex-col overflow-hidden border-cyan-500/30">
                
                <!-- Viewport Header HUD -->
                <div class="flex items-center justify-between pb-3 mb-3 border-b border-slate-800 text-xs font-mono">
                    <div class="flex items-center gap-2">
                        <span class="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span>
                        <span class="text-slate-300">CÂMARA DE VÁCUO MHD - LEVITAÇÃO MAGNÉTICA EM TEMPO REAL</span>
                    </div>
                    <div class="flex items-center gap-4 text-slate-400">
                        <span>Estado: <strong id="hud-state" class="text-cyan-400">FLUIDO LEVITANTE</strong></span>
                        <span>Contaminação: <strong id="hud-contamination" class="text-emerald-400">0.000 ppm</strong></span>
                    </div>
                </div>

                <!-- Canvas Container -->
                <div class="relative w-full aspect-[4/3] bg-slate-950 rounded-xl overflow-hidden border border-slate-800 shadow-inner">
                    <canvas id="simCanvas" class="w-full h-full block"></canvas>
                    
                    <!-- HUD Instructions / Legend -->
                    <div class="absolute bottom-4 left-4 pointer-events-none bg-slate-900/80 backdrop-blur-md px-3 py-2 rounded-lg border border-cyan-500/30 text-[11px] font-mono text-cyan-300 space-y-1">
                        <div>🧲 Bobinas magnéticas mantêm o metal fundido suspenso no vácuo</div>
                        <div>⚡ Plasma e campos eletromagnéticos misturam a liga perfeitamente</div>
                    </div>

                    <!-- Solidification Success Banner -->
                    <div id="success-banner" class="absolute top-4 inset-x-4 pointer-events-none hidden transition-all duration-300">
                        <div class="bg-emerald-950/90 border border-emerald-400 text-emerald-200 px-4 py-2 rounded-xl text-xs font-mono font-bold flex items-center justify-center gap-2 animate-bounce">
                            <svg class="w-4 h-4 text-emerald-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                            PEÇA FORJADA COM SUCESSO! HIERARQUIA HIPERCONDUTORA ATINGIDA SEM CONTATO COM PAREDES!
                        </div>
                    </div>
                </div>

                <!-- Quick Metrics Bar -->
                <div class="grid grid-cols-3 gap-3 mt-4 text-center font-mono">
                    <div class="bg-slate-900/60 p-2.5 rounded-xl border border-slate-800">
                        <div class="text-[10px] text-slate-400">Condutividade Elétrica</div>
                        <div id="metric-conductivity" class="text-sm font-bold text-cyan-400">10,400 MS/m</div>
                    </div>
                    <div class="bg-slate-900/60 p-2.5 rounded-xl border border-slate-800">
                        <div class="text-[10px] text-slate-400">Estabilidade da Levitação</div>
                        <div id="metric-levitation" class="text-sm font-bold text-emerald-400">100.0%</div>
                    </div>
                    <div class="bg-slate-900/60 p-2.5 rounded-xl border border-slate-800">
                        <div class="text-[10px] text-slate-400">Resistência à Tração</div>
                        <div id="metric-tensile" class="text-sm font-bold text-purple-400">4.8 GPa</div>
                    </div>
                </div>

            </div>
        </section>

        <!-- Right Sidebar: Telemetry & MHD Industrial Console -->
        <section class="lg:col-span-3 flex flex-col gap-6">
            
            <!-- Material Properties -->
            <div class="glass-panel rounded-2xl p-5 shadow-xl">
                <h2 class="text-sm font-semibold tracking-wide text-cyan-400 uppercase mb-4 flex items-center gap-2">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 3v2m6-2v2M9 19v2m6-2v2M5 9H3m2 6H3m18-6h-2m2 6h-2M7 19h10a2 2 0 002-2V7a2 2 0 00-2-2H7a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
                    Propriedades Atômicas da Liga
                </h2>
                <div class="space-y-3 font-mono text-xs">
                    <div class="flex justify-between items-center bg-slate-900/80 p-2.5 rounded-xl border border-slate-800">
                        <span class="text-slate-400">Densidade Atômica</span>
                        <span class="text-cyan-400 font-bold">4.21 g/cm³</span>
                    </div>
                    <div class="flex justify-between items-center bg-slate-900/80 p-2.5 rounded-xl border border-slate-800">
                        <span class="text-slate-400">Ponto de Fusão</span>
                        <span class="text-amber-400 font-bold">3,850 °C</span>
                    </div>
                    <div class="flex justify-between items-center bg-slate-900/80 p-2.5 rounded-xl border border-slate-800">
                        <span class="text-slate-400">Inclusões de Impureza</span>
                        <span class="text-emerald-400 font-bold">0.00001%</span>
                    </div>
                    <div class="flex justify-between items-center bg-slate-900/80 p-2.5 rounded-xl border border-slate-800">
                        <span class="text-slate-400">Eficiência do Reator</span>
                        <span class="text-purple-400 font-bold">99.94%</span>
                    </div>
                </div>
            </div>

            <!-- MHD AI Console -->
            <div class="glass-panel rounded-2xl p-5 shadow-xl flex flex-col flex-1 min-h-[260px]">
                <h2 class="text-sm font-semibold tracking-wide text-cyan-400 uppercase mb-3 flex items-center gap-2">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 9l3 3-3 3m5 0h3M5 20h14a2 2 0 002-2V6a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"/></svg>
                    Console MHD Industrial AI
                </h2>
                <div id="ai-console" class="flex-1 bg-slate-950/80 rounded-xl p-3 border border-slate-900 font-mono text-[11px] text-slate-300 space-y-1.5 overflow-y-auto max-h-[220px]">
                    <div class="text-slate-500">[00:00:01] Reator MHD e bobinas de levitação ativadas.</div>
                    <div class="text-cyan-400">[00:00:03] Câmara de vácuo purgada para 10^-9 Torr.</div>
                    <div class="text-amber-400">[00:00:05] Plasma gerado a 6,500 K. Gotas metálicas em suspensão magnética pura.</div>
                </div>
            </div>

        </section>

    </main>

    <!-- Footer -->
    <footer class="text-center py-4 text-xs text-slate-500 border-t border-slate-900 font-mono">
        MHD Reactor & Levitação Magnética Pura &bull; Indústria Pesada e Manufatura Avançada v3.2
    </footer>

    <!-- JavaScript Simulation Engine -->
    <script>
        // --- Simulation State ---
        let state = {
            alloy: 'superconductor', // 'superconductor', 'tungsten', 'exotic'
            mhdActive: true,
            magneticTesla: 14,
            time: 0,
            moltenState: 'liquid', // 'liquid', 'solidifying', 'solid'
            particles: []
        };

        // DOM Elements
        const canvas = document.getElementById('simCanvas');
        const ctx = canvas.getContext('2d');
        const mhdToggleEl = document.getElementById('mhdToggle');
        const mhdBadgeEl = document.getElementById('mhd-badge');
        const mhdStatusTextEl = document.getElementById('mhd-status-text');
        const successBannerEl = document.getElementById('success-banner');
        const hudStateEl = document.getElementById('hud-state');
        const hudContaminationEl = document.getElementById('hud-contamination');
        const aiConsole = document.getElementById('ai-console');

        // Audio Helper
        let audioCtx = null;
        function initAudio() {
            if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
        }

        function playBeep(freq = 440, type = 'sine', duration = 0.1) {
            try {
                initAudio();
                if (!audioCtx) return;
                const osc = audioCtx.createOscillator();
                const gain = audioCtx.createGain();
                osc.type = type;
                osc.frequency.value = freq;
                gain.gain.setValueAtTime(0.04, audioCtx.currentTime);
                gain.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime + duration);
                osc.connect(gain);
                gain.connect(audioCtx.destination);
                osc.start();
                osc.stop(audioCtx.currentTime + duration);
            } catch (e) {}
        }

        // Initialize molten particles inside droplet
        function initParticles() {
            state.particles = [];
            for (let i = 0; i < 50; i++) {
                state.particles.push({
                    angle: Math.random() * Math.PI * 2,
                    dist: Math.random() * 55,
                    speed: 0.02 + Math.random() * 0.04,
                    size: 2 + Math.random() * 3,
                    color: Math.random() > 0.5 ? '#06b6d4' : '#f59e0b'
                });
            }
        }

        // Resize Canvas
        function resizeCanvas() {
            const rect = canvas.getBoundingClientRect();
            canvas.width = rect.width * window.devicePixelRatio;
            canvas.height = rect.height * window.devicePixelRatio;
            ctx.setTransform(window.devicePixelRatio, 0, 0, window.devicePixelRatio, 0, 0);
            if (state.particles.length === 0) initParticles();
        }

        window.addEventListener('resize', resizeCanvas);

        // Control Handlers
        function setAlloy(all) {
            state.alloy = all;
            ['superconductor', 'tungsten', 'exotic'].forEach(a => {
                const btn = document.getElementById(`alloy-${a}`);
                if (a === all) {
                    btn.className = "w-full text-left p-3 rounded-xl border border-cyan-500/40 bg-cyan-500/10 transition-all flex items-center justify-between group";
                } else {
                    btn.className = "w-full text-left p-3 rounded-xl border border-slate-700 bg-slate-900/60 transition-all hover:border-slate-500 flex items-center justify-between group";
                }
            });

            if (all === 'superconductor') {
                logAI("Liga selecionada: Titanium-Graphene Hipercondutor.");
                playBeep(520, 'sine', 0.15);
            } else if (all === 'tungsten') {
                logAI("Liga selecionada: Tungstênio-Plasma Quântico.");
                playBeep(440, 'triangle', 0.15);
            } else {
                logAI("Liga selecionada: Elemento X-9 Estelar.");
                playBeep(680, 'sine', 0.15);
            }
            state.moltenState = 'liquid';
        }

        function toggleMHD() {
            state.mhdActive = mhdToggleEl.checked;
            if (state.mhdActive) {
                mhdBadgeEl.textContent = "ATIVO";
                mhdBadgeEl.className = "px-2.5 py-0.5 rounded text-xs font-mono font-bold bg-cyan-500/20 text-cyan-300 border border-cyan-500/40";
                mhdStatusTextEl.textContent = `ESTÁVEL (${state.magneticTesla}.2 Tesla)`;
                logAI("Reator MHD reativado: Levitação magnética restaurada no vácuo.");
                playBeep(880, 'sine', 0.2);
            } else {
                mhdBadgeEl.textContent = "QUEDA DE CAMPO";
                mhdBadgeEl.className = "px-2.5 py-0.5 rounded text-xs font-mono font-bold bg-rose-500/20 text-rose-300 border border-rose-500/40";
                mhdStatusTextEl.textContent = "ALERTA (Metal colidiu com as paredes!)";
                logAI("⚠️ ALERTA CRÍTICO: Campo magnético desligado! O metal fundido caiu nas paredes e foi contaminado!");
                playBeep(180, 'sawtooth', 0.4);
            }
        }

        function updateTesla(val) {
            state.magneticTesla = parseInt(val);
            document.getElementById('tesla-val').textContent = val + ' T';
            if (state.mhdActive) {
                mhdStatusTextEl.textContent = `ESTÁVEL (${val}.0 Tesla)`;
            }
        }

        function triggerAlloyInject() {
            logAI("⚡ Injeção de elementos raros na gotícula levitada. Agitação por indução eletromagnética iniciada.");
            playBeep(950, 'square', 0.25);
            // Add extra swirl particles
            for (let i = 0; i < 20; i++) {
                state.particles.push({
                    angle: Math.random() * Math.PI * 2,
                    dist: 10 + Math.random() * 40,
                    speed: 0.05 + Math.random() * 0.05,
                    size: 3,
                    color: '#10b981'
                });
            }
        }

        function solidifyAlloy() {
            if (!state.mhdActive) {
                logAI("❌ Erro: Impossível solidificar com pureza sem o campo MHD ativo.");
                playBeep(220, 'sawtooth', 0.3);
                return;
            }
            state.moltenState = 'solidifying';
            successBannerEl.classList.remove('hidden');
            logAI("❄️ Resfriamento por indução quântica ativado. Gotícula solidificando mantendo levitação perfeita.");
            playBeep(1200, 'square', 0.3);

            setTimeout(() => {
                successBannerEl.classList.add('hidden');
                state.moltenState = 'solid';
                logAI("✨ Peça forjada com estrutura cristalina perfeita sem nenhuma inclusão de impureza.");
            }, 3500);
        }

        function logAI(message) {
            const timeStr = new Date().toTimeString().split(' ')[0];
            const div = document.createElement('div');
            div.className = "text-slate-300";
            div.innerHTML = `<span class="text-slate-500">[${timeStr}]</span> ${message}`;
            aiConsole.appendChild(div);
            aiConsole.scrollTop = aiConsole.scrollHeight;
        }

        // --- Main Animation & Simulation Loop ---
        function updateSimulation() {
            state.time += 0.04;

            // Update particle positions
            state.particles.forEach(p => {
                p.angle += p.speed;
            });

            drawCanvas();
            requestAnimationFrame(updateSimulation);
        }

        function drawCanvas() {
            const width = canvas.clientWidth;
            const height = canvas.clientHeight;
            
            ctx.clearRect(0, 0, width, height);

            // Draw vacuum chamber interior (dark metallic tech ring)
            const centerX = width / 2;
            const centerY = height / 2;
            const chamberRadius = Math.min(width, height) * 0.38;

            ctx.fillStyle = '#060913';
            ctx.beginPath();
            ctx.arc(centerX, centerY, chamberRadius, 0, Math.PI * 2);
            ctx.fill();

            // Chamber Wall (Titanium Casing with magnetic induction coils)
            ctx.strokeStyle = state.mhdActive ? '#06b6d4' : '#f43f5e';
            ctx.lineWidth = 4;
            ctx.beginPath();
            ctx.arc(centerX, centerY, chamberRadius, 0, Math.PI * 2);
            ctx.stroke();

            // Draw Induction Coils around chamber perimeter
            for (let i = 0; i < 12; i++) {
                const angle = (i * Math.PI * 2) / 12;
                const cx = centerX + Math.cos(angle) * (chamberRadius - 15);
                const cy = centerY + Math.sin(angle) * (chamberRadius - 15);
                ctx.fillStyle = state.mhdActive ? '#10b981' : '#f43f5e';
                ctx.beginPath();
                ctx.arc(cx, cy, 6, 0, Math.PI * 2);
                ctx.fill();
            }

            // If MHD is OFF, the molten metal drops to the bottom wall and gets contaminated
            let dropletX = centerX;
            let dropletY = centerY + Math.sin(state.time * 3) * 8;
            let dropletRadius = 65;

            if (!state.mhdActive) {
                dropletX = centerX;
                dropletY = chamberRadius - 35; // fallen to the bottom wall
                dropletRadius = 70;
            }

            // Draw Magnetic Field Flux Lines (if MHD is Active)
            if (state.mhdActive) {
                ctx.strokeStyle = 'rgba(6, 182, 212, 0.25)';
                ctx.lineWidth = 1.5;
                for (let i = 0; i < 6; i++) {
                    const ringR = 20 + i * 22 + Math.sin(state.time * 5 + i) * 4;
                    ctx.beginPath();
                    ctx.arc(centerX, centerY, ringR, 0, Math.PI * 2);
                    ctx.stroke();
                }

                // Plasma Arcs connecting coils to droplet
                for (let i = 0; i < 4; i++) {
                    const coilAngle = state.time * 2 + (i * Math.PI / 2);
                    const startX = centerX + Math.cos(coilAngle) * (chamberRadius - 20);
                    const startY = centerY + Math.sin(coilAngle) * (chamberRadius - 20);
                    const endX = dropletX + Math.cos(coilAngle + Math.PI) * dropletRadius * 0.8;
                    const endY = dropletY + Math.sin(coilAngle + Math.PI) * dropletRadius * 0.8;

                    ctx.strokeStyle = 'rgba(245, 158, 11, 0.6)';
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.moveTo(startX, startY);
                    ctx.quadraticCurveTo(centerX + Math.cos(coilAngle) * 30, centerY + Math.sin(coilAngle) * 30, endX, endY);
                    ctx.stroke();
                }
            }

            // Draw Levitated Molten Metal Droplet (or Solidified Final Part)
            ctx.save();
            if (state.moltenState === 'solid') {
                // Forged solid metallic part (Diamond-like sheen)
                ctx.fillStyle = '#94a3b8';
                ctx.strokeStyle = '#38bdf8';
                ctx.lineWidth = 3;
                ctx.beginPath();
                // Draw a sleek hexagonal/advanced geometric ingot
                for (let i = 0; i < 6; i++) {
                    const ang = (i * Math.PI / 3) + 0.5;
                    const px = dropletX + Math.cos(ang) * 55;
                    const py = dropletY + Math.sin(ang) * 55;
                    if (i === 0) ctx.moveTo(px, py);
                    else ctx.lineTo(px, py);
                }
                ctx.closePath();
                ctx.fill();
                ctx.stroke();
            } else {
                // Molten Metal Droplet
                const grad = ctx.createRadialGradient(dropletX - 15, dropletY - 15, 5, dropletX, dropletY, dropletRadius);
                if (state.mhdActive) {
                    grad.addColorStop(0, '#fef08a'); // glowing hot core
                    grad.addColorStop(0.5, '#f59e0b');
                    grad.addColorStop(1, '#c2410c');
                } else {
                    grad.addColorStop(0, '#64748b'); // contaminated dull metal on wall
                    grad.addColorStop(1, '#0f172a');
                }

                ctx.fillStyle = grad;
                ctx.shadowColor = state.mhdActive ? '#f59e0b' : '#000000';
                ctx.shadowBlur = state.mhdActive ? 25 : 0;
                ctx.beginPath();
                // Slightly organic pulsing shape for molten liquid
                const pulseX = dropletRadius + Math.sin(state.time * 8) * 4;
                const pulseY = dropletRadius + Math.cos(state.time * 7) * 4;
                ctx.ellipse(dropletX, dropletY, pulseX, pulseY, 0, 0, Math.PI * 2);
                ctx.fill();
                ctx.shadowBlur = 0; // reset

                // Draw swirl internal particles inside molten metal
                if (state.mhdActive) {
                    state.particles.forEach(p => {
                        const px = dropletX + Math.cos(p.angle) * p.dist * 0.7;
                        const py = dropletY + Math.sin(p.angle) * p.dist * 0.7;
                        ctx.fillStyle = p.color;
                        ctx.beginPath();
                        ctx.arc(px, py, p.size, 0, Math.PI * 2);
                        ctx.fill();
                    });
                }
            }
            ctx.restore();

            // Update HUD values dynamically
            if (state.mhdActive) {
                if (state.moltenState === 'solid') {
                    hudStateEl.textContent = "PEÇA FORJADA SÓLIDA";
                    hudStateEl.className = "text-emerald-400 font-bold";
                    hudContaminationEl.textContent = "0.000 ppm (Perfeito)";
                } else if (state.moltenState === 'solidifying') {
                    hudStateEl.textContent = "RESFRIAMENTO POR INDUÇÃO";
                    hudStateEl.className = "text-amber-400 font-bold";
                    hudContaminationEl.textContent = "0.000 ppm";
                } else {
                    hudStateEl.textContent = "FLUIDO LEVITANTE";
                    hudStateEl.className = "text-cyan-400 font-bold";
                    hudContaminationEl.textContent = "0.000 ppm";
                }
            } else {
                hudStateEl.textContent = "COLIDIDO COM PARED!";
                hudStateEl.className = "text-rose-400 font-bold";
                hudContaminationEl.textContent = "42,500 ppm (Contaminado!)";
            }
        }

        // Initialize on load
        window.onload = function() {
            resizeCanvas();
            updateSimulation();
        };
    </script>
</body>
</html>
