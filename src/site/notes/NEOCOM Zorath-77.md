---
{"dg-publish":true,"permalink":"/neocom-zorath-77/","tags":["gardenEntry"],"created":"2026-02-28T21:09:16.622+01:00"}
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&display=swap');

/* RESET ET FOND HOLOGRAPHIQUE */
body, .markdown-preview-view, .markdown-rendered { background-color: #010102 !important; font-family: 'Rajdhani', sans-serif !important; color: #b3b3b3 !important; }
.eve-window { background: rgba(8, 9, 12, 0.9); border: 1px solid #333; box-shadow: 0 15px 50px rgba(0,0,0,1), inset 0 0 40px rgba(0,0,0,0.8); max-width: 950px; margin: 0 auto; border-top: 3px solid #D4AF37; font-family: 'Rajdhani', sans-serif; position: relative; overflow: hidden; }

/* SCANLINES ET BRUIT CRT */
.eve-window::after { content: ""; position: absolute; top: 0; left: 0; right: 0; bottom: 0; background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), linear-gradient(90deg, rgba(255,0,0,0.03), rgba(0,255,255,0.02)); background-size: 100% 4px, 3px 100%; pointer-events: none; opacity: 0.6; z-index: 50; }

/* LAYOUT PRINCIPAL */
.eve-main-flex { display: flex; align-items: stretch; position: relative; z-index: 1; }

/* TERMINAL DE PIRATAGE ULTRA-RÉALISTE */
.eve-terminal-left { width: 190px; flex-shrink: 0; background: #000; border-right: 1px solid #222; position: relative; overflow: hidden; padding: 0; font-family: monospace; color: #7DF9FF; box-shadow: inset -10px 0 20px rgba(0,0,0,0.9); -webkit-mask-image: linear-gradient(to bottom, transparent 0%, black 10%, black 90%, transparent 100%); mask-image: linear-gradient(to bottom, transparent 0%, black 10%, black 90%, transparent 100%); }
.eve-terminal-scroll { position: absolute; top: 0; left: 15px; right: 10px; animation: scrollHack 15s linear infinite; }
.eve-terminal-scroll p { margin: 0; padding: 2px 0; font-size: 10px; line-height: 1.3; text-shadow: 0 0 6px rgba(125, 249, 255, 0.8); opacity: 0.85; letter-spacing: 0.5px; }

/* CONTENU DROIT */
.eve-content { flex: 1; padding: 40px; position: relative; min-width: 0; background: radial-gradient(circle at center, rgba(20,20,25,0.4) 0%, rgba(0,0,0,0.8) 100%); }

/* DATA STRIPS */
.eve-table { width: 100%; border-collapse: collapse; font-family: 'Rajdhani', sans-serif; margin-bottom: 20px; }
.eve-table tr { border-bottom: 1px solid rgba(212, 175, 55, 0.15); transition: all 0.2s ease-in-out; }
.eve-table tr:hover { background: linear-gradient(90deg, rgba(212, 175, 55, 0.1) 0%, transparent 100%); border-left: 2px solid #D4AF37; transform: translateX(3px); }
.eve-table td { padding: 12px 10px; }
.eve-table td:first-child { color: #888; width: 35%; text-transform: uppercase; font-size: 13px; letter-spacing: 1px; }
.eve-table td:last-child { color: #fff; font-weight: 500; font-size: 16px; word-break: break-word; }

/* LIENS ET BOUTONS INTERACTIFS */
.eve-btn { display: block; padding: 15px; border: 1px solid #333; text-align: center; text-decoration: none !important; transition: 0.3s; background: rgba(10,10,12,0.8); position: relative; overflow: hidden; }
.eve-btn::before { content: ""; position: absolute; top: 0; left: -100%; width: 50%; height: 100%; background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent); transform: skewX(-20deg); transition: 0.5s; }
.eve-btn:hover::before { left: 150%; }
.eve-btn-red { border-top: 2px solid #522; }
.eve-btn-red:hover { border-color: #ff4d4d; background: rgba(255, 77, 77, 0.1); box-shadow: 0 0 20px rgba(255, 77, 77, 0.2); }
.eve-btn-cyan { border-top: 2px solid #244; }
.eve-btn-cyan:hover { border-color: #7DF9FF; background: rgba(125, 249, 255, 0.1); box-shadow: 0 0 20px rgba(125, 249, 255, 0.2); }

.eve-row { padding: 10px 15px 10px 40px; display: flex; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.03); transition: all 0.2s; position: relative; flex-wrap: wrap; }
.eve-row::before { content: "►"; position: absolute; left: 15px; font-size: 10px; color: #444; transition: 0.2s; }
.eve-row:hover { background: rgba(125, 249, 255, 0.05); padding-left: 45px; }
.eve-row:hover::before { color: #7DF9FF; text-shadow: 0 0 5px #7DF9FF; }
.eve-row p { margin: 0; padding: 0; display: flex; align-items: center; } 
a.internal-link { color: #e0e0e0 !important; text-decoration: none !important; font-size: 15px; transition: 0.2s; font-weight: 500; letter-spacing: 0.5px; }
a.internal-link:hover { color: #7DF9FF !important; text-shadow: 0 0 8px #7DF9FF; }

/* ANIMATIONS ÉVOLUÉES */
@keyframes scrollHack { 0% { transform: translateY(0); } 100% { transform: translateY(-50%); } }
@keyframes pulseAlert { 0%, 100% { border-color: #ff4d4d; box-shadow: 0 0 10px rgba(255, 77, 77, 0.2); background-color: rgba(30, 0, 0, 0.5); } 50% { border-color: #ff0000; box-shadow: inset 0 0 30px rgba(255, 0, 0, 0.5), 0 0 25px rgba(255, 0, 0, 0.6); background-color: rgba(50, 0, 0, 0.8); } }
@keyframes scanMove { 0% { top: 0%; opacity: 0; } 10% { opacity: 1; } 90% { opacity: 1; } 100% { top: 100%; opacity: 0; } }
@keyframes waveform { 0%, 100% { height: 20%; } 50% { height: 100%; } }
@keyframes loadingBar { 0% { width: 0%; } 100% { width: 100%; } }
@keyframes hideText { 0%, 99% { opacity: 1; } 100% { opacity: 0; display: none; } }
@keyframes showText { 0%, 99% { opacity: 0; } 100% { opacity: 1; } }

/* CLASSES ANIMÉES */
.eve-alert-pulse { animation: pulseAlert 2s infinite; }
.scan-line { position: absolute; left: 0; width: 100%; height: 2px; background: #fff; box-shadow: 0 0 10px #fff, 0 -8px 15px rgba(255,0,0,0.8), 0 8px 15px rgba(255,0,0,0.8); z-index: 10; animation: scanMove 2.5s cubic-bezier(0.4, 0, 0.2, 1) infinite; pointer-events: none; border-radius: 50%; }

.sync-bar-container { width: 100%; height: 3px; background: #111; margin-top: 10px; position: relative; overflow: hidden; border-radius: 2px; }
.sync-bar-fill { height: 100%; background: linear-gradient(90deg, transparent, #7DF9FF); width: 100%; animation: loadingBar 2s ease-out forwards; box-shadow: 0 0 10px #7DF9FF; }
.ai-waveform-container { display: flex; align-items: flex-end; gap: 3px; height: 18px; position: absolute; bottom: 15px; right: 15px; opacity: 0.9; }
.waveform-bar { width: 3px; background-color: #7DF9FF; box-shadow: 0 0 8px #7DF9FF; border-radius: 1px; }

/* ==========================================================
   🛠️ RESPONSIVE DESIGN (POUR SMARTPHONES ET PETITS ÉCRANS)
   ========================================================== */
@media (max-width: 768px) {
    .eve-main-flex { flex-direction: column; }
    
    /* Le terminal de gauche passe en haut et devient plus petit */
    .eve-terminal-left { width: 100%; height: 120px; border-right: none; border-bottom: 1px solid #222; box-shadow: inset 0 -10px 20px rgba(0,0,0,0.9); }
    .eve-terminal-scroll { left: 10px; right: 10px; text-align: center; }
    
    /* Ajustement des marges du contenu principal */
    .eve-content { padding: 20px 15px; }
    
    /* Header (Titre plus petit pour rentrer sur l'écran) */
    .eve-window-header { flex-direction: column; text-align: center; gap: 10px; padding: 15px !important; }
    .eve-window-header strong { font-size: 12px !important; letter-spacing: 2px !important; }
    
    /* L'alerte MIO s'empile */
    .eve-alert-pulse { flex-direction: column-reverse; text-align: center; padding: 15px; }
    .eve-alert-pulse h3 { font-size: 16px !important; }
    
    /* Profil et Data empilés */
    .eve-profile-container { flex-direction: column; align-items: center; text-align: center; gap: 20px !important; }
    
    /* Tableaux plus compacts */
    .eve-table td:first-child { width: auto; display: block; padding-bottom: 2px; color: #D4AF37; }
    .eve-table td:last-child { display: block; padding-top: 2px; padding-bottom: 12px; }
    
    /* Les lignes d'archives s'adaptent */
    .eve-row { flex-direction: column; align-items: flex-start; gap: 5px; }
    .eve-row div { text-align: left !important; }
}
</style>

<div class="eve-window">

<div class="eve-window-header" style="background: linear-gradient(to bottom, #2a2a2e, #101012); padding: 12px 20px; border-bottom: 1px solid #111; display: flex; justify-content: space-between; align-items: center; position: relative; z-index: 10; box-shadow: 0 5px 15px rgba(0,0,0,0.8);">
<div style="display: flex; align-items: center; gap: 12px; justify-content: center;">
<img src="https://image.eveonline.com/Corporation/1000082_128.png" width="18" style="filter: drop-shadow(0 0 8px rgba(212, 175, 55, 1));">
<strong style="color: #fff; font-size: 15px; letter-spacing: 4px; text-transform: uppercase; text-shadow: 0 2px 4px rgba(0,0,0,0.8);">MIO // SECURE_INFO_TERMINAL // NODE 77-A</strong>
</div>
<div style="display: flex; align-items: center; gap: 8px; font-family: monospace; font-size: 11px; color: #7DF9FF; letter-spacing: 2px;">
<span style="width: 8px; height: 8px; background: #7DF9FF; border-radius: 50%; box-shadow: 0 0 10px #7DF9FF; animation: pulseAlert 1s infinite alternate;"></span> LINK SECURE
</div>
</div>

<div class="eve-main-flex">

<div class="eve-terminal-left">
<div class="eve-terminal-scroll">
<p>> CONNECTING_TO_NODE_77-A...</p>
<p>> ESTABLISHING_NEURAL_LINK...</p>
<p>> AUTH_REQUEST_SENT...</p>
<p style="color: #ff4d4d;">*WAITING_FOR_RESPONSE*</p>
<p>> MIO_AUTH_RECEIVED...</p>
<p>> SECURE_CHANNEL_ALPHA-7</p>
<p>ANALYZING_FIREWALL_LAYER_3...</p>
<p>> INJECTING_EXPLOIT_VECTOR...</p>
<p>> FIREWALL_BYPASSED...</p>
<p style="color: #ff4d4d; font-weight: bold;">> WARNING:ELEVATION_DETECTED!</p>
<p style="color: #ff4d4d; font-weight: bold;">> WARNING:ELEVATION_DETECTED!</p>
<p>> RE-ROUTING_TRACE_DETECTION...</p>
<p>PACKET_SNIFFING_ACTIVE...</p>
<p>> EXTRACTING_SIGNATURE...</p>
<p style="color: #D4AF37;">> SUCCESS!_ID:ZORATH_ITHIKA</p>
<p style="color: #ff4d4d;">> WARNING:TRACE_INBOUND!</p>
<p style="color: #ff4d4d;">> *MIO_PURGE_INITIATED*</p>
<p>> SECURITY_BREACH_SECTOR-G</p>
<p>DATA_MINING_ACTIVE...</p>
<p>> CONNECTING_TO_NODE_77-A...</p>
<p>> ESTABLISHING_NEURAL_LINK...</p>
<p>> AUTH_REQUEST_SENT...</p>
<p style="color: #ff4d4d;">*WAITING_FOR_RESPONSE*</p>
<p>> MIO_AUTH_RECEIVED...</p>
<p>> SECURE_CHANNEL_ALPHA-7</p>
<p>ANALYZING_FIREWALL_LAYER_3...</p>
<p>> INJECTING_EXPLOIT_VECTOR...</p>
<p>> FIREWALL_BYPASSED...</p>
<p style="color: #ff4d4d; font-weight: bold;">> WARNING:ELEVATION_DETECTED!</p>
<p style="color: #ff4d4d; font-weight: bold;">> WARNING:ELEVATION_DETECTED!</p>
<p>> RE-ROUTING_TRACE_DETECTION...</p>
<p>PACKET_SNIFFING_ACTIVE...</p>
<p>> EXTRACTING_SIGNATURE...</p>
<p style="color: #D4AF37;">> SUCCESS!_ID:ZORATH_ITHIKA</p>
<p style="color: #ff4d4d;">> WARNING:TRACE_INBOUND!</p>
<p style="color: #ff4d4d;">> *MIO_PURGE_INITIATED*</p>
<p>> SECURITY_BREACH_SECTOR-G</p>
<p>DATA_MINING_ACTIVE...</p>
</div>
</div>

<div class="eve-content">

<div style="border: 1px solid #222; background: rgba(0, 15, 25, 0.4); padding: 15px; margin-bottom: 30px; font-family: monospace; font-size: 11px; letter-spacing: 1px; position: relative; box-shadow: inset 0 0 20px rgba(0,255,255,0.05);">
  <div style="display: flex; justify-content: space-between; position: relative; height: 16px;">
    <div style="color: #666;">> INITIALIZING NEURAL PATHWAYS...</div>
    <div style="animation: hideText 2s forwards; position: absolute; right: 0; color: #D4AF37; text-shadow: 0 0 5px #D4AF37;">SCANNING PILOT SIGNATURE [ WAIT ]</div>
    <div style="animation: showText 2s forwards; opacity: 0; position: absolute; right: 0; color: #7DF9FF; font-weight: bold; text-shadow: 0 0 8px #7DF9FF;">SIGNATURE MATCHED [ SYNC 100% ]</div>
  </div>
  <div class="sync-bar-container">
    <div class="sync-bar-fill"></div>
  </div>
  <div class="ai-waveform-container">
    <div class="waveform-bar" style="animation: waveform 0.6s infinite 0.1s;"></div>
    <div class="waveform-bar" style="animation: waveform 0.8s infinite 0.3s;"></div>
    <div class="waveform-bar" style="animation: waveform 0.5s infinite 0.2s;"></div>
    <div class="waveform-bar" style="animation: waveform 0.9s infinite 0.5s;"></div>
    <div class="waveform-bar" style="animation: waveform 0.7s infinite 0.4s;"></div>
  </div>
</div>

<div class="eve-alert-pulse" style="border-left: 5px solid #ff4d4d; padding: 20px; margin-bottom: 40px; display: flex; justify-content: space-between; align-items: center; gap: 20px;">
<div>
<h3 style="color: #ff4d4d; margin: 0 0 8px 0; font-size: 19px; text-transform: uppercase; letter-spacing: 3px; text-shadow: 0 0 5px rgba(255,0,0,0.5);">⚠ Restricted Access Protocol</h3>
<p style="font-size: 15px; margin: 0; color: #ddd;">Monitoring active. Any synaptic deviation is logged by the Ministry of Internal Order.</p>
</div>
<img src="https://image.eveonline.com/Corporation/1000082_128.png" width="64" style="filter: drop-shadow(0 0 15px #ff0000);">
</div>

<div class="eve-profile-container" style="display: flex; gap: 40px; flex-wrap: wrap; margin-bottom: 50px; align-items: flex-start;">
<div style="width: 190px; border: 1px solid #444; padding: 5px; background: #000; position: relative; box-shadow: 0 10px 30px rgba(0,0,0,0.9);">
<div class="scan-line"></div>
<div style="position: absolute; top: -1px; left: -1px; width: 20px; height: 20px; border-top: 2px solid #D4AF37; border-left: 2px solid #D4AF37; z-index: 11;"></div>
<div style="position: absolute; bottom: -1px; right: -1px; width: 20px; height: 20px; border-bottom: 2px solid #D4AF37; border-right: 2px solid #D4AF37; z-index: 11;"></div>

![Portrait.jpg](/img/user/Images/Portrait.jpg)

</div>

<div style="flex: 1; min-width: 0; width: 100%;">
<h4 style="color: #D4AF37; border-bottom: 1px solid rgba(212, 175, 55, 0.3); padding-bottom: 10px; margin: 0 0 15px 0; font-size: 16px; letter-spacing: 4px; text-transform: uppercase;">Biometric Data</h4>
<table class="eve-table">
<tr><td>Designation</td><td>Ithika Zorath</td></tr>
<tr><td>Bio-Tech Status</td><td style="color: #7DF9FF; text-shadow: 0 0 10px rgba(125,249,255,0.6);">Capsuleer [ ACTIVE ]</td></tr>
<tr><td>Genetic Origin</td><td style="color: #bbb;">Nafomeh III (Somi)</td></tr>
<tr><td>Allegiance</td><td style="color: #D4AF37;">House Tash-Murkon</td></tr>
</table>
</div>
</div>

<h4 style="color: #555; border-bottom: 1px solid #333; padding-bottom: 10px; margin: 0 0 20px 0; font-size: 14px; letter-spacing: 3px; text-transform: uppercase;">Index Manager</h4>

<div style="border: 1px solid #222; background: rgba(0, 0, 0, 0.6); margin-bottom: 50px; box-shadow: inset 0 0 20px rgba(0,0,0,1);">

<div style="background: linear-gradient(90deg, rgba(212, 175, 55, 0.1), transparent); padding: 10px 15px; border-bottom: 1px solid #222; color: #D4AF37; font-size: 12px; letter-spacing: 2px;">
<strong>SYS.LANG // ENGLISH</strong>
</div>

<div style="padding: 10px 15px 10px 25px; display: flex; align-items: center; gap: 10px; border-bottom: 1px solid #111; background: rgba(255,255,255,0.01);">
<span style="font-size: 10px; color: #666;">▼</span> <span style="font-size: 16px;">📁</span> <strong style="color: #ccc; font-size: 14px; letter-spacing: 2px;">MIO ARCHIVES</strong>
</div>

<div class="eve-row">
<div style="flex: 2; display: flex; align-items: center; gap: 12px;">
<span style="color: #7DF9FF; font-size: 16px; filter: drop-shadow(0 0 5px #7DF9FF);">📄</span>

[[ARCHIVES MIO/EN - ARCHIVES OF HOUSE TASH-MURKON\|EN - ARCHIVES OF HOUSE TASH-MURKON]]

</div>
<div style="flex: 1; color: #666; font-size: 11px; letter-spacing: 2px;">SEC: <span style="color: #ff4d4d;">CLASSIFIED</span></div>
<div style="flex: 1; color: #666; font-size: 11px; letter-spacing: 2px; text-align: right;">SIZE: 2.4 TB</div>
</div>


<div style="background: linear-gradient(90deg, rgba(212, 175, 55, 0.1), transparent); padding: 10px 15px; border-bottom: 1px solid #222; border-top: 1px solid #222; color: #D4AF37; font-size: 12px; letter-spacing: 2px;">
<strong>SYS.LANG // FRANÇAIS</strong>
</div>

<div style="padding: 10px 15px 10px 25px; display: flex; align-items: center; gap: 10px; border-bottom: 1px solid #111; background: rgba(255,255,255,0.01);">
<span style="font-size: 10px; color: #666;">▼</span> <span style="font-size: 16px;">📁</span> <strong style="color: #ccc; font-size: 14px; letter-spacing: 2px;">ARCHIVES MIO</strong>
</div>

<div class="eve-row">
<div style="flex: 2; display: flex; align-items: center; gap: 12px;">
<span style="color: #7DF9FF; font-size: 16px; filter: drop-shadow(0 0 5px #7DF9FF);">📄</span>

[[ARCHIVES MIO/FR - ARCHIVES OF HOUSE TASH-MURKON\|FR - ARCHIVES OF HOUSE TASH-MURKON]]

</div>
<div style="flex: 1; color: #666; font-size: 11px; letter-spacing: 2px;">SÉC: <span style="color: #ff4d4d;">CLASSIFIÉ</span></div>
<div style="flex: 1; color: #666; font-size: 11px; letter-spacing: 2px; text-align: right;">TAILLE: 2.4 TB</div>
</div>

</div>

<h4 style="color: #555; border-bottom: 1px solid #333; padding-bottom: 10px; margin: 0 0 20px 0; font-size: 14px; letter-spacing: 3px; text-transform: uppercase;">External Live Feeds</h4>
<div style="display: flex; gap: 30px; flex-wrap: wrap;">
<a href="https://zkillboard.com/character/2124123129/" target="_blank" class="eve-btn eve-btn-red" style="flex: 1; min-width: 100%;">
<span style="display: block; color: #ff4d4d; font-size: 11px; margin-bottom: 10px; letter-spacing: 3px; position: relative; z-index: 2;">COMBAT REGISTRY</span>
<span style="display: block; color: #fff; font-size: 18px; letter-spacing: 2px; font-weight: bold; position: relative; z-index: 2;">[ BLOOD TITHE METRICS ]</span>
</a>
<a href="https://abysstracker.com/u/ithika-zorath" target="_blank" class="eve-btn eve-btn-cyan" style="flex: 1; min-width: 100%;">
<span style="display: block; color: #7DF9FF; font-size: 11px; margin-bottom: 10px; letter-spacing: 3px; position: relative; z-index: 2;">DEADSPACE ANOMALIES</span>
<span style="display: block; color: #fff; font-size: 18px; letter-spacing: 2px; font-weight: bold; position: relative; z-index: 2;">[ ABYSSAL TELEMETRY ]</span>
</a>
</div>

</div> </div> </div> ```