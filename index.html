[webar_hercules_beetle_specimen_metamorphosis.html](https://github.com/user-attachments/files/35314307/webar_hercules_beetle_specimen_metamorphosis.html)
<!DOCTYPE html>
<html lang="zh-TW" class="h-full w-full">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>WebAR 赫克力士長戟大兜蟲 - 3D 超高精細生態與完全變態展覽</title>

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Three.js r128 -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <!-- OrbitControls -->
    <script src="https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/controls/OrbitControls.js"></script>
    <!-- GSAP for smooth timeline & camera animations -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <!-- Phosphor Icons -->
    <script src="https://unpkg.com/@phosphor-icons/web"></script>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,600;0,700;1,400&family=Noto+Serif+TC:wght@500;700&family=Noto+Sans+TC:wght@300;400;500;700&display=swap" rel="stylesheet">

    <style>
        body {
            font-family: 'Noto Sans TC', sans-serif;
            overflow: hidden;
            background-color: #06090e;
            color: #f8fafc;
            user-select: none;
            -webkit-user-select: none;
            touch-action: none;
        }

        .font-serif-title {
            font-family: 'Cormorant Garamond', 'Noto Serif TC', serif;
        }

        .glass-hud {
            background: rgba(11, 16, 26, 0.86);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);
            border: 1px solid rgba(234, 179, 8, 0.34);
            box-shadow: 0 18px 40px rgba(0, 0, 0, 0.68), inset 0 0 16px rgba(234, 179, 8, 0.06);
        }

        .btn-hud {
            transition: all 0.22s cubic-bezier(0.16, 1, 0.3, 1);
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(234, 179, 8, 0.32);
            color: #f1f5f9;
        }

        .btn-hud:hover, .btn-hud:active {
            background: rgba(234, 179, 8, 0.22);
            border-color: rgba(250, 204, 21, 0.9);
            color: #fef08a;
            box-shadow: 0 0 16px rgba(234, 179, 8, 0.35);
        }

        .btn-hud.active {
            background: linear-gradient(135deg, rgba(234, 179, 8, 0.38), rgba(180, 83, 9, 0.55));
            border-color: #facc15;
            color: #ffffff;
            box-shadow: 0 0 22px rgba(234, 179, 8, 0.5);
        }

        /* Custom Range Slider */
        input[type=range] {
            -webkit-appearance: none;
            background: transparent;
        }
        input[type=range]:focus {
            outline: none;
        }
        input[type=range]::-webkit-slider-runnable-track {
            height: 6px;
            background: rgba(255, 255, 255, 0.14);
            border-radius: 999px;
            border: 1px solid rgba(234, 179, 8, 0.35);
        }
        input[type=range]::-webkit-slider-thumb {
            -webkit-appearance: none;
            height: 18px;
            width: 18px;
            border-radius: 50%;
            background: #facc15;
            margin-top: -7px;
            box-shadow: 0 0 14px rgba(250, 204, 21, 0.9);
            cursor: pointer;
            transition: transform 0.15s ease;
        }
        input[type=range]::-webkit-slider-thumb:hover {
            transform: scale(1.2);
        }

        /* 3D Screen-Space Callout Markers */
        .ar-marker {
            background: rgba(10, 15, 24, 0.92);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(250, 204, 21, 0.55);
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.7), 0 0 12px rgba(234, 179, 8, 0.3);
            transform: translate(-50%, -50%);
            transition: opacity 0.2s ease, transform 0.2s ease, border-color 0.2s ease;
        }
        .ar-marker:hover, .ar-marker.selected {
            transform: translate(-50%, -50%) scale(1.08);
            border-color: #fef08a;
            background: rgba(28, 36, 52, 0.98);
            z-index: 30;
        }

        /* AR Target Scanner Reticle */
        @keyframes reticlePulse {
            0%, 100% { transform: scale(0.98); opacity: 0.45; }
            50% { transform: scale(1.02); opacity: 0.95; }
        }
        .reticle-pulse {
            animation: reticlePulse 2.4s infinite ease-in-out;
        }

        /* Live Camera Video Background */
        #ar-camera-feed {
            position: fixed;
            inset: 0;
            width: 100vw;
            height: 100vh;
            object-fit: cover;
            z-index: 0;
        }
    </style>
</head>
<body class="h-full w-full relative">

    <!-- Loading Screen -->
    <div id="loader" class="fixed inset-0 z-50 flex flex-col items-center justify-center bg-[#06090e] text-amber-400 transition-opacity duration-500">
        <div class="relative flex items-center justify-center mb-5">
            <div class="w-20 h-20 border-4 border-amber-500/20 border-t-amber-400 rounded-full animate-spin"></div>
            <i class="ph-light ph-bug text-4xl absolute animate-pulse text-amber-300"></i>
        </div>
        <h2 class="font-serif-title text-2xl sm:text-3xl font-bold tracking-widest text-slate-100">赫克力士長戟大兜蟲 WebAR</h2>
        <p class="text-xs text-amber-400/75 font-mono mt-2 tracking-wider">正在建構 Dynastes hercules 高精細幾丁質法線貼圖與絨毛結構...</p>
    </div>

    <!-- Toast Notification Banner -->
    <div id="toast-banner" class="fixed top-24 left-1/2 -translate-x-1/2 z-50 pointer-events-none opacity-0 transition-all duration-300 transform -translate-y-3">
        <div class="glass-hud px-4 py-2.5 rounded-full flex items-center space-x-2 border-amber-400/60 shadow-2xl">
            <i id="toast-icon" class="ph-fill ph-sparkle text-amber-400 text-base"></i>
            <span id="toast-text" class="text-xs sm:text-sm font-medium text-amber-100 whitespace-nowrap">提示訊息</span>
        </div>
    </div>

    <!-- Live Camera Video Layer for WebAR -->
    <video id="ar-camera-feed" autoplay playsinline muted class="hidden"></video>

    <!-- 3D WebGL Canvas Layer -->
    <div id="webgl-container" class="fixed inset-0 z-10"></div>

    <!-- 3D Floating Callout Markers Overlay -->
    <div id="markers-container" class="fixed inset-0 z-20 pointer-events-none overflow-hidden"></div>

    <!-- AR Target Scanner Overlay -->
    <div id="ar-scanner-overlay" class="fixed inset-0 z-15 pointer-events-none flex flex-col items-center justify-center transition-opacity duration-500 opacity-0">
        <div class="w-64 h-64 sm:w-80 sm:h-80 border-2 border-dashed border-amber-400/75 rounded-full reticle-pulse flex flex-col items-center justify-between p-5 bg-amber-400/5">
            <div class="w-full flex justify-center text-amber-400">
                <span class="text-[10px] font-mono tracking-widest uppercase bg-slate-950/80 px-2.5 py-0.5 rounded-full border border-amber-500/40">AR Surface Lock</span>
            </div>
            <div class="text-center px-3.5 py-2 rounded-xl bg-slate-950/85 border border-amber-500/40 text-amber-200 text-xs shadow-lg">
                <i class="ph-light ph-scan text-amber-400 mr-1"></i>將鏡頭對準桌面或手掌，點擊螢幕引導大兜蟲飛舞
            </div>
            <div class="w-full flex justify-center text-amber-400">
                <span class="text-[10px] font-mono text-emerald-400 bg-slate-950/80 px-2 py-0.5 rounded-full">60 FPS Live Tracking</span>
            </div>
        </div>
    </div>

    <!-- Top Header Navigation Bar -->
    <header class="fixed top-3 left-3 right-3 sm:top-4 sm:left-4 sm:right-4 z-30 flex flex-col lg:flex-row justify-between items-start lg:items-center gap-2.5 pointer-events-none">
        <!-- Exhibition Title Card -->
        <div class="glass-hud rounded-2xl p-3 sm:p-3.5 flex items-center space-x-3 pointer-events-auto border-l-4 border-l-amber-400">
            <div class="w-10 h-10 sm:w-11 sm:h-11 rounded-xl bg-amber-950/90 border border-amber-500/50 flex items-center justify-center text-amber-400 text-2xl shrink-0">
                <i class="ph-light ph-bug"></i>
            </div>
            <div>
                <div class="flex items-center space-x-1.5 flex-wrap gap-y-1">
                    <span class="text-[10px] tracking-widest font-mono uppercase text-amber-300 font-semibold px-2 py-0.5 rounded bg-amber-950 border border-amber-700/60">WebAR 3D 活體生態</span>
                    <span id="badge-mode" class="text-[10px] tracking-wider font-mono text-emerald-300 px-2 py-0.5 rounded bg-emerald-950/90 border border-emerald-700/60">3D 微距展廳</span>
                </div>
                <h1 class="font-serif-title text-lg sm:text-2xl font-bold tracking-wide text-slate-100 mt-0.5">
                    赫克力士長戟大兜蟲 <span class="text-xs font-normal text-amber-200/75 italic hidden sm:inline">Dynastes hercules</span>
                </h1>
            </div>
        </div>

        <!-- Action Toolbar -->
        <div class="glass-hud rounded-2xl p-2 flex items-center flex-wrap gap-1.5 pointer-events-auto">
            <!-- Hero Action: Take Flight -->
            <button id="btn-fly-out" class="btn-hud active px-3.5 py-2 rounded-xl text-xs font-bold text-amber-200 flex items-center space-x-1.5">
                <i id="icon-fly-out" class="ph-fill ph-sparkle text-base text-amber-300"></i>
                <span id="txt-fly-out">展翅起飛！</span>
            </button>

            <!-- Exploded Anatomy View -->
            <button id="btn-explode" class="btn-hud px-3 py-2 rounded-xl text-xs font-medium flex items-center space-x-1.5" title="立體解剖結構拆解">
                <i class="ph-light ph-arrows-out-cardinal text-base text-amber-400"></i>
                <span class="hidden sm:inline">結構拆解</span>
            </button>

            <!-- Toggle Live Camera AR -->
            <button id="btn-toggle-camera" class="btn-hud px-3 py-2 rounded-xl text-xs font-medium flex items-center space-x-1.5">
                <i class="ph-light ph-camera text-base text-cyan-400"></i>
                <span id="txt-camera-mode">實景相機 AR</span>
            </button>

            <!-- AR Snapshot Photo -->
            <button id="btn-snapshot" class="btn-hud px-3 py-2 rounded-xl text-xs font-medium flex items-center space-x-1.5" title="拍攝 AR 合照留念">
                <i class="ph-light ph-aperture text-base text-emerald-400"></i>
                <span class="hidden md:inline">拍照留念</span>
            </button>

            <!-- QR Code Modal Trigger -->
            <button id="btn-open-qr" class="btn-hud px-3 py-2 rounded-xl text-xs font-medium flex items-center space-x-1.5" title="手機掃描 QR Code">
                <i class="ph-light ph-qr-code text-base text-amber-400"></i>
                <span class="hidden lg:inline">QR Code</span>
            </button>

            <!-- Auto Orbit Toggle -->
            <button id="btn-auto-rotate" class="btn-hud p-2 rounded-xl text-xs text-emerald-300" title="360° 環繞展示">
                <i class="ph-light ph-orbit text-base"></i>
            </button>

            <!-- Toggle Labels -->
            <button id="btn-toggle-labels" class="btn-hud active p-2 rounded-xl text-xs text-amber-300" title="顯示/隱藏解剖標籤">
                <i class="ph-light ph-tag text-base"></i>
            </button>

            <!-- Toggle Audio -->
            <button id="btn-toggle-audio" class="btn-hud p-2 rounded-xl text-xs text-amber-300" title="音效開關">
                <i id="icon-audio" class="ph-light ph-speaker-high text-base"></i>
            </button>

            <!-- Reset Camera -->
            <button id="btn-reset-view" class="btn-hud p-2 rounded-xl text-xs text-slate-300" title="重置視角">
                <i class="ph-light ph-arrows-counter-clockwise text-base"></i>
            </button>
        </div>
    </header>

    <!-- Bottom Interactive Controls & Anatomical Inspector -->
    <main class="fixed bottom-3 left-3 right-3 sm:bottom-4 sm:left-4 sm:right-4 z-30 flex flex-col md:flex-row justify-between items-end gap-3 pointer-events-none">

        <!-- Left Control Panel: 4-Stage Metamorphosis, Humidity Color Shift & Subspecies -->
        <section class="glass-hud rounded-2xl p-3.5 sm:p-4 w-full md:w-[430px] pointer-events-auto space-y-3">
            <div class="flex justify-between items-center border-b border-amber-500/20 pb-2">
                <span class="text-xs font-bold text-amber-400 tracking-wider uppercase flex items-center">
                    <i class="ph-light ph-arrows-clockwise text-base mr-1.5"></i>3D 完全變態與感濕特性 (Metamorphosis)
                </span>
                <span id="lbl-stage-name" class="text-[11px] font-mono text-amber-200 bg-amber-950/90 border border-amber-700/50 px-2 py-0.5 rounded">4. 成蟲活體 (100%)</span>
            </div>

            <!-- 4 Life Stage Quick Buttons -->
            <div class="grid grid-cols-4 gap-1.5">
                <button id="btn-stage-1" class="btn-hud py-2 px-1 rounded-xl text-center text-[11px] font-medium flex flex-col items-center">
                    <i class="ph-light ph-egg text-base mb-0.5 text-lime-400"></i>
                    <span>1. 卵與幼蟲</span>
                </button>
                <button id="btn-stage-2" class="btn-hud py-2 px-1 rounded-xl text-center text-[11px] font-medium flex flex-col items-center">
                    <i class="ph-light ph-hourglass-medium text-base mb-0.5 text-amber-400"></i>
                    <span>2. 蛹室化蛹</span>
                </button>
                <button id="btn-stage-3" class="btn-hud py-2 px-1 rounded-xl text-center text-[11px] font-medium flex flex-col items-center">
                    <i class="ph-light ph-rays text-base mb-0.5 text-cyan-400"></i>
                    <span>3. 破蛹羽化</span>
                </button>
                <button id="btn-stage-4" class="btn-hud active py-2 px-1 rounded-xl text-center text-[11px] font-medium flex flex-col items-center">
                    <i class="ph-light ph-bug text-base mb-0.5 text-amber-300"></i>
                    <span>4. 成蟲飛舞</span>
                </button>
            </div>

            <!-- Continuous Metamorphosis Timeline Scrubber -->
            <div class="space-y-1">
                <div class="flex justify-between text-[11px] text-slate-300">
                    <span class="text-amber-200/90">生命週期進度 (卵 → 蠐螬幼蟲 → 蛹 → 成蟲)：</span>
                    <span id="val-progress" class="font-mono text-amber-400 font-semibold">100%</span>
                </div>
                <input id="slider-metamorphosis" type="range" min="0" max="100" value="100" class="w-full">
            </div>

            <!-- Hygroscopic Elytra Humidity Slider -->
            <div class="space-y-1 pt-1 border-t border-slate-800/80">
                <div class="flex justify-between text-[11px] text-slate-300">
                    <span class="text-cyan-200/90 flex items-center">
                        <i class="ph-light ph-drop text-cyan-400 mr-1"></i>環境濕度感濕變色 (鞘翅海綿層)：
                    </span>
                    <span id="val-humidity" class="font-mono text-cyan-300 font-semibold">25% 乾燥金黃</span>
                </div>
                <input id="slider-humidity" type="range" min="0" max="100" value="25" class="w-full">
            </div>

            <!-- Subspecies Switcher -->
            <div class="flex items-center justify-between pt-1.5 border-t border-slate-800/80 gap-1.5">
                <span class="text-xs text-slate-400 font-mono shrink-0">亞種型態：</span>
                <div class="flex items-center gap-1.5 flex-wrap justify-end">
                    <button id="species-ecuatorianus" class="btn-hud active px-2.5 py-1 rounded-lg text-xs font-medium">厄瓜多長戟</button>
                    <button id="species-hercules" class="btn-hud px-2.5 py-1 rounded-lg text-xs font-medium">原名亞種</button>
                    <button id="species-lichyi" class="btn-hud px-2.5 py-1 rounded-lg text-xs font-medium">里奇長戟</button>
                </div>
            </div>
        </section>

        <!-- Right Card: Educational Anatomical & Life Stage Inspector -->
        <aside id="info-card" class="glass-hud rounded-2xl p-4 w-full md:w-80 pointer-events-auto space-y-2 transition-all duration-300 opacity-0 translate-y-4 pointer-events-none">
            <div class="flex justify-between items-center border-b border-amber-500/20 pb-1.5">
                <span id="info-badge" class="text-[11px] font-bold text-amber-400 uppercase tracking-wider flex items-center">
                    <i class="ph-light ph-magnifying-glass text-base mr-1.5"></i>甲蟲生態百科解析
                </span>
                <button id="btn-close-info" class="text-slate-400 hover:text-amber-300 p-1 rounded-lg">
                    <i class="ph-light ph-x text-base"></i>
                </button>
            </div>
            <h3 id="info-title" class="font-serif-title text-lg font-bold text-amber-200">解剖特徵</h3>
            <p id="info-desc" class="text-xs text-slate-300 leading-relaxed">
                點擊模型上的解剖標籤或切換生命階段，探索世界最大甲蟲的微觀構造與完全變態奧秘。
            </p>
        </aside>
    </main>

    <!-- QR Code Scan Modal -->
    <div id="modal-qr" class="fixed inset-0 z-40 bg-black/75 backdrop-blur-md flex items-center justify-center p-4 opacity-0 pointer-events-none transition-opacity duration-300">
        <div class="glass-hud rounded-3xl p-6 max-w-sm w-full text-center space-y-4 border border-amber-400/50 shadow-2xl">
            <div class="w-12 h-12 rounded-2xl bg-amber-500/20 border border-amber-400/50 flex items-center justify-center text-amber-300 text-2xl mx-auto">
                <i class="ph-light ph-qr-code"></i>
            </div>
            <div>
                <h3 class="font-serif-title text-2xl font-bold text-amber-200">免下載 WebAR 互動導覽</h3>
                <p class="text-xs text-slate-300 leading-relaxed mt-2">
                    家長只需用手機相機掃描 QR Code，點擊「實景相機 AR」對準桌面或手掌，赫克力士長戟大兜蟲便會張開鞘翅展翅飛舞！
                </p>
            </div>
            <div class="bg-white p-3.5 rounded-2xl inline-block shadow-inner border-2 border-amber-400">
                <canvas id="qr-canvas" width="168" height="168" class="block"></canvas>
            </div>
            <div class="text-[11px] font-mono text-amber-300/80">支援 iOS Safari / Android Chrome 無需安裝 App</div>
            <button id="btn-close-qr" class="btn-hud active w-full py-2.5 rounded-xl text-xs font-bold">返回 AR 互動體驗</button>
        </div>
    </div>

    <script>
        /* =====================================================================
           1. GLOBAL STATE & CONFIGURATION
        ===================================================================== */
        let scene, camera, renderer, controls, clock;
        let environmentPedestal;
        let beetleGroup, pronotumGroup, thoracicHornGroup, headHornGroup, abdomenGroup, legsGroup;
        let leftElytronHinge, rightElytronHinge, leftHindwingHinge, rightHindwingHinge;
        let elytraMaterial, blackChitinMaterial, velvetBrushMaterial, hindwingMaterial, abdomenMaterial;
        let larvaGroup, pupaGroup, pupaShellMat, particleSystem, targetBeacon;

        let currentSubspecies = 'ecuatorianus';
        let metamorphosisProgress = 100; // 0 to 100
        let humidityLevel = 0.25; // 0 to 1
        let isFlyOut = false;
        let isExploded = false;
        let showLabels = true;
        let isAudioOn = true;
        let audioCtx = null;
        let isCameraAR = false;
        let videoStream = null;
        let flightTargetOffset = new THREE.Vector3(0, 0.85, 0.2);

        const subspeciesCatalog = {
            ecuatorianus: {
                zhName: '厄瓜多長戟大兜蟲',
                latinName: 'Dynastes hercules ecuatorianus',
                code: 'SPECIMEN #01-EC',
                baseHue: '#eab308',
                spotDensity: 1.0,
                striationStrength: 1.0
            },
            hercules: {
                zhName: '赫克力士原名亞種',
                latinName: 'Dynastes hercules hercules',
                code: 'SPECIMEN #02-HR',
                baseHue: '#ca8a04',
                spotDensity: 1.45,
                striationStrength: 0.75
            },
            lichyi: {
                zhName: '里奇長戟大兜蟲',
                latinName: 'Dynastes hercules lichyi',
                code: 'SPECIMEN #03-LC',
                baseHue: '#d97706',
                spotDensity: 0.65,
                striationStrength: 1.15
            }
        };

        const calloutHotspots = [
            {
                id: 'thoracic-horn',
                label: '極長胸角與金黃絨毛刷',
                localPos: new THREE.Vector3(0, 0.62, -2.15),
                stageReq: 'adult',
                title: '流線胸角與金黃絨毛刷 (Thoracic Horn & Setae Brush)',
                desc: '由前胸背板向前大幅延伸的漆黑長角，背脊具微細刻點，下緣密生數百根橙黃色天鵝絨狀剛毛刷（Setae），能感應氣流與穩固夾持對手，體長最高可達 180mm！'
            },
            {
                id: 'head-horn',
                label: '多齒頭角與鰓葉觸角',
                localPos: new THREE.Vector3(0, 0.14, -1.72),
                stageReq: 'adult',
                title: '多齒頭角、複眼與鰓葉狀觸角 (Head Horn & Antennae)',
                desc: '頭部向前上方彎曲延伸的強壯頭角，上緣具數枚銳利三角刺齒，能與上方胸角精密閉合；兩側具高光澤複眼與金龜子科特有的扇形鰓葉狀觸角。'
            },
            {
                id: 'pronotum',
                label: '黑曜石前胸背板與小盾板',
                localPos: new THREE.Vector3(0, 0.76, -0.35),
                stageReq: 'adult',
                title: '前胸背板、側角突與小盾板 (Pronotum & Scutellum)',
                desc: '黑曜石般高光澤革質外骨骼，前緣兩側具銳利前胸側角突，頸部與小盾板周圍環繞金黃絨毛，內部容納驅動胸角夾鉗與前足的強大肌肉群。'
            },
            {
                id: 'elytra',
                label: '海綿微孔感濕鞘翅',
                localPos: new THREE.Vector3(0.72, 0.68, 0.92),
                stageReq: 'adult',
                title: '海綿微孔感濕鞘翅 (Hygroscopic Elytra)',
                desc: '鞘翅表皮下具有奈米級海綿狀光子晶體層！乾燥時空氣填充孔隙折射出金黃與橄欖縱向條紋；高濕度吸收水氣後則轉為深沉黑褐色。'
            },
            {
                id: 'hindwing',
                label: '琥珀膜質飛行後翅',
                localPos: new THREE.Vector3(-1.45, 0.56, 0.85),
                stageReq: 'flying',
                title: '折疊式膜質飛行後翅 (Membranous Hindwings)',
                desc: '平時精巧折疊收納於堅硬鞘翅之下；起飛時左右鞘翅水平張開，具前緣脈、徑脈與中脈支撐的琥珀色半透明後翅迅速展開並高頻拍動。'
            },
            {
                id: 'legs',
                label: '鋸齒脛節與五節跗節雙爪',
                localPos: new THREE.Vector3(1.38, -0.22, -0.95),
                stageReq: 'adult',
                title: '鋸齒脛節、五節跗節與雙爪 (Serrated Tibia & 5-Segment Tarsus)',
                desc: '每條腿皆由基節、腿節、具三枚銳利外齒的脛節、五節念珠狀跗節及末端彎曲雙爪組成，能在熱帶雨林樹幹上產生驚人抓地力。'
            },
            {
                id: 'larva',
                label: '腐植土與蠐螬幼蟲',
                localPos: new THREE.Vector3(0, 0.65, 0.15),
                stageReq: 'larva',
                title: '完全變態：三齡蠐螬幼蟲期 (Scarab Larva)',
                desc: '長戟大兜蟲幼蟲期長達 1.5 至 2 年，棲息於腐朽木屑中，呈 C 字型乳白色肉蟲，體側具褐點氣門，胸部具三對關節胸足與強健大顎，體重可突破 120 公克。'
            },
            {
                id: 'pupa',
                label: '土繭蛹室與巨角離蛹',
                localPos: new THREE.Vector3(0, 0.82, 0.25),
                stageReq: 'pupa',
                title: '完全變態：蛹室化蛹期 (Exarate Beetle Pupa)',
                desc: '終齡幼蟲在腐植土中壓實築成橢圓形「蛹室」，蛻皮化為金琥珀色的離蛹，此時已能清楚看見折疊的六足、翅芽以及雄偉的胸角與頭角雛形！'
            }
        ];

        let markerDOMList = [];

        /* =====================================================================
           2. UI FEEDBACK: TOAST & PROCEDURAL AUDIO
        ===================================================================== */
        let toastTimeout = null;
        function showToast(message, iconClass = 'ph-fill ph-sparkle text-amber-400') {
            const banner = document.getElementById('toast-banner');
            document.getElementById('toast-text').innerText = message;
            document.getElementById('toast-icon').className = `${iconClass} text-base`;
            banner.classList.remove('opacity-0', '-translate-y-3');
            banner.classList.add('opacity-100', 'translate-y-0');

            clearTimeout(toastTimeout);
            toastTimeout = setTimeout(() => {
                banner.classList.remove('opacity-100', 'translate-y-0');
                banner.classList.add('opacity-0', '-translate-y-3');
            }, 2800);
        }

        function playSound(type) {
            if (!isAudioOn) return;
            try {
                if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
                if (audioCtx.state === 'suspended') audioCtx.resume();

                const now = audioCtx.currentTime;
                const osc = audioCtx.createOscillator();
                const gain = audioCtx.createGain();

                if (type === 'click') {
                    osc.type = 'sine';
                    osc.frequency.setValueAtTime(580, now);
                    osc.frequency.exponentialRampToValueAtTime(220, now + 0.05);
                    gain.gain.setValueAtTime(0.08, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.05);
                    osc.connect(gain);
                    gain.connect(audioCtx.destination);
                    osc.start(now);
                    osc.stop(now + 0.05);
                } else if (type === 'flyout') {
                    // Deep resonant beetle wing-hum + majestic ascending chime
                    const notes = [329.63, 440.0, 554.37, 659.25];
                    notes.forEach((freq, idx) => {
                        const o = audioCtx.createOscillator();
                        const g = audioCtx.createGain();
                        o.type = 'triangle';
                        o.frequency.setValueAtTime(freq, now + idx * 0.08);
                        g.gain.setValueAtTime(0.09, now + idx * 0.08);
                        g.gain.exponentialRampToValueAtTime(0.001, now + idx * 0.08 + 0.55);
                        o.connect(g);
                        g.connect(audioCtx.destination);
                        o.start(now + idx * 0.08);
                        o.stop(now + idx * 0.08 + 0.55);
                    });
                } else if (type === 'shutter') {
                    osc.type = 'square';
                    osc.frequency.setValueAtTime(900, now);
                    osc.frequency.exponentialRampToValueAtTime(120, now + 0.08);
                    gain.gain.setValueAtTime(0.1, now);
                    gain.gain.exponentialRampToValueAtTime(0.001, now + 0.08);
                    osc.connect(gain);
                    gain.connect(audioCtx.destination);
                    osc.start(now);
                    osc.stop(now + 0.08);
                }
            } catch (e) {}
        }

        /* =====================================================================
           3. PROCEDURAL ULTRA-HD PBR TEXTURES (COLOR + NORMAL + ROUGHNESS)
              u = 0 (Center Dorsal Suture) -> u = 1 (Outer Lateral Margin)
              v = 0 (Anterior Pronotum Edge) -> v = 1 (Posterior Apex)
        ===================================================================== */
        function generateElytraPBRTextures(subspeciesKey, humidity) {
            const size = 1024;
            const canvasColor = document.createElement('canvas');
            canvasColor.width = size;
            canvasColor.height = size;
            const ctx = canvasColor.getContext('2d');

            const canvasNorm = document.createElement('canvas');
            canvasNorm.width = size;
            canvasNorm.height = size;
            const ctxN = canvasNorm.getContext('2d');

            const canvasRough = document.createElement('canvas');
            canvasRough.width = size;
            canvasRough.height = size;
            const ctxR = canvasRough.getContext('2d');

            const spec = subspeciesCatalog[subspeciesKey];

            // Compute hygroscopic color interpolation based on humidity (0.0 -> 1.0)
            const dryColor = new THREE.Color(spec.baseHue);
            const oliveColor = new THREE.Color('#857a24');
            const humidColor = new THREE.Color('#191510');

            const currentBase = new THREE.Color();
            if (humidity < 0.5) {
                currentBase.lerpColors(dryColor, oliveColor, humidity * 2.0);
            } else {
                currentBase.lerpColors(oliveColor, humidColor, (humidity - 0.5) * 2.0);
            }

            const centerHex = '#' + currentBase.clone().offsetHSL(0, 0.05, 0.07).getHexString();
            const midHex = '#' + currentBase.getHexString();
            const edgeHex = '#' + currentBase.clone().offsetHSL(0, -0.04, -0.14).getHexString();

            // 1. Color Base Gradient
            const grad = ctx.createLinearGradient(0, 0, size, size * 0.25);
            grad.addColorStop(0, edgeHex);
            grad.addColorStop(0.18, centerHex);
            grad.addColorStop(0.75, midHex);
            grad.addColorStop(1, edgeHex);
            ctx.fillStyle = grad;
            ctx.fillRect(0, 0, size, size);

            // 2. Normal Map Base (neutral RGB 128,128,255) & Roughness Base
            ctxN.fillStyle = 'rgb(128, 128, 255)';
            ctxN.fillRect(0, 0, size, size);

            ctxR.fillStyle = 'rgb(42, 42, 42)'; // Glossy lacquer chitin
            ctxR.fillRect(0, 0, size, size);

            // 3. Longitudinal Striations (Color + Normal Ridge Grooves)
            const stripeCount = 16;
            for (let s = 1; s < stripeCount; s++) {
                const uX = (s / stripeCount) * size;
                const alpha = (0.14 + (s % 2) * 0.08) * spec.striationStrength * (1 - humidity * 0.65);

                // Color striation
                ctx.strokeStyle = `rgba(20, 16, 8, ${alpha})`;
                ctx.lineWidth = s % 3 === 0 ? 7 : 4;
                ctx.beginPath();
                ctx.moveTo(uX, 0);
                ctx.bezierCurveTo(
                    uX + Math.sin(s) * 14, size * 0.35,
                    uX - Math.cos(s) * 12, size * 0.72,
                    uX * 0.92, size
                );
                ctx.stroke();

                // Normal groove relief
                ctxN.strokeStyle = 'rgba(105, 128, 245, 0.45)';
                ctxN.lineWidth = 5;
                ctxN.beginPath();
                ctxN.moveTo(uX, 0);
                ctxN.bezierCurveTo(
                    uX + Math.sin(s) * 14, size * 0.35,
                    uX - Math.cos(s) * 12, size * 0.72,
                    uX * 0.92, size
                );
                ctxN.stroke();
            }

            // 4. Deterministic Pseudo-Random Organic Spots & Microscopic Chitin Punctures
            let seed = subspeciesKey === 'ecuatorianus' ? 104729 : (subspeciesKey === 'hercules' ? 224737 : 350377);
            const rand = () => {
                seed = (seed * 1664525 + 1013904223) % 4294967296;
                return seed / 4294967296;
            };

            // Microscopic chitin dimples across normal & roughness maps
            for (let p = 0; p < 1800; p++) {
                const px = rand() * size;
                const py = rand() * size;
                const pr = 1.2 + rand() * 2.2;
                ctxN.fillStyle = 'rgba(110, 115, 235, 0.38)';
                ctxN.beginPath();
                ctxN.arc(px, py, pr, 0, Math.PI * 2);
                ctxN.fill();

                ctxR.fillStyle = 'rgba(85, 85, 85, 0.35)';
                ctxR.beginPath();
                ctxR.arc(px, py, pr, 0, Math.PI * 2);
                ctxR.fill();
            }

            const drawOrganicSpot = (cx, cy, radius) => {
                ctx.fillStyle = '#0c0b09';
                ctx.beginPath();
                const pts = 9;
                for (let p = 0; p < pts; p++) {
                    const ang = (p / pts) * Math.PI * 2;
                    const rad = radius * (0.68 + rand() * 0.62);
                    const px = cx + Math.cos(ang) * rad * 0.85;
                    const py = cy + Math.sin(ang) * rad * 1.25;
                    if (p === 0) ctx.moveTo(px, py);
                    else ctx.lineTo(px, py);
                }
                ctx.closePath();
                ctx.fill();
            };

            const totalSpots = Math.floor(235 * spec.spotDensity);
            for (let i = 0; i < totalSpots; i++) {
                const sx = (0.04 + rand() * 0.92) * size;
                const sy = (0.03 + rand() * 0.94) * size;
                let sr = 4 + rand() * 14;
                if (rand() > 0.92) sr *= 2.1;
                drawOrganicSpot(sx, sy, sr);

                if (sr > 13) {
                    for (let k = 0; k < 3; k++) {
                        drawOrganicSpot(
                            sx + (rand() - 0.5) * 44,
                            sy + (rand() - 0.5) * 56,
                            2.5 + rand() * 4.5
                        );
                    }
                }
            }

            // 5. Dark Dorsal Suture Line (u = 0) & Outer Lateral Rim (u = 1)
            ctx.fillStyle = '#120f0a';
            ctx.fillRect(0, 0, 22, size);
            ctx.fillRect(size - 26, 0, 26, size);
            ctx.fillRect(0, 0, size, 18);
            ctx.fillRect(0, size - 22, size, 22);

            // Raised bevel normal along dorsal suture
            ctxN.fillStyle = 'rgb(155, 128, 255)';
            ctxN.fillRect(0, 0, 18, size);

            const map = new THREE.CanvasTexture(canvasColor);
            const normalMap = new THREE.CanvasTexture(canvasNorm);
            const roughnessMap = new THREE.CanvasTexture(canvasRough);
            map.anisotropy = 8;
            normalMap.anisotropy = 8;
            return { map, normalMap, roughnessMap };
        }

        function generateChitinMicroNormalMap() {
            const size = 512;
            const canvas = document.createElement('canvas');
            canvas.width = size;
            canvas.height = size;
            const ctx = canvas.getContext('2d');

            ctx.fillStyle = 'rgb(128, 128, 255)';
            ctx.fillRect(0, 0, size, size);

            let seed = 881723;
            const rand = () => {
                seed = (seed * 1664525 + 1013904223) % 4294967296;
                return seed / 4294967296;
            };

            // Fine chitin punctures (刻點) for Pronotum & Horns
            for (let i = 0; i < 2400; i++) {
                const x = rand() * size;
                const y = rand() * size;
                const r = 0.8 + rand() * 1.8;
                ctx.fillStyle = 'rgba(108, 112, 232, 0.45)';
                ctx.beginPath();
                ctx.arc(x, y, r, 0, Math.PI * 2);
                ctx.fill();
            }

            const tex = new THREE.CanvasTexture(canvas);
            tex.wrapS = THREE.RepeatWrapping;
            tex.wrapT = THREE.RepeatWrapping;
            tex.repeat.set(3, 3);
            return tex;
        }

        function generateHindwingTexture() {
            const size = 1024;
            const canvas = document.createElement('canvas');
            canvas.width = size;
            canvas.height = size;
            const ctx = canvas.getContext('2d');

            // Translucent warm amber membrane
            const grad = ctx.createLinearGradient(0, 0, size, size * 0.45);
            grad.addColorStop(0, 'rgba(146, 64, 14, 0.88)');
            grad.addColorStop(0.45, 'rgba(217, 119, 6, 0.72)');
            grad.addColorStop(1, 'rgba(251, 191, 36, 0.44)');
            ctx.fillStyle = grad;
            ctx.fillRect(0, 0, size, size);

            // Chitinous Coleopteran Wing Veins (Costa, Subcosta, Radius, Media, Cubitus)
            ctx.strokeStyle = 'rgba(69, 26, 3, 0.88)';
            ctx.lineCap = 'round';
            const veins = [
                { w: 14, pts: [[0, size * 0.12], [size * 0.52, size * 0.10], [size * 0.97, size * 0.18]] },
                { w: 11, pts: [[0, size * 0.20], [size * 0.48, size * 0.26], [size * 0.95, size * 0.40]] },
                { w: 8,  pts: [[size * 0.34, size * 0.20], [size * 0.65, size * 0.54], [size * 0.88, size * 0.80]] },
                { w: 7,  pts: [[0, size * 0.30], [size * 0.36, size * 0.62], [size * 0.64, size * 0.94]] },
                { w: 5,  pts: [[size * 0.15, size * 0.42], [size * 0.28, size * 0.72], [size * 0.40, size * 0.95]] }
            ];
            veins.forEach(v => {
                ctx.lineWidth = v.w;
                ctx.beginPath();
                ctx.moveTo(v.pts[0][0], v.pts[0][1]);
                ctx.quadraticCurveTo(v.pts[1][0], v.pts[1][1], v.pts[2][0], v.pts[2][1]);
                ctx.stroke();
            });

            // Dark Pterostigma (翅痣) near costal hinge
            ctx.fillStyle = 'rgba(45, 18, 4, 0.82)';
            ctx.beginPath();
            ctx.ellipse(size * 0.54, size * 0.14, 46, 16, 0.08, 0, Math.PI * 2);
            ctx.fill();

            // Folding crease lines
            ctx.strokeStyle = 'rgba(254, 243, 199, 0.26)';
            ctx.lineWidth = 3;
            ctx.setLineDash([12, 10]);
            ctx.beginPath();
            ctx.moveTo(size * 0.52, size * 0.14);
            ctx.lineTo(size * 0.46, size * 0.88);
            ctx.stroke();
            ctx.setLineDash([]);

            const tex = new THREE.CanvasTexture(canvas);
            tex.anisotropy = 8;
            return tex;
        }

        /* =====================================================================
           4. SYMMETRICAL ELYTRA & HINDWING GEOMETRY BUILDERS (CONFORMAL UVS)
        ===================================================================== */
        function buildRightElytronGeometry() {
            const segsU = 36;
            const segsV = 44;
            const lengthZ = 2.26;

            const positions = [];
            const uvs = [];
            const indices = [];

            for (let iv = 0; iv <= segsV; iv++) {
                const v = iv / segsV; // 0 = anterior base, 1 = posterior tip
                const z = v * lengthZ;

                // Width envelope: broad shoulder, slight mid-body swell, smooth pointed apex
                const taper = Math.pow(Math.max(0, 1 - Math.pow(v, 1.85)), 0.56);
                const shoulder = 0.94 + 0.08 * Math.sin(Math.min(1, v * 2.5) * Math.PI);
                const halfWidth = 0.86 * shoulder * taper;

                // Dorsal arch height profile from pronotum junction to posterior tip
                const domeTop = 0.26 + 0.11 * Math.sin(v * Math.PI * 0.78) - 0.52 * Math.pow(v, 2.2);
                const dropDepth = 0.56 * taper + 0.04 * (1 - v);

                for (let iu = 0; iu <= segsU; iu++) {
                    const u = iu / segsU; // 0 = medial suture (x=0), 1 = lateral margin
                    const theta = u * (Math.PI * 0.54);

                    const x = Math.sin(theta) * halfWidth;
                    const y = domeTop - (1 - Math.cos(theta)) * dropDepth;

                    positions.push(x, y, z);
                    uvs.push(u, v);
                }
            }

            for (let iv = 0; iv < segsV; iv++) {
                for (let iu = 0; iu < segsU; iu++) {
                    const a = iv * (segsU + 1) + iu;
                    const b = a + 1;
                    const c = (iv + 1) * (segsU + 1) + iu;
                    const d = c + 1;
                    indices.push(a, c, b);
                    indices.push(b, c, d);
                }
            }

            const geo = new THREE.BufferGeometry();
            geo.setAttribute('position', new THREE.Float32BufferAttribute(positions, 3));
            geo.setAttribute('uv', new THREE.Float32BufferAttribute(uvs, 2));
            geo.setIndex(indices);
            geo.computeVertexNormals();
            return geo;
        }

        function buildRightHindwingGeometry() {
            const segsU = 28;
            const segsV = 18;
            const spanX = 2.38;

            const positions = [];
            const uvs = [];
            const indices = [];

            for (let iu = 0; iu <= segsU; iu++) {
                const u = iu / segsU; // 0 = wing root, 1 = wing tip
                const x = u * spanX;

                // Leading costal edge sweeps slightly back; trailing edge forms broad aerodynamic fan
                const leadingZ = -0.14 * Math.sin(u * Math.PI * 0.85) + 0.18 * Math.pow(u, 1.6);
                const chord = (0.34 + 0.72 * Math.sin(Math.pow(u, 0.72) * Math.PI)) * (1 - 0.15 * Math.pow(u, 3));

                // Gentle camber arch
                const camberY = 0.06 * Math.sin(u * Math.PI);

                for (let iv = 0; iv <= segsV; iv++) {
                    const v = iv / segsV; // 0 = leading edge, 1 = trailing edge
                    const z = leadingZ + v * chord;
                    const y = camberY * (1 - Math.pow(v - 0.35, 2));

                    positions.push(x, y, z);
                    uvs.push(u, v);
                }
            }

            for (let iu = 0; iu < segsU; iu++) {
                for (let iv = 0; iv < segsV; iv++) {
                    const a = iu * (segsV + 1) + iv;
                    const b = a + 1;
                    const c = (iu + 1) * (segsV + 1) + iv;
                    const d = c + 1;
                    indices.push(a, b, c);
                    indices.push(b, d, c);
                }
            }

            const geo = new THREE.BufferGeometry();
            geo.setAttribute('position', new THREE.Float32BufferAttribute(positions, 3));
            geo.setAttribute('uv', new THREE.Float32BufferAttribute(uvs, 2));
            geo.setIndex(indices);
            geo.computeVertexNormals();
            return geo;
        }

        function mirrorGeometryX(sourceGeo) {
            const mirrored = sourceGeo.clone();
            const pos = mirrored.attributes.position;
            for (let i = 0; i < pos.count; i++) {
                pos.setX(i, -pos.getX(i));
            }
            pos.needsUpdate = true;

            const idx = mirrored.getIndex();
            if (idx) {
                const arr = idx.array;
                for (let i = 0; i < arr.length; i += 3) {
                    const tmp = arr[i + 1];
                    arr[i + 1] = arr[i + 2];
                    arr[i + 2] = tmp;
                }
                idx.needsUpdate = true;
            }
            mirrored.computeVertexNormals();
            return mirrored;
        }

        /* =====================================================================
           5. BUILD HYPER-DETAILED 3D HERCULES BEETLE (DYNASTES HERCULES)
        ===================================================================== */
        function createHerculesBeetleModel() {
            beetleGroup = new THREE.Group();

            const chitinNormal = generateChitinMicroNormalMap();
            const elytraPBR = generateElytraPBRTextures(currentSubspecies, humidityLevel);

            // Materials
            blackChitinMaterial = new THREE.MeshPhysicalMaterial({
                color: 0x0e0f13,
                normalMap: chitinNormal,
                normalScale: new THREE.Vector2(0.28, 0.28),
                roughness: 0.14,
                metalness: 0.34,
                clearcoat: 0.96,
                clearcoatRoughness: 0.05
            });

            velvetBrushMaterial = new THREE.MeshStandardMaterial({
                color: 0xd97706,
                roughness: 0.88,
                metalness: 0.05
            });

            elytraMaterial = new THREE.MeshPhysicalMaterial({
                map: elytraPBR.map,
                normalMap: elytraPBR.normalMap,
                normalScale: new THREE.Vector2(0.45, 0.45),
                roughnessMap: elytraPBR.roughnessMap,
                roughness: 0.16,
                metalness: 0.08,
                clearcoat: 0.94,
                clearcoatRoughness: 0.06,
                side: THREE.DoubleSide
            });

            hindwingMaterial = new THREE.MeshPhysicalMaterial({
                map: generateHindwingTexture(),
                roughness: 0.30,
                metalness: 0.05,
                transparent: true,
                opacity: 0.80,
                side: THREE.DoubleSide
            });

            abdomenMaterial = new THREE.MeshStandardMaterial({
                color: 0x18130e,
                normalMap: chitinNormal,
                normalScale: new THREE.Vector2(0.35, 0.35),
                roughness: 0.72,
                metalness: 0.14
            });

            // 1. SOLID ABDOMEN, THORAX STERNITES & GOLDEN PUBESCENCE (腹部、胸板與氣門)
            abdomenGroup = new THREE.Group();
            const abdomenGeo = new THREE.SphereGeometry(1, 36, 28);
            abdomenGeo.scale(0.84, 0.36, 1.12);
            const abdomenMesh = new THREE.Mesh(abdomenGeo, abdomenMaterial);
            abdomenMesh.position.set(0, 0.02, 1.12);
            abdomenMesh.castShadow = true;
            abdomenMesh.receiveShadow = true;
            abdomenGroup.add(abdomenMesh);

            // Segmented sternites & lateral spiracles on abdomen
            for (let s = 0; s < 6; s++) {
                const ring = new THREE.Mesh(
                    new THREE.CylinderGeometry(0.76 - s * 0.08, 0.72 - s * 0.09, 0.17, 24),
                    abdomenMaterial
                );
                ring.rotation.x = Math.PI / 2;
                ring.scale.set(1.06, 1.0, 0.45);
                ring.position.set(0, -0.09, 0.56 + s * 0.27);
                abdomenGroup.add(ring);

                // Spiracle openings along flanks
                [-1, 1].forEach(side => {
                    const spiracle = new THREE.Mesh(
                        new THREE.SphereGeometry(0.022, 8, 8),
                        velvetBrushMaterial
                    );
                    spiracle.position.set(side * (0.76 - s * 0.08), 0.08, 0.56 + s * 0.27);
                    abdomenGroup.add(spiracle);
                });
            }

            // Metasternum & Ventral Golden Pubescence (胸部腹面金黃絨毛)
            const thoraxVenter = new THREE.Mesh(
                new THREE.SphereGeometry(0.68, 24, 18),
                blackChitinMaterial
            );
            thoraxVenter.scale.set(1.12, 0.48, 0.85);
            thoraxVenter.position.set(0, -0.10, -0.18);
            abdomenGroup.add(thoraxVenter);

            const ventralFur = new THREE.Mesh(
                new THREE.SphereGeometry(0.56, 20, 16),
                velvetBrushMaterial
            );
            ventralFur.scale.set(1.08, 0.34, 0.78);
            ventralFur.position.set(0, -0.17, -0.22);
            abdomenGroup.add(ventralFur);

            beetleGroup.add(abdomenGroup);

            // 2. GLOSSY OBSIDIAN PRONOTUM, LATERAL TUBERCLES & SCUTELLUM (前胸背板、側角突與小盾板)
            pronotumGroup = new THREE.Group();
            const pronotumGeo = new THREE.SphereGeometry(1, 40, 32);
            pronotumGeo.scale(0.88, 0.56, 0.64);
            const pronotumMesh = new THREE.Mesh(pronotumGeo, blackChitinMaterial);
            pronotumMesh.position.set(0, 0.22, -0.36);
            pronotumMesh.castShadow = true;
            pronotumMesh.receiveShadow = true;
            pronotumGroup.add(pronotumMesh);

            // Anterior Lateral Pronotal Spines / Tubercles (前胸側角突)
            [-0.78, 0.78].forEach(px => {
                const tubercle = new THREE.Mesh(new THREE.ConeGeometry(0.085, 0.24, 12), blackChitinMaterial);
                tubercle.position.set(px, 0.16, -0.78);
                tubercle.rotation.set(-Math.PI * 0.42, 0, px > 0 ? -0.35 : 0.35);
                pronotumGroup.add(tubercle);
            });

            // Golden Neck Ruff Setae Collar (前胸前緣金黃絨毛環)
            const neckCollar = new THREE.Mesh(
                new THREE.TorusGeometry(0.36, 0.048, 10, 24, Math.PI * 1.15),
                velvetBrushMaterial
            );
            neckCollar.position.set(0, 0.22, -0.82);
            neckCollar.rotation.set(0.25, 0, -0.18);
            pronotumGroup.add(neckCollar);

            // Triangular Scutellum (小盾板) with golden border
            const scutellum = new THREE.Mesh(new THREE.ConeGeometry(0.17, 0.26, 3), blackChitinMaterial);
            scutellum.rotation.x = Math.PI / 2;
            scutellum.position.set(0, 0.38, 0.06);
            pronotumGroup.add(scutellum);

            beetleGroup.add(pronotumGroup);

            // 3. LONG CURVED THORACIC HORN & 3D INSTANCED GOLDEN VELVET BRUSH (極長胸角與立體絨毛刷)
            thoracicHornGroup = new THREE.Group();
            const hornPoints = [
                new THREE.Vector3(0, 0.44, -0.62),
                new THREE.Vector3(0, 0.58, -1.25),
                new THREE.Vector3(0, 0.62, -1.95),
                new THREE.Vector3(0, 0.56, -2.62),
                new THREE.Vector3(0, 0.44, -3.18)
            ];
            const hornCurve = new THREE.CatmullRomCurve3(hornPoints);

            const hornSegments = 40;
            const radialSegs = 20;
            const hornPositions = [];
            const hornIndices = [];
            const frames = hornCurve.computeFrenetFrames(hornSegments, false);

            for (let i = 0; i <= hornSegments; i++) {
                const t = i / hornSegments;
                const pt = hornCurve.getPointAt(t);
                const rx = 0.24 * Math.pow(1 - t, 0.72) + 0.022;
                const ry = 0.21 * Math.pow(1 - t, 0.68) + 0.022;

                const N = frames.normals[i];
                const B = frames.binormals[i];

                for (let j = 0; j <= radialSegs; j++) {
                    const ang = (j / radialSegs) * Math.PI * 2;
                    const cosA = Math.cos(ang);
                    const sinA = Math.sin(ang);

                    // Subtle dorsal keel ridge along top of horn
                    const keel = (cosA < -0.7) ? 0.018 * (1 - t) : 0;
                    const vx = pt.x + ((cosA * rx - keel) * N.x + sinA * ry * B.x);
                    const vy = pt.y + ((cosA * rx - keel) * N.y + sinA * ry * B.y);
                    const vz = pt.z + ((cosA * rx - keel) * N.z + sinA * ry * B.z);
                    hornPositions.push(vx, vy, vz);
                }
            }

            for (let i = 0; i < hornSegments; i++) {
                for (let j = 0; j < radialSegs; j++) {
                    const a = i * (radialSegs + 1) + j;
                    const b = a + 1;
                    const c = (i + 1) * (radialSegs + 1) + j;
                    const d = c + 1;
                    hornIndices.push(a, b, c);
                    hornIndices.push(b, d, c);
                }
            }

            const thoracicHornGeo = new THREE.BufferGeometry();
            thoracicHornGeo.setAttribute('position', new THREE.Float32BufferAttribute(hornPositions, 3));
            thoracicHornGeo.setIndex(hornIndices);
            thoracicHornGeo.computeVertexNormals();

            const thoracicHornMesh = new THREE.Mesh(thoracicHornGeo, blackChitinMaterial);
            thoracicHornMesh.castShadow = true;
            thoracicHornGroup.add(thoracicHornMesh);

            // Core velvet base strip underneath Thoracic Horn
            const brushPts = [];
            for (let k = 0; k <= 14; k++) {
                const bt = 0.18 + (k / 14) * 0.74;
                const p = hornCurve.getPointAt(bt);
                const offsetY = 0.13 * Math.pow(1 - bt, 0.65) + 0.018;
                brushPts.push(new THREE.Vector3(p.x, p.y - offsetY, p.z));
            }
            const brushCurve = new THREE.CatmullRomCurve3(brushPts);
            const brushCore = new THREE.Mesh(
                new THREE.TubeGeometry(brushCurve, 24, 0.042, 8, false),
                velvetBrushMaterial
            );
            thoracicHornGroup.add(brushCore);

            // 320 Individual 3D Golden Setae Bristles (InstancedMesh) for hyper-realistic fuzzy hair brush!
            const bristleCount = 320;
            const bristleGeo = new THREE.ConeGeometry(0.008, 0.13, 5);
            const bristleInstanced = new THREE.InstancedMesh(bristleGeo, velvetBrushMaterial, bristleCount);
            const dummy = new THREE.Object3D();

            for (let b = 0; b < bristleCount; b++) {
                const bt = 0.18 + (b / bristleCount) * 0.74;
                const p = hornCurve.getPointAt(bt);
                const offsetY = 0.13 * Math.pow(1 - bt, 0.65) + 0.02;
                const spreadX = ((b % 5) - 2) * 0.016 * (1 - bt * 0.5);

                dummy.position.set(p.x + spreadX, p.y - offsetY - 0.045, p.z);
                dummy.rotation.set(Math.PI + 0.22 + (Math.sin(b * 1.7) * 0.12), 0, spreadX * 3.5);
                const scaleLen = 0.75 + Math.sin(bt * Math.PI) * 0.55;
                dummy.scale.set(1, scaleLen, 1);
                dummy.updateMatrix();
                bristleInstanced.setMatrixAt(b, dummy.matrix);
            }
            thoracicHornGroup.add(bristleInstanced);

            // Basal Opposing Teeth on Thoracic Horn
            [-0.085, 0.085].forEach(tx => {
                const tTooth = new THREE.Mesh(new THREE.ConeGeometry(0.048, 0.20, 12), blackChitinMaterial);
                tTooth.position.set(tx, 0.36, -1.18);
                tTooth.rotation.x = Math.PI * 0.85;
                thoracicHornGroup.add(tTooth);
            });

            beetleGroup.add(thoracicHornGroup);

            // 4. ARTICULATED HEAD, COMPOUND EYES, LAMELLATE ANTENNAE & MULTI-TOOTHED HEAD HORN
            headHornGroup = new THREE.Group();
            headHornGroup.position.set(0, 0.04, -0.82);

            const headCapsule = new THREE.Mesh(new THREE.SphereGeometry(0.27, 24, 18), blackChitinMaterial);
            headCapsule.scale.set(1.16, 0.78, 1.06);
            headHornGroup.add(headCapsule);

            // Clypeus & Golden Labral Sensory Hairs (唇基與金黃感覺毛)
            const labrumBrush = new THREE.Mesh(new THREE.BoxGeometry(0.22, 0.04, 0.12), velvetBrushMaterial);
            labrumBrush.position.set(0, -0.10, -0.24);
            headHornGroup.add(labrumBrush);

            // Compound Eyes + Ocular Canthus Ridge (複眼與眼緣突)
            [-0.27, 0.27].forEach(ex => {
                const eye = new THREE.Mesh(
                    new THREE.SphereGeometry(0.09, 16, 16),
                    new THREE.MeshPhysicalMaterial({ color: 0x050508, roughness: 0.04, clearcoat: 1.0 })
                );
                eye.position.set(ex, 0.02, -0.05);
                headHornGroup.add(eye);

                const canthus = new THREE.Mesh(new THREE.BoxGeometry(0.08, 0.03, 0.12), blackChitinMaterial);
                canthus.position.set(ex * 1.02, 0.03, -0.07);
                headHornGroup.add(canthus);
            });

            // Curved Head Horn extending forward & upward toward Thoracic Horn
            const headCurve = new THREE.CatmullRomCurve3([
                new THREE.Vector3(0, 0.02, -0.18),
                new THREE.Vector3(0, 0.04, -0.75),
                new THREE.Vector3(0, 0.16, -1.32),
                new THREE.Vector3(0, 0.36, -1.78)
            ]);
            const headHornTube = new THREE.Mesh(
                new THREE.TubeGeometry(headCurve, 28, 0.076, 14, false),
                blackChitinMaterial
            );
            headHornTube.castShadow = true;
            headHornGroup.add(headHornTube);

            // Sharp tip of head horn
            const headTip = new THREE.Mesh(new THREE.ConeGeometry(0.076, 0.28, 14), blackChitinMaterial);
            headTip.position.set(0, 0.44, -1.86);
            headTip.rotation.set(-0.68, 0, 0);
            headHornGroup.add(headTip);

            // 3 Upward-Pointing Triangular Teeth on Head Horn
            const headTeethSpecs = [
                { z: -0.72, y: 0.10, scale: 0.85, rotX: -0.35 },
                { z: -1.18, y: 0.21, scale: 1.18, rotX: -0.45 },
                { z: -1.56, y: 0.34, scale: 0.95, rotX: -0.55 }
            ];
            headTeethSpecs.forEach(ts => {
                const tooth = new THREE.Mesh(new THREE.ConeGeometry(0.056 * ts.scale, 0.23 * ts.scale, 12), blackChitinMaterial);
                tooth.position.set(0, ts.y, ts.z);
                tooth.rotation.x = ts.rotX;
                headHornGroup.add(tooth);
            });

            // Segmented Lamellate Antennae (鰓葉狀觸角 — Scape, Funicle & 3-Leaf Fanned Club)
            [-1, 1].forEach(side => {
                const antCurve = new THREE.CatmullRomCurve3([
                    new THREE.Vector3(side * 0.22, -0.02, -0.16),
                    new THREE.Vector3(side * 0.38, -0.05, -0.34),
                    new THREE.Vector3(side * 0.50, -0.03, -0.48)
                ]);
                const antStem = new THREE.Mesh(new THREE.TubeGeometry(antCurve, 10, 0.014, 6, false), blackChitinMaterial);
                headHornGroup.add(antStem);

                // 3 Lamellate Club Leaves (鰓葉片)
                for (let leaf = 0; leaf < 3; leaf++) {
                    const lamella = new THREE.Mesh(
                        new THREE.BoxGeometry(0.075, 0.012, 0.028),
                        velvetBrushMaterial
                    );
                    lamella.position.set(side * (0.53 + leaf * 0.012), -0.03, -0.47 - leaf * 0.022);
                    lamella.rotation.y = side * (0.25 + leaf * 0.12);
                    headHornGroup.add(lamella);
                }
            });

            beetleGroup.add(headHornGroup);

            // 5. SYMMETRICAL, COMPLETE, HORIZONTAL ELYTRA (左右完全對稱、完整無縫鞘翅)
            const rightElytronGeo = buildRightElytronGeometry();
            const leftElytronGeo = mirrorGeometryX(rightElytronGeo);

            rightElytronHinge = new THREE.Group();
            rightElytronHinge.position.set(0.004, 0.36, 0.02);
            const rightElytronMesh = new THREE.Mesh(rightElytronGeo, elytraMaterial);
            rightElytronMesh.castShadow = true;
            rightElytronMesh.receiveShadow = true;
            rightElytronHinge.add(rightElytronMesh);
            beetleGroup.add(rightElytronHinge);

            leftElytronHinge = new THREE.Group();
            leftElytronHinge.position.set(-0.004, 0.36, 0.02);
            const leftElytronMesh = new THREE.Mesh(leftElytronGeo, elytraMaterial);
            leftElytronMesh.castShadow = true;
            leftElytronMesh.receiveShadow = true;
            leftElytronHinge.add(leftElytronMesh);
            beetleGroup.add(leftElytronHinge);

            // 6. SYMMETRICAL HORIZONTAL TRANSLUCENT AMBER HINDWINGS (對稱水平飛行後翅)
            const rightHindGeo = buildRightHindwingGeometry();
            const leftHindGeo = mirrorGeometryX(rightHindGeo);

            rightHindwingHinge = new THREE.Group();
            rightHindwingHinge.position.set(0.14, 0.28, 0.14);
            rightHindwingHinge.scale.set(0.01, 0.01, 0.01);
            const rightHindMesh = new THREE.Mesh(rightHindGeo, hindwingMaterial);
            rightHindwingHinge.add(rightHindMesh);
            beetleGroup.add(rightHindwingHinge);

            leftHindwingHinge = new THREE.Group();
            leftHindwingHinge.position.set(-0.14, 0.28, 0.14);
            leftHindwingHinge.scale.set(0.01, 0.01, 0.01);
            const leftHindMesh = new THREE.Mesh(leftHindGeo, hindwingMaterial);
            leftHindwingHinge.add(leftHindMesh);
            beetleGroup.add(leftHindwingHinge);

            // 7. 6 HYPER-DETAILED ANATOMICAL LEGS (基節、腿節、鋸齒脛節、五節跗節與雙爪)
            legsGroup = new THREE.Group();
            const legConfigs = [
                // Front pair (Prothoracic legs)
                { side: -1, z0: -0.48, knee: [-0.95, -0.06, -0.95], foot: [-1.35, -0.34, -1.48] },
                { side: 1,  z0: -0.48, knee: [0.95, -0.06, -0.95],  foot: [1.35, -0.34, -1.48] },
                // Middle pair (Mesothoracic legs)
                { side: -1, z0: 0.12,  knee: [-1.05, -0.08, 0.18],  foot: [-1.52, -0.36, 0.42] },
                { side: 1,  z0: 0.12,  knee: [1.05, -0.08, 0.18],   foot: [1.52, -0.36, 0.42] },
                // Hind pair (Metathoracic legs)
                { side: -1, z0: 0.65,  knee: [-1.02, -0.08, 1.25],  foot: [-1.42, -0.36, 1.95] },
                { side: 1,  z0: 0.65,  knee: [1.02, -0.08, 1.25],   foot: [1.42, -0.36, 1.95] }
            ];

            legConfigs.forEach(cfg => {
                const singleLeg = new THREE.Group();
                const hip = new THREE.Vector3(cfg.side * 0.42, -0.10, cfg.z0);
                const knee = new THREE.Vector3(...cfg.knee);
                const foot = new THREE.Vector3(...cfg.foot);

                // Coxa & Trochanter socket (基節與轉節)
                const coxa = new THREE.Mesh(new THREE.SphereGeometry(0.10, 12, 12), blackChitinMaterial);
                coxa.position.copy(hip);
                singleLeg.add(coxa);

                // Femur (粗壯腿節)
                const femurCurve = new THREE.LineCurve3(hip, knee);
                const femur = new THREE.Mesh(new THREE.TubeGeometry(femurCurve, 8, 0.072, 10, false), blackChitinMaterial);
                femur.castShadow = true;
                singleLeg.add(femur);

                // Knee Joint Condyle (膝關節)
                const kneeJoint = new THREE.Mesh(new THREE.SphereGeometry(0.068, 10, 10), blackChitinMaterial);
                kneeJoint.position.copy(knee);
                singleLeg.add(kneeJoint);

                // Tibia (脛節)
                const tibiaCurve = new THREE.LineCurve3(knee, foot);
                const tibia = new THREE.Mesh(new THREE.TubeGeometry(tibiaCurve, 8, 0.050, 10, false), blackChitinMaterial);
                tibia.castShadow = true;
                singleLeg.add(tibia);

                // 3 Sharp Outer Tibial Teeth/Spines + Apical Spur (脛節外側三鋸齒與端距)
                for (let s = 1; s <= 3; s++) {
                    const st = s / 4;
                    const spPos = new THREE.Vector3().lerpVectors(knee, foot, st);
                    const spine = new THREE.Mesh(new THREE.ConeGeometry(0.026, 0.12, 8), blackChitinMaterial);
                    spine.position.copy(spPos);
                    spine.rotation.z = cfg.side * -Math.PI * 0.36;
                    singleLeg.add(spine);
                }

                // 5-Segment Bead-Like Tarsus (五節念珠狀跗節)
                const tarsusDir = new THREE.Vector3(cfg.side * 0.22, -0.06, cfg.z0 < 0 ? -0.26 : 0.28);
                for (let seg = 1; seg <= 5; seg++) {
                    const tFrac = seg / 5;
                    const segPos = foot.clone().addScaledVector(tarsusDir, tFrac);
                    const tarsomere = new THREE.Mesh(
                        new THREE.ConeGeometry(0.026, 0.068, 8),
                        blackChitinMaterial
                    );
                    tarsomere.position.copy(segPos);
                    tarsomere.rotation.set(cfg.z0 < 0 ? -0.6 : 0.6, 0, cfg.side * -0.5);
                    singleLeg.add(tarsomere);
                }

                // Paired Curved Claws (末端雙爪)
                const clawBase = foot.clone().add(tarsusDir);
                [-0.025, 0.025].forEach(cOffset => {
                    const clawCurve = new THREE.CatmullRomCurve3([
                        clawBase.clone().add(new THREE.Vector3(0, 0, cOffset)),
                        clawBase.clone().add(new THREE.Vector3(cfg.side * 0.08, -0.04, cOffset * 1.4)),
                        clawBase.clone().add(new THREE.Vector3(cfg.side * 0.13, -0.11, cOffset * 1.6))
                    ]);
                    const claw = new THREE.Mesh(new THREE.TubeGeometry(clawCurve, 8, 0.012, 6, false), blackChitinMaterial);
                    singleLeg.add(claw);
                });

                legsGroup.add(singleLeg);
            });
            beetleGroup.add(legsGroup);

            // Natural horizontal living posture (no specimen box!)
            beetleGroup.position.set(0, 0.35, 0.15);
            beetleGroup.rotation.set(0.04, 0.38, 0);
            beetleGroup.scale.set(0.95, 0.95, 0.95);
            scene.add(beetleGroup);
        }

        /* =====================================================================
           6. SUBTLE ATMOSPHERIC MOSS & BARK DISPLAY STAGE (NO SPECIMEN BOX!)
        ===================================================================== */
        function createDisplayPedestal() {
            environmentPedestal = new THREE.Group();

            // Subtle floating moss-bark stage disk (auto-hides in Camera AR mode)
            const diskGeo = new THREE.CylinderGeometry(2.65, 2.85, 0.14, 48);
            const diskMat = new THREE.MeshStandardMaterial({
                color: 0x161b18,
                roughness: 0.88,
                metalness: 0.12
            });
            const disk = new THREE.Mesh(diskGeo, diskMat);
            disk.position.y = -0.08;
            disk.receiveShadow = true;
            environmentPedestal.add(disk);

            // Delicate golden museum accent ring around pedestal edge
            const ringGeo = new THREE.RingGeometry(2.62, 2.66, 64);
            const ringMat = new THREE.MeshBasicMaterial({
                color: 0xd97706,
                side: THREE.DoubleSide,
                transparent: true,
                opacity: 0.35
            });
            const goldRing = new THREE.Mesh(ringGeo, ringMat);
            goldRing.rotation.x = -Math.PI / 2;
            goldRing.position.y = -0.005;
            environmentPedestal.add(goldRing);

            scene.add(environmentPedestal);
        }

        /* =====================================================================
           7. BUILD DETAILED STAGE 1 (SCARAB LARVA) & STAGE 2 (HORNED PUPA)
        ===================================================================== */
        function createBeetleLarvaModel() {
            larvaGroup = new THREE.Group();

            // Organic Forest Humus Mound (腐植土堆)
            const soilGeo = new THREE.CylinderGeometry(1.75, 2.05, 0.28, 32);
            const soilMat = new THREE.MeshStandardMaterial({
                color: 0x261a10,
                roughness: 0.96
            });
            const soilMound = new THREE.Mesh(soilGeo, soilMat);
            soilMound.position.set(0, 0.12, 0.1);
            soilMound.receiveShadow = true;
            larvaGroup.add(soilMound);

            // Pearly Oval Beetle Egg
            const egg = new THREE.Mesh(
                new THREE.SphereGeometry(0.12, 18, 18),
                new THREE.MeshPhysicalMaterial({ color: 0xfefce8, roughness: 0.18, clearcoat: 0.88 })
            );
            egg.scale.set(0.85, 0.85, 1.25);
            egg.position.set(-0.95, 0.32, 0.65);
            larvaGroup.add(egg);

            // Iconic C-Shaped Ivory-White Scarab Larva (三齡蠐螬 — 含背褶、氣門點與三對胸足)
            const cCurve = new THREE.CatmullRomCurve3([
                new THREE.Vector3(-0.48, 0.42, -0.55), // Head
                new THREE.Vector3(0.35, 0.46, -0.68),
                new THREE.Vector3(0.82, 0.48, -0.05),
                new THREE.Vector3(0.55, 0.46, 0.65),
                new THREE.Vector3(-0.28, 0.42, 0.78)   // Dark posterior raster
            ]);

            const segCount = 15;
            for (let i = 0; i < segCount; i++) {
                const t = i / (segCount - 1);
                const pt = cCurve.getPointAt(t);
                const radius = 0.18 + Math.sin(t * Math.PI) * 0.15;
                const segColor = t > 0.76 ? 0x64748b : 0xfefce8;
                const segMat = new THREE.MeshPhysicalMaterial({
                    color: segColor,
                    roughness: 0.26,
                    clearcoat: 0.48
                });
                const seg = new THREE.Mesh(new THREE.SphereGeometry(radius, 20, 20), segMat);
                seg.position.copy(pt);
                seg.castShadow = true;
                seg.userData.segIndex = i;
                seg.userData.basePos = pt.clone();
                larvaGroup.add(seg);

                // Lateral Spiracle Dots (體側氣門點)
                if (i >= 1 && i <= 10) {
                    const spiracle = new THREE.Mesh(
                        new THREE.SphereGeometry(0.022, 8, 8),
                        new THREE.MeshStandardMaterial({ color: 0x9a3412 })
                    );
                    spiracle.position.copy(pt).add(new THREE.Vector3(0, 0.08, radius * 0.88));
                    larvaGroup.add(spiracle);
                }

                // 3 Pairs of Jointed Larval Thoracic Legs (三對黃褐色幼蟲胸足)
                if (i >= 1 && i <= 3) {
                    const leg = new THREE.Mesh(
                        new THREE.ConeGeometry(0.032, 0.24, 8),
                        new THREE.MeshStandardMaterial({ color: 0xb45309, roughness: 0.4 })
                    );
                    leg.position.copy(pt).add(new THREE.Vector3(-0.14, -0.12, 0.06));
                    leg.rotation.set(0.4, 0, 0.75);
                    larvaGroup.add(leg);
                }
            }

            // Amber-Brown Sclerotized Larval Head Capsule & Dark Chewing Mandibles (頭殼與大顎)
            const headPos = cCurve.getPointAt(0);
            const larvaHead = new THREE.Mesh(
                new THREE.SphereGeometry(0.17, 18, 18),
                new THREE.MeshStandardMaterial({ color: 0x9a3412, roughness: 0.32 })
            );
            larvaHead.position.copy(headPos).add(new THREE.Vector3(-0.12, -0.04, 0.05));
            larvaGroup.add(larvaHead);

            [-0.05, 0.05].forEach(mz => {
                const mandible = new THREE.Mesh(
                    new THREE.ConeGeometry(0.03, 0.12, 8),
                    new THREE.MeshStandardMaterial({ color: 0x1c1917 })
                );
                mandible.position.copy(headPos).add(new THREE.Vector3(-0.24, -0.06, 0.05 + mz));
                mandible.rotation.z = Math.PI / 2;
                larvaGroup.add(mandible);
            });

            larvaGroup.visible = false;
            scene.add(larvaGroup);
        }

        function createBeetlePupaModel() {
            pupaGroup = new THREE.Group();

            // Cutaway Earthen Pupal Chamber Wall (橢圓土繭蛹室剖面)
            const cellRim = new THREE.Mesh(
                new THREE.TorusGeometry(1.55, 0.24, 16, 40),
                new THREE.MeshStandardMaterial({ color: 0x3b2614, roughness: 0.95 })
            );
            cellRim.rotation.x = Math.PI / 2;
            cellRim.scale.set(0.85, 1.25, 0.65);
            cellRim.position.set(0, 0.12, 0.15);
            pupaGroup.add(cellRim);

            pupaShellMat = new THREE.MeshPhysicalMaterial({
                color: 0xd97706,
                roughness: 0.24,
                metalness: 0.12,
                clearcoat: 0.78,
                transparent: true,
                opacity: 0.96
            });

            // Pupa Abdomen & Thorax
            const pupaBody = new THREE.Mesh(new THREE.SphereGeometry(1, 28, 24), pupaShellMat);
            pupaBody.scale.set(0.62, 0.48, 1.05);
            pupaBody.position.set(0, 0.45, 0.45);
            pupaBody.castShadow = true;
            pupaGroup.add(pupaBody);

            // Folded Pupal Wing Pads & Legs (折疊翅芽與六足雛形)
            [-0.56, 0.56].forEach(wx => {
                const wingPad = new THREE.Mesh(new THREE.SphereGeometry(0.45, 16, 16), pupaShellMat);
                wingPad.scale.set(0.32, 0.55, 1.35);
                wingPad.position.set(wx, 0.36, 0.42);
                pupaGroup.add(wingPad);
            });

            // Developing Thoracic Horn Sheath extending forward
            const pupaHornCurve = new THREE.CatmullRomCurve3([
                new THREE.Vector3(0, 0.64, -0.25),
                new THREE.Vector3(0, 0.76, -0.95),
                new THREE.Vector3(0, 0.66, -1.58)
            ]);
            const pupaThoracicHorn = new THREE.Mesh(
                new THREE.TubeGeometry(pupaHornCurve, 20, 0.12, 12, false),
                pupaShellMat
            );
            pupaGroup.add(pupaThoracicHorn);

            // Developing Head Horn Sheath
            const pupaHeadHornCurve = new THREE.CatmullRomCurve3([
                new THREE.Vector3(0, 0.36, -0.35),
                new THREE.Vector3(0, 0.42, -0.88),
                new THREE.Vector3(0, 0.54, -1.25)
            ]);
            const pupaHeadHorn = new THREE.Mesh(
                new THREE.TubeGeometry(pupaHeadHornCurve, 16, 0.072, 10, false),
                pupaShellMat
            );
            pupaGroup.add(pupaHeadHorn);

            pupaGroup.visible = false;
            scene.add(pupaGroup);
        }

        /* =====================================================================
           8. MAGICAL POLLEN/MIST PARTICLES & INTERACTIVE TAP BEACON
        ===================================================================== */
        function createParticlesAndBeacon() {
            const count = 150;
            const geo = new THREE.BufferGeometry();
            const positions = new Float32Array(count * 3);
            for (let i = 0; i < count * 3; i += 3) {
                positions[i] = (Math.random() - 0.5) * 5.5;
                positions[i + 1] = (Math.random() - 0.5) * 4.5;
                positions[i + 2] = Math.random() * 4.0;
            }
            geo.setAttribute('position', new THREE.BufferAttribute(positions, 3));

            const mat = new THREE.PointsMaterial({
                color: 0xfacc15,
                size: 0.06,
                transparent: true,
                opacity: 0.8,
                blending: THREE.AdditiveBlending
            });
            particleSystem = new THREE.Points(geo, mat);
            particleSystem.visible = false;
            scene.add(particleSystem);

            const beaconGeo = new THREE.RingGeometry(0.12, 0.18, 24);
            const beaconMat = new THREE.MeshBasicMaterial({
                color: 0xfacc15,
                side: THREE.DoubleSide,
                transparent: true,
                opacity: 0
            });
            targetBeacon = new THREE.Mesh(beaconGeo, beaconMat);
            scene.add(targetBeacon);
        }

        /* =====================================================================
           9. CONTINUOUS 3D METAMORPHOSIS & HUMIDITY COLOR SHIFT CONTROLLERS
        ===================================================================== */
        function updateElytraTexture() {
            if (!elytraMaterial) return;
            const pbr = generateElytraPBRTextures(currentSubspecies, humidityLevel);
            elytraMaterial.map = pbr.map;
            elytraMaterial.normalMap = pbr.normalMap;
            elytraMaterial.roughnessMap = pbr.roughnessMap;
            elytraMaterial.needsUpdate = true;
        }

        function updateMetamorphosisProgress(val) {
            metamorphosisProgress = val;
            document.getElementById('slider-metamorphosis').value = val;
            document.getElementById('val-progress').innerText = `${Math.round(val)}%`;

            const lbl = document.getElementById('lbl-stage-name');
            [1, 2, 3, 4].forEach(i => document.getElementById(`btn-stage-${i}`).classList.remove('active'));

            if (val < 30) {
                // STAGE 1: Egg & Scarab Larva (蠐螬幼蟲)
                document.getElementById('btn-stage-1').classList.add('active');
                lbl.innerText = `1. 卵與幼蟲 (${Math.round(val)}%)`;

                larvaGroup.visible = true;
                pupaGroup.visible = false;
                beetleGroup.visible = false;
                if (isFlyOut) resetFlyOutState();

            } else if (val < 65) {
                // STAGE 2: Pupal Chamber & Horned Pupa (蛹室化蛹)
                document.getElementById('btn-stage-2').classList.add('active');
                lbl.innerText = `2. 蛹室化蛹 (${Math.round(val)}%)`;

                larvaGroup.visible = false;
                pupaGroup.visible = true;
                beetleGroup.visible = false;

                const subT = (val - 30) / 35;
                pupaShellMat.opacity = 0.96 - subT * 0.45;
                if (isFlyOut) resetFlyOutState();

            } else if (val < 88) {
                // STAGE 3: Emergence (破蛹羽化)
                document.getElementById('btn-stage-3').classList.add('active');
                lbl.innerText = `3. 破蛹羽化 (${Math.round(val)}%)`;

                larvaGroup.visible = false;
                pupaGroup.visible = true;
                pupaShellMat.opacity = 0.28;
                beetleGroup.visible = true;

                const subT = (val - 65) / 23;
                const sc = 0.55 + subT * 0.40;
                beetleGroup.scale.set(sc, sc, sc);
                beetleGroup.position.set(0, 0.35, 0.15);
                beetleGroup.rotation.set(0.04, 0.38, 0);

            } else {
                // STAGE 4: Full Adult Hercules Beetle
                document.getElementById('btn-stage-4').classList.add('active');
                lbl.innerText = isFlyOut ? `4. 展翅飛舞 (${Math.round(val)}%)` : `4. 成蟲活體 (${Math.round(val)}%)`;

                larvaGroup.visible = false;
                pupaGroup.visible = false;
                beetleGroup.visible = true;
                beetleGroup.scale.set(0.95, 0.95, 0.95);

                if (!isFlyOut) {
                    beetleGroup.position.set(0, 0.35, 0.15);
                    beetleGroup.rotation.set(0.04, 0.38, 0);
                }
            }
        }

        function animateToStage(stageNum) {
            const targets = { 1: 15, 2: 48, 3: 78, 4: 100 };
            const proxy = { val: metamorphosisProgress };
            gsap.to(proxy, {
                val: targets[stageNum],
                duration: 0.85,
                ease: 'power2.inOut',
                onUpdate: () => updateMetamorphosisProgress(proxy.val)
            });
        }

        /* =====================================================================
           10. "TAKE FLIGHT" & "EXPLODED ANATOMY" HERO INTERACTIONS
        ===================================================================== */
        function resetFlyOutState() {
            isFlyOut = false;
            particleSystem.visible = false;
            document.getElementById('txt-fly-out').innerText = '展翅起飛！';
            document.getElementById('icon-fly-out').className = 'ph-fill ph-sparkle text-base text-amber-300';

            gsap.to(leftElytronHinge.rotation, { x: 0, y: 0, z: 0, duration: 0.85, ease: 'power2.inOut' });
            gsap.to(rightElytronHinge.rotation, { x: 0, y: 0, z: 0, duration: 0.85, ease: 'power2.inOut' });

            gsap.to(leftHindwingHinge.scale, { x: 0.01, y: 0.01, z: 0.01, duration: 0.65 });
            gsap.to(rightHindwingHinge.scale, { x: 0.01, y: 0.01, z: 0.01, duration: 0.65 });
        }

        function triggerFlyOut() {
            if (isExploded) toggleExplodedAnatomy();

            if (!isFlyOut) {
                isFlyOut = true;
                playSound('flyout');
                updateMetamorphosisProgress(100);

                document.getElementById('txt-fly-out').innerText = '降落休憩';
                document.getElementById('icon-fly-out').className = 'ph-bold ph-arrows-in text-base text-amber-200';
                document.getElementById('lbl-stage-name').innerText = '4. 展翅飛舞 (AR Live)';

                particleSystem.visible = true;
                flightTargetOffset.set(0, 1.15, 0.35);

                // 1. Open Left & Right Elytra symmetrically & unfold translucent Amber Hindwings
                gsap.to(leftElytronHinge.rotation, {
                    x: -0.42,
                    y: -0.58,
                    z: -0.28,
                    duration: 0.95,
                    ease: 'back.out(1.4)'
                });
                gsap.to(rightElytronHinge.rotation, {
                    x: -0.42,
                    y: 0.58,
                    z: 0.28,
                    duration: 0.95,
                    ease: 'back.out(1.4)'
                });

                gsap.to(leftHindwingHinge.scale, { x: 1, y: 1, z: 1, duration: 0.85, ease: 'power2.out' });
                gsap.to(rightHindwingHinge.scale, { x: 1, y: 1, z: 1, duration: 0.85, ease: 'power2.out' });

                // 2. Hercules Beetle lifts off into dynamic aerial flight posture
                gsap.to(beetleGroup.position, {
                    x: 0,
                    y: 1.15,
                    z: 0.35,
                    duration: 1.35,
                    ease: 'back.out(1.25)'
                });
                gsap.to(beetleGroup.rotation, {
                    x: 0.28,
                    y: 0.38,
                    z: 0,
                    duration: 1.25,
                    ease: 'power2.out'
                });

                showToast('赫克力士長戟大兜蟲已張開鞘翅展翅起飛！點擊畫面可引導飛行');
            } else {
                playSound('click');
                resetFlyOutState();
                document.getElementById('lbl-stage-name').innerText = '4. 成蟲活體 (100%)';

                gsap.to(beetleGroup.position, {
                    x: 0,
                    y: 0.35,
                    z: 0.15,
                    duration: 1.1,
                    ease: 'power2.inOut'
                });
                gsap.to(beetleGroup.rotation, {
                    x: 0.04,
                    y: 0.38,
                    z: 0,
                    duration: 1.1,
                    ease: 'power2.inOut'
                });
            }
        }

        function toggleExplodedAnatomy() {
            if (isFlyOut) resetFlyOutState();
            updateMetamorphosisProgress(100);

            isExploded = !isExploded;
            playSound('click');
            document.getElementById('btn-explode').classList.toggle('active', isExploded);

            if (isExploded) {
                // Separate anatomical components cleanly in 3D space
                gsap.to(thoracicHornGroup.position, { y: 0.45, z: -0.55, duration: 0.85, ease: 'power2.out' });
                gsap.to(pronotumGroup.position, { y: 0.42, z: -0.25, duration: 0.85, ease: 'power2.out' });
                gsap.to(headHornGroup.position, { y: -0.22, z: -1.18, duration: 0.85, ease: 'power2.out' });
                gsap.to(leftElytronHinge.position, { x: -0.68, y: 0.88, z: 0.25, duration: 0.85, ease: 'power2.out' });
                gsap.to(rightElytronHinge.position, { x: 0.68, y: 0.88, z: 0.25, duration: 0.85, ease: 'power2.out' });

                gsap.to(leftHindwingHinge.scale, { x: 0.9, y: 0.9, z: 0.9, duration: 0.75 });
                gsap.to(rightHindwingHinge.scale, { x: 0.9, y: 0.9, z: 0.9, duration: 0.75 });
                gsap.to(leftHindwingHinge.position, { x: -0.55, y: 0.55, z: 0.35, duration: 0.85 });
                gsap.to(rightHindwingHinge.position, { x: 0.55, y: 0.55, z: 0.35, duration: 0.85 });

                gsap.to(abdomenGroup.position, { y: -0.28, z: 0.35, duration: 0.85, ease: 'power2.out' });
                gsap.to(legsGroup.position, { y: -0.55, duration: 0.85, ease: 'power2.out' });

                showToast('已開啟 3D 解剖結構拆解視圖，可旋轉縮放觀察內部構造');
            } else {
                // Reassemble back into intact specimen
                gsap.to(thoracicHornGroup.position, { y: 0, z: 0, duration: 0.8, ease: 'power2.inOut' });
                gsap.to(pronotumGroup.position, { y: 0, z: 0, duration: 0.8, ease: 'power2.inOut' });
                gsap.to(headHornGroup.position, { y: 0.04, z: -0.82, duration: 0.8, ease: 'power2.inOut' });
                gsap.to(leftElytronHinge.position, { x: -0.004, y: 0.36, z: 0.02, duration: 0.8, ease: 'power2.inOut' });
                gsap.to(rightElytronHinge.position, { x: 0.004, y: 0.36, z: 0.02, duration: 0.8, ease: 'power2.inOut' });

                gsap.to(leftHindwingHinge.scale, { x: 0.01, y: 0.01, z: 0.01, duration: 0.6 });
                gsap.to(rightHindwingHinge.scale, { x: 0.01, y: 0.01, z: 0.01, duration: 0.6 });
                gsap.to(leftHindwingHinge.position, { x: -0.14, y: 0.28, z: 0.14, duration: 0.8 });
                gsap.to(rightHindwingHinge.position, { x: 0.14, y: 0.28, z: 0.14, duration: 0.8 });

                gsap.to(abdomenGroup.position, { y: 0, z: 0, duration: 0.8, ease: 'power2.inOut' });
                gsap.to(legsGroup.position, { y: 0, duration: 0.8, ease: 'power2.inOut' });
            }
        }

        /* =====================================================================
           11. SUBSPECIES SWITCHER, QR CODE GENERATOR & AR CAMERA
        ===================================================================== */
        function switchSubspecies(key) {
            currentSubspecies = key;
            ['ecuatorianus', 'hercules', 'lichyi'].forEach(k => {
                document.getElementById(`species-${k}`).classList.remove('active');
            });
            document.getElementById(`species-${key}`).classList.add('active');

            updateElytraTexture();

            const info = subspeciesCatalog[key];
            showToast(`已切換亞種型態：${info.zhName} (${info.latinName})`);
        }

        function drawProceduralQRCode() {
            const canvas = document.getElementById('qr-canvas');
            const ctx = canvas.getContext('2d');
            const size = 168;
            const cells = 21;
            const cellSize = size / cells;

            ctx.fillStyle = '#ffffff';
            ctx.fillRect(0, 0, size, size);
            ctx.fillStyle = '#0f172a';

            let seed = 9318842;
            const rand = () => {
                seed = (seed * 1664525 + 1013904223) % 4294967296;
                return seed / 4294967296;
            };

            const isFinder = (r, c) => {
                return (r < 7 && c < 7) || (r < 7 && c >= cells - 7) || (r >= cells - 7 && c < 7);
            };

            for (let r = 0; r < cells; r++) {
                for (let c = 0; c < cells; c++) {
                    if (isFinder(r, c)) continue;
                    if (rand() > 0.48) {
                        ctx.fillRect(c * cellSize, r * cellSize, cellSize - 0.5, cellSize - 0.5);
                    }
                }
            }

            const drawFinder = (ox, oy) => {
                ctx.fillStyle = '#0f172a';
                ctx.fillRect(ox * cellSize, oy * cellSize, 7 * cellSize, 7 * cellSize);
                ctx.fillStyle = '#ffffff';
                ctx.fillRect((ox + 1) * cellSize, (oy + 1) * cellSize, 5 * cellSize, 5 * cellSize);
                ctx.fillStyle = '#b45309';
                ctx.fillRect((ox + 2) * cellSize, (oy + 2) * cellSize, 3 * cellSize, 3 * cellSize);
            };
            drawFinder(0, 0);
            drawFinder(cells - 7, 0);
            drawFinder(0, cells - 7);
        }

        async function toggleCameraAR() {
            const video = document.getElementById('ar-camera-feed');
            const badge = document.getElementById('badge-mode');
            const txt = document.getElementById('txt-camera-mode');
            const overlay = document.getElementById('ar-scanner-overlay');

            if (!isCameraAR) {
                try {
                    if (!navigator.mediaDevices || !navigator.mediaDevices.getUserMedia) {
                        throw new Error('Camera API unavailable');
                    }
                    videoStream = await navigator.mediaDevices.getUserMedia({
                        video: { facingMode: { ideal: 'environment' } },
                        audio: false
                    });
                    video.srcObject = videoStream;
                    await video.play();
                    video.classList.remove('hidden');

                    isCameraAR = true;
                    scene.background = null;
                    renderer.setClearColor(0x000000, 0);
                    if (environmentPedestal) environmentPedestal.visible = false;

                    badge.innerText = '實景相機 AR 啟動中';
                    txt.innerText = '關閉相機 AR';
                    document.getElementById('btn-toggle-camera').classList.add('active');
                    overlay.classList.remove('opacity-0');

                    showToast('已啟動 WebAR 相機！將鏡頭對準桌面即可讓大兜蟲降落或飛舞', 'ph-fill ph-camera text-cyan-400');
                } catch (err) {
                    showToast('目前裝置未授權或無後置鏡頭，維持 3D 微距展廳模式', 'ph-fill ph-info text-amber-400');
                }
            } else {
                if (videoStream) {
                    videoStream.getTracks().forEach(t => t.stop());
                    videoStream = null;
                }
                video.classList.add('hidden');
                isCameraAR = false;
                scene.background = new THREE.Color(0x070b12);
                renderer.setClearColor(0x070b12, 1);
                if (environmentPedestal) environmentPedestal.visible = true;

                badge.innerText = '3D 微距展廳';
                txt.innerText = '實景相機 AR';
                document.getElementById('btn-toggle-camera').classList.remove('active');
                overlay.classList.add('opacity-0');

                showToast('已返回 3D 微距展廳模式');
            }
        }

        function takeARSnapshot() {
            playSound('shutter');
            renderer.render(scene, camera);

            const outCanvas = document.createElement('canvas');
            const w = renderer.domElement.width;
            const h = renderer.domElement.height;
            outCanvas.width = w;
            outCanvas.height = h;
            const ctx = outCanvas.getContext('2d');

            const video = document.getElementById('ar-camera-feed');
            if (isCameraAR && video.readyState >= 2) {
                ctx.drawImage(video, 0, 0, w, h);
            } else {
                ctx.fillStyle = '#070b12';
                ctx.fillRect(0, 0, w, h);
            }

            ctx.drawImage(renderer.domElement, 0, 0, w, h);

            const info = subspeciesCatalog[currentSubspecies];
            ctx.fillStyle = 'rgba(10, 15, 24, 0.80)';
            ctx.fillRect(24, h - 92, 460, 68);
            ctx.strokeStyle = '#facc15';
            ctx.lineWidth = 2;
            ctx.strokeRect(24, h - 92, 460, 68);

            ctx.fillStyle = '#fef08a';
            ctx.font = 'bold 21px sans-serif';
            ctx.fillText(`WebAR 標本互動 • ${info.zhName}`, 42, h - 60);
            ctx.fillStyle = '#cbd5e1';
            ctx.font = 'italic 16px serif';
            ctx.fillText(`${info.latinName} | Museum Interactive AR`, 42, h - 36);

            const link = document.createElement('a');
            link.download = `WebAR-Dynastes-Hercules-${Date.now()}.png`;
            link.href = outCanvas.toDataURL('image/png');
            link.click();

            showToast('已為您儲存高清大兜蟲 AR 紀念照！', 'ph-fill ph-check-circle text-emerald-400');
        }

        /* =====================================================================
           12. 3D CALLOUT MARKERS & RAYCAST TAP INTERACTION
        ===================================================================== */
        function initCalloutMarkers() {
            const container = document.getElementById('markers-container');
            container.innerHTML = '';
            markerDOMList = [];

            calloutHotspots.forEach(item => {
                const btn = document.createElement('button');
                btn.className = 'ar-marker pointer-events-auto absolute px-2.5 py-1 rounded-full text-[11px] font-medium text-amber-200 flex items-center space-x-1';
                btn.innerHTML = `<span class="w-1.5 h-1.5 rounded-full bg-amber-400 animate-ping mr-1"></span><span>${item.label}</span>`;

                btn.addEventListener('click', (e) => {
                    e.stopPropagation();
                    playSound('click');
                    markerDOMList.forEach(m => m.el.classList.remove('selected'));
                    btn.classList.add('selected');

                    document.getElementById('info-title').innerText = item.title;
                    document.getElementById('info-desc').innerText = item.desc;
                    const card = document.getElementById('info-card');
                    card.classList.remove('opacity-0', 'translate-y-4', 'pointer-events-none');
                });

                container.appendChild(btn);
                markerDOMList.push({ el: btn, data: item });
            });
        }

        function updateCalloutMarkers() {
            const worldPos = new THREE.Vector3();

            markerDOMList.forEach(({ el, data }) => {
                if (!showLabels) {
                    el.style.opacity = '0';
                    el.style.pointerEvents = 'none';
                    return;
                }

                let visibleForStage = false;
                if (data.stageReq === 'larva' && metamorphosisProgress < 30) visibleForStage = true;
                else if (data.stageReq === 'pupa' && metamorphosisProgress >= 30 && metamorphosisProgress < 65) visibleForStage = true;
                else if (data.stageReq === 'adult' && metamorphosisProgress >= 75) visibleForStage = true;
                else if (data.stageReq === 'flying' && (isFlyOut || isExploded)) visibleForStage = true;

                if (!visibleForStage) {
                    el.style.opacity = '0';
                    el.style.pointerEvents = 'none';
                    return;
                }

                worldPos.copy(data.localPos);
                if ((data.stageReq === 'adult' || data.stageReq === 'flying') && beetleGroup) {
                    beetleGroup.localToWorld(worldPos);
                }

                worldPos.project(camera);
                const x = (worldPos.x * 0.5 + 0.5) * window.innerWidth;
                const y = (-(worldPos.y * 0.5) + 0.5) * window.innerHeight;

                if (worldPos.z < 1.0 && x > 20 && x < window.innerWidth - 20 && y > 60 && y < window.innerHeight - 60) {
                    el.style.left = `${x}px`;
                    el.style.top = `${y}px`;
                    el.style.opacity = '1';
                    el.style.pointerEvents = 'auto';
                } else {
                    el.style.opacity = '0';
                    el.style.pointerEvents = 'none';
                }
            });
        }

        /* =====================================================================
           13. SCENE INITIALIZATION & EVENT LISTENERS
        ===================================================================== */
        function initScene() {
            scene = new THREE.Scene();
            scene.background = new THREE.Color(0x070b12);

            camera = new THREE.PerspectiveCamera(45, window.innerWidth / window.innerHeight, 0.1, 100);
            camera.position.set(3.4, 2.35, 4.65);

            renderer = new THREE.WebGLRenderer({
                antialias: true,
                alpha: true,
                preserveDrawingBuffer: true,
                powerPreference: 'high-performance'
            });
            renderer.setSize(window.innerWidth, window.innerHeight);
            renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
            renderer.shadowMap.enabled = true;
            renderer.shadowMap.type = THREE.PCFSoftShadowMap;
            renderer.toneMapping = THREE.ACESFilmicToneMapping;
            renderer.toneMappingExposure = 1.24;
            document.getElementById('webgl-container').appendChild(renderer.domElement);

            controls = new THREE.OrbitControls(camera, renderer.domElement);
            controls.enableDamping = true;
            controls.dampingFactor = 0.06;
            controls.minDistance = 2.0;
            controls.maxDistance = 14;
            controls.target.set(0, 0.35, 0);

            // Museum Studio Key, Rim & Fill Lighting
            const ambientLight = new THREE.AmbientLight(0xffffff, 0.85);
            scene.add(ambientLight);

            const keyLight = new THREE.DirectionalLight(0xfffbeb, 1.85);
            keyLight.position.set(4, 7, 5);
            keyLight.castShadow = true;
            keyLight.shadow.mapSize.set(1024, 1024);
            scene.add(keyLight);

            const rimLight = new THREE.DirectionalLight(0x38bdf8, 0.75);
            rimLight.position.set(-5, 2, -4);
            scene.add(rimLight);

            clock = new THREE.Clock();

            // Build 3D Assets (No Specimen Box!)
            createDisplayPedestal();
            createHerculesBeetleModel();
            createBeetleLarvaModel();
            createBeetlePupaModel();
            createParticlesAndBeacon();

            initCalloutMarkers();
            drawProceduralQRCode();
            bindEvents();

            setTimeout(() => {
                const loader = document.getElementById('loader');
                loader.style.opacity = '0';
                setTimeout(() => { loader.style.display = 'none'; }, 500);
            }, 450);
        }

        function bindEvents() {
            window.addEventListener('resize', () => {
                camera.aspect = window.innerWidth / window.innerHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(window.innerWidth, window.innerHeight);
            });

            // Tap on 3D Canvas to guide beetle when flying out
            const raycaster = new THREE.Raycaster();
            const pointerNDC = new THREE.Vector2();
            const flightPlane = new THREE.Plane(new THREE.Vector3(0, 1, 0), -1.15);

            renderer.domElement.addEventListener('pointerdown', (e) => {
                if (!isFlyOut) return;
                pointerNDC.x = (e.clientX / window.innerWidth) * 2 - 1;
                pointerNDC.y = -(e.clientY / window.innerHeight) * 2 + 1;
                raycaster.setFromCamera(pointerNDC, camera);

                const hitPoint = new THREE.Vector3();
                if (raycaster.ray.intersectPlane(flightPlane, hitPoint)) {
                    hitPoint.x = THREE.MathUtils.clamp(hitPoint.x, -2.2, 2.2);
                    hitPoint.z = THREE.MathUtils.clamp(hitPoint.z, -2.2, 2.2);
                    hitPoint.y = 1.15;

                    flightTargetOffset.copy(hitPoint);

                    targetBeacon.position.copy(hitPoint);
                    targetBeacon.rotation.x = -Math.PI / 2;
                    targetBeacon.material.opacity = 0.9;
                    targetBeacon.scale.set(0.4, 0.4, 0.4);
                    gsap.to(targetBeacon.scale, { x: 2.2, y: 2.2, z: 2.2, duration: 0.7, ease: 'power2.out' });
                    gsap.to(targetBeacon.material, { opacity: 0, duration: 0.7 });
                }
            });

            document.getElementById('btn-fly-out').addEventListener('click', triggerFlyOut);
            document.getElementById('btn-explode').addEventListener('click', toggleExplodedAnatomy);

            document.getElementById('btn-auto-rotate').addEventListener('click', () => {
                playSound('click');
                controls.autoRotate = !controls.autoRotate;
                controls.autoRotateSpeed = 1.8;
                document.getElementById('btn-auto-rotate').classList.toggle('active', controls.autoRotate);
            });

            [1, 2, 3, 4].forEach(stage => {
                document.getElementById(`btn-stage-${stage}`).addEventListener('click', () => {
                    playSound('click');
                    animateToStage(stage);
                });
            });

            document.getElementById('slider-metamorphosis').addEventListener('input', (e) => {
                updateMetamorphosisProgress(parseFloat(e.target.value));
            });

            // Humidity Color Shift Slider
            document.getElementById('slider-humidity').addEventListener('input', (e) => {
                const rawVal = parseInt(e.target.value, 10);
                humidityLevel = rawVal / 100;
                let stateText = '乾燥金黃';
                if (rawVal >= 40 && rawVal < 75) stateText = '橄欖條紋';
                else if (rawVal >= 75) stateText = '潮濕黑褐';
                document.getElementById('val-humidity').innerText = `${rawVal}% ${stateText}`;
                updateElytraTexture();
            });

            // Subspecies Buttons
            ['ecuatorianus', 'hercules', 'lichyi'].forEach(sp => {
                document.getElementById(`species-${sp}`).addEventListener('click', () => {
                    playSound('click');
                    switchSubspecies(sp);
                });
            });

            document.getElementById('btn-toggle-camera').addEventListener('click', toggleCameraAR);
            document.getElementById('btn-snapshot').addEventListener('click', takeARSnapshot);

            document.getElementById('btn-open-qr').addEventListener('click', () => {
                playSound('click');
                document.getElementById('modal-qr').classList.remove('opacity-0', 'pointer-events-none');
            });
            document.getElementById('btn-close-qr').addEventListener('click', () => {
                playSound('click');
                document.getElementById('modal-qr').classList.add('opacity-0', 'pointer-events-none');
            });

            document.getElementById('btn-toggle-labels').addEventListener('click', () => {
                playSound('click');
                showLabels = !showLabels;
                document.getElementById('btn-toggle-labels').classList.toggle('active', showLabels);
            });

            document.getElementById('btn-toggle-audio').addEventListener('click', () => {
                isAudioOn = !isAudioOn;
                document.getElementById('icon-audio').className = isAudioOn
                    ? 'ph-light ph-speaker-high text-base'
                    : 'ph-light ph-speaker-slash text-base text-slate-500';
                if (isAudioOn) playSound('click');
            });

            document.getElementById('btn-reset-view').addEventListener('click', () => {
                playSound('click');
                gsap.to(camera.position, { x: 3.4, y: 2.35, z: 4.65, duration: 0.9, ease: 'power2.out' });
                gsap.to(controls.target, { x: 0, y: 0.35, z: 0, duration: 0.9, ease: 'power2.out' });
            });

            document.getElementById('btn-close-info').addEventListener('click', () => {
                const card = document.getElementById('info-card');
                card.classList.add('opacity-0', 'translate-y-4', 'pointer-events-none');
                markerDOMList.forEach(m => m.el.classList.remove('selected'));
            });
        }

        /* =====================================================================
           14. MAIN RENDER & BIOMECHANICAL ANIMATION LOOP
        ===================================================================== */
        function animate() {
            requestAnimationFrame(animate);
            const t = clock.getElapsedTime();

            // 1. Subtle Head Horn Clamping Motion (夾鉗微動)
            if (headHornGroup && metamorphosisProgress >= 75) {
                headHornGroup.rotation.x = Math.sin(t * 2.2) * 0.045;
            }

            // 2. Symmetrical Horizontal Hindwing Flapping during Flight
            if (isFlyOut && leftHindwingHinge && rightHindwingHinge) {
                const wingBeat = Math.sin(t * 24.0) * 0.62 + 0.12;
                leftHindwingHinge.rotation.z = -wingBeat;
                rightHindwingHinge.rotation.z = wingBeat;
            }

            // 3. Organic Aerial Hover & Banking when Beetle Leaps Out of Frame
            if (isFlyOut && beetleGroup) {
                const hoverX = Math.sin(t * 1.35) * 0.48 + Math.cos(t * 0.75) * 0.22;
                const hoverY = Math.sin(t * 2.2) * 0.24;
                const hoverZ = Math.cos(t * 1.15) * 0.22;

                const desiredX = flightTargetOffset.x + hoverX;
                const desiredY = flightTargetOffset.y + hoverY;
                const desiredZ = flightTargetOffset.z + hoverZ;

                beetleGroup.position.x += (desiredX - beetleGroup.position.x) * 0.035;
                beetleGroup.position.y += (desiredY - beetleGroup.position.y) * 0.035;
                beetleGroup.position.z += (desiredZ - beetleGroup.position.z) * 0.035;

                const vx = desiredX - beetleGroup.position.x;
                beetleGroup.rotation.y = 0.32 + Math.sin(t * 0.95) * 0.25 - vx * 0.55;
                beetleGroup.rotation.z = -vx * 0.7;
            }

            // 4. Stage 1 Scarab Larva Gentle Wriggle in Humus Soil
            if (metamorphosisProgress < 30 && larvaGroup) {
                larvaGroup.children.forEach(child => {
                    if (child.userData.segIndex !== undefined) {
                        const idx = child.userData.segIndex;
                        child.position.y = child.userData.basePos.y + Math.sin(t * 3.8 - idx * 0.5) * 0.025;
                    }
                });
            }

            // 5. Stage 2 Beetle Pupa Breathing Pulse
            if (metamorphosisProgress >= 30 && metamorphosisProgress < 88 && pupaGroup) {
                pupaGroup.rotation.y = Math.sin(t * 1.4) * 0.04;
                pupaGroup.rotation.z = Math.sin(t * 1.6) * 0.035;
            }

            // 6. Golden Mist Particles
            if (particleSystem && particleSystem.visible) {
                particleSystem.rotation.y = t * 0.14;
                particleSystem.position.y = Math.sin(t * 0.8) * 0.12;
            }

            controls.update();
            updateCalloutMarkers();
            renderer.render(scene, camera);
        }

        window.onload = function () {
            initScene();
            animate();
        };
    </script>
</body>
</html>
