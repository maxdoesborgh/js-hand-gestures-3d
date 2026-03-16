🖐️ 3D Hand Particle System (Prototype V1)
Dit prototype is onderdeel van het project The Attention Storm voor Night of the Nerds 2026. Het is een technisch experiment waarin we onderzoeken hoe we de traditionele interface (sliders) kunnen vervangen door intuïtieve handgebaren met behulp van AI en computer vision.

⚙️ Technische Features
Real-time AI Tracking: Maakt gebruik van de @mediapipe/tasks-vision Hand Landmarker voor ultra-lage latentie tracking via de GPU.

High-Density Particles: Rendert 15.000 deeltjes simultaan met Three.WebGLRenderer en BufferGeometry voor optimale performance.

Gesture Mapping: * Positie: Het systeem volgt de Middle Finger MCP (landmark 9) voor een stabiel middelpunt.

Expansion: De afstand tussen pols en vingertoppen bepaalt de spreiding ("bloom") van de deeltjes.

Tension: De spreiding tussen duim en pink bepaalt de schaal en de strakheid van de simulatie.

Organic Physics: Gebruikt een combinatie van sinus-orbitaalbewegingen en easing functies om een vloeibaar, natuurlijk gevoel te creëren.

🛠️ Stack
Core: Three.js (R160)

AI/ML: MediaPipe Hand Landmarker

Rendering: WebGL met Additive Blending voor een "glow" effect.

🚀 Hoe het werkt
AI Initialisatie: Bij het laden wordt het MediaPipe Wasm-bestand opgehaald voor snelle berekeningen.

Landmark Extractie: Elke frame analyseert de webcam de positie van 21 hand-coördinaten.

Vector Math: De ruwe data wordt omgezet naar Three.js Vector3 posities.

Particle Update: De posities van de 45.000 individuele punten (15k * 3 coördinaten) worden in de animate loop bijgewerkt via de posAttr.needsUpdate vlag.

🎮 Gebruik
Open hand: Deeltjes spreiden zich uit (creativiteit/rust).

Vuist: Deeltjes trekken samen tot een compacte vorm (focus/spanning).

Kleur: Gebruik de Color Picker in de UI om de sfeer van de storm real-time aan te passen.

🎓 Context
Dit prototype is ontwikkeld door Max Doesborgh als onderdeel van het Attention Arcade collectief. Het dient als bewijslast voor de leeruitkomst Interactive Media en Professional Standard binnen de opleiding Fontys ICT & Media Design.
