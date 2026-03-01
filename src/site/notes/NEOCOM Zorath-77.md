---
{"dg-publish":true,"permalink":"/neocom-zorath-77/","tags":["gardenEntry"],"created":"2026-02-28T21:09:16.622+01:00"}
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&display=swap');
body, .markdown-preview-view, .markdown-rendered { background-color: #030304 !important; font-family: 'Rajdhani', sans-serif !important; color: #b3b3b3 !important; }

/* Conteneur principal fluide (Plus de limitation de hauteur qui casse le site) */
.eve-window { background: rgba(12, 12, 15, 0.85); border: 1px solid #333; box-shadow: 0 15px 50px rgba(0,0,0,0.9), inset 0 0 20px rgba(0,0,0,0.5); max-width: 950px; margin: 0 auto; border-top: 3px solid #D4AF37; font-family: 'Rajdhani', sans-serif; position: relative; overflow: hidden; }
.eve-window::before { content: ""; position: absolute; top: 0; left: 0; right: 0; bottom: 0; background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%); background-size: 100% 4px; pointer-events: none; opacity: 0.3; z-index: 0; }

/* Nouveau Layout Sécurisé pour le Terminal Gauche */
.eve-main-flex { display: flex; align-items: stretch; position: relative; z-index: 1; }
.eve-terminal-left { width: 180px; flex-shrink: 0; background: #020202; border-right: 1px solid #222; position: relative; overflow: hidden; padding: 10px; font-family: monospace; color: #7DF9FF; box-shadow: inset -5px 0 15px rgba(0,0,0,0.8); }
.eve-terminal-scroll { position: absolute; top: 0; left: 10px; right: 10px; animation: scrollHack 20s linear infinite; }
.eve-terminal-scroll p { margin: 0; padding: 2px 0; font-size: 10px; line-height: 1.2; text-shadow: 0 0 4px rgba(125, 249, 255, 0.6); opacity: 0.8; }
.eve-content { flex: 1; padding: 30px; position: relative; min-width: 300px; }

/* Boutons et Liens */
.eve-btn { display: block; padding: 15px; border: 1px solid #333; text-align: center; text-decoration: none !important; transition: 0.3s; background: rgba(20,20,20,0.5); }
.eve-btn-red { border-top: 2px solid #522; }
.eve-btn-red:hover { border-color: #ff4d4d; background: rgba(255, 77, 77, 0.1); box-shadow: 0 0 15px rgba(255, 77, 77, 0.2); }
.eve-btn-cyan { border-top: 2px solid #244; }
.eve-btn-cyan:hover { border-color: #7DF9FF; background: rgba(125, 249, 255, 0.1); box-shadow: 0 0 15px rgba(125, 249, 255, 0.2); }
.eve-row { padding: 8px 15px 8px 55px; display: flex; align-items: center; border-bottom: 1px dotted #222; transition: background 0.2s; }
.eve-row:hover { background: rgba(255,255,255,0.05); }
.eve-row p { margin: 0; padding: 0; display: flex; align-items: center; } 
a.internal-link { color: #e0e0e0 !important; text-decoration: none !important; font-size: 15px; transition: 0.2s; font-weight: 500; }
a.internal-link:hover { color: #fff !important; text-shadow: 0 0 5px #fff; }

/* ANIMATIONS */
@keyframes scrollHack { 0% { transform: translateY(0); } 100% { transform: translateY(-50%); } }
@keyframes loadingBar { 0% { width: 0%; } 100% { width: 100%; } }
@keyframes hideText { 0% { opacity: 1; } 99% { opacity: 1; } 100% { opacity: 0; display: none; } }
@keyframes showText { 0% { opacity: 0; } 99% { opacity: 0; } 100% { opacity: 1; } }
@keyframes pulseGlow { 0% { opacity: 0.5; box-shadow: 0 0 5px #7DF9FF; } 50% { opacity: 1; box-shadow: 0 0 15px #7DF9FF; } 100% { opacity: 0.5; box-shadow: 0 0 5px #7DF9FF; } }
@keyframes pulseAlert { 0%, 100% { border-color: #ff4d4d; box-shadow: 0 0 10px rgba(255, 77, 77, 0.2); background-color: rgba(30, 0, 0, 0.5); } 50% { border-color: #ff0000; box-shadow: 0 0 25px rgba(255, 0, 0, 0.6); background-color: rgba(50, 0, 0, 0.7); } }
@keyframes scanMove { 0% { top: 0%; } 100% { top: 100%; } }
@keyframes waveform { 0%, 100% { height: 20%; } 50% { height: 100%; } }

/* CLASSES ANIMÉES */
.eve-alert-pulse { animation: pulseAlert 2.5s infinite; position: relative; }
.sync-bar-container { width: 100%; height: 4px; background: #222; margin-top: 8px; position: relative; overflow: hidden; }
.sync-bar-fill { height: 100%; background: #7DF9FF; width: 100%; animation: loadingBar 2.5s ease-out forwards; box-shadow: 0 0 10px #7DF9FF; }
.sync-text-loading { animation: hideText 2.5s forwards; position: absolute; }
.sync-text-done { animation: showText 2.5s forwards; opacity: 0; color: #7DF9FF; font-weight: bold; }
.sync-status-dot { width: 8px; height: 8px; background: #7DF9FF; border-radius: 50%; display: inline-block; margin-right: 8px; animation: pulseGlow 1.5s infinite; }
.scan-line { position: absolute; left: 0; width: 100%; height: 2px; background: rgba(255, 77, 77, 0.5); z-index: 10; animation: scanMove 2s linear infinite; pointer-events: none; }
.ai-waveform-container { display: flex; align-items: flex-end; gap: 2px; height: 20px; position: absolute; bottom: 15px; right: 15px; opacity: 0.8; }
.waveform-bar { width: 3px; background-color: #7DF9FF; box-shadow: 0 0 5px #7DF9FF; }
</style>

<div class="eve-window">

<div style="background: linear-gradient(to bottom, #2a2a2e, #101012); padding: 12px 20px; border-bottom: 1px solid #222; display: flex; justify-content: space-between; align-items: center; position: relative; z-index: 10;">
<div style="display: flex; align-items: center; gap: 12px;">
<img src="https://image.eveonline.com/Corporation/1000082_128.png" width="18" style="filter: drop-shadow(0 0 5px rgba(212, 175, 55, 0.8));">
<strong style="color: #fff; font-size: 15px; letter-spacing: 3px; text-transform: uppercase;">MIO // SECURE_INFO_TERMINAL // NODE 77-A</strong>
</div>
<div style="display: flex; align-items: center; gap: 6px; font-family: monospace; font-size: 10px; color: #7DF9FF; letter-spacing: 1px;">
<span class="sync-status-dot"></span> LINK ACTIVE
</div>
</div>

<div class="eve-main-flex">

<div class="eve-terminal-left">
<div class="eve-terminal-scroll">
<p>> CONNECTING_TO_NODE_77-A...</p>
<p>> ESTABLISHING_NEURAL_LINK...</p>
<p>> AUTH_REQUEST_SENT...</p>
<p>*WAITING_FOR_RESPONSE*</p>
<p>> MIO_AUTH_RECEIVED...</p>
<p>> SECURE_CHANNEL_ALPHA-7</p>
<p>ANALYZING_FIREWALL_LAYER_3...</p>
<p>> INJECTING_EXPLOIT_VECTOR...</p>
<p>> FIREWALL_BYPASSED...</p>
<p>> WARNING:ELEVATION_DETECTED!</p>
<p>> WARNING:ELEVATION_DETECTED!</p>
<p>> RE-ROUTING_TRACE_DETECTION...</p>
<p>PACKET_SNIFFING_ACTIVE...</p>
<p>> EXTRACTING_SIGNATURE...</p>
<p>> SUCCESS!_ID:ZORATH_ITHIKA</p>
<p>> WARNING:TRACE_INBOUND!</p>
<p>> *MIO_PURGE_INITIATED*</p>
<p>> SECURITY_BREACH_SECTOR-G</p>
<p>DATA_MINING_ACTIVE...</p>
<p>> CONNECTING_TO_NODE_77-A...</p>
<p>> ESTABLISHING_NEURAL_LINK...</p>
<p>> AUTH_REQUEST_SENT...</p>
<p>*WAITING_FOR_RESPONSE*</p>
<p>> MIO_AUTH_RECEIVED...</p>
<p>> SECURE_CHANNEL_ALPHA-7</p>
<p>ANALYZING_FIREWALL_LAYER_3...</p>
<p>> INJECTING_EXPLOIT_VECTOR...</p>
<p>> FIREWALL_BYPASSED...</p>
<p>> WARNING:ELEVATION_DETECTED!</p>
<p>> WARNING:ELEVATION_DETECTED!</p>
<p>> RE-ROUTING_TRACE_DETECTION...</p>
<p>PACKET_SNIFFING_ACTIVE...</p>
<p>> EXTRACTING_SIGNATURE...</p>
<p>> SUCCESS!_ID:ZORATH_ITHIKA</p>
<p>> WARNING:TRACE_INBOUND!</p>
<p>> *MIO_PURGE_INITIATED*</p>
<p>> SECURITY_BREACH_SECTOR-G</p>
<p>DATA_MINING_ACTIVE...</p>
</div>
</div>

<div class="eve-content">

<div style="border: 1px solid #333; background: rgba(0, 20, 30, 0.3); padding: 12px 15px; margin-bottom: 25px; font-family: monospace; font-size: 12px; letter-spacing: 1px; position: relative;">
  <div style="display: flex; justify-content: space-between; position: relative; height: 16px;">
    <div style="color: #888;">> INITIALIZING NEURAL PATHWAYS...</div>
    <div class="sync-text-loading" style="right: 0; color: #D4AF37;">SCANNING PILOT SIGNATURE [ WAIT ]</div>
    <div class="sync-text-done" style="right: 0;">SIGNATURE MATCHED [ SYNC 100% ]</div>
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

<div class="eve-alert-pulse" style="border-left: 4px solid #ff4d4d; padding: 18px; margin-bottom: 35px; display: flex; justify-content: space-between; align-items: center; gap: 20px;">
<div>
<h3 style="color: #ff4d4d; margin: 0 0 8px 0; font-size: 18px; text-transform: uppercase; letter-spacing: 2px;">⚠ Restricted Access Protocol</h3>
<p style="font-size: 15px; margin: 0; color: #ccc;">Monitoring active. Any synaptic deviation is logged by the Ministry of Internal Order.</p>
</div>
<img src="https://image.eveonline.com/Corporation/1000082_128.png" width="64" style="opacity: 0.85; filter: drop-shadow(0 0 12px rgba(255, 77, 77, 0.6)); flex-shrink: 0;">
</div>

<div style="display: flex; gap: 40px; flex-wrap: wrap; margin-bottom: 40px; align-items: flex-start;">
<div style="width: 190px; border: 1px solid #444; padding: 4px; background: #000; position: relative; box-shadow: 0 0 20px rgba(0,0,0,0.8);">
<div class="scan-line"></div>
<div style="position: absolute; top: -1px; left: -1px; width: 15px; height: 15px; border-top: 2px solid #D4AF37; border-left: 2px solid #D4AF37; z-index: 11;"></div>
<div style="position: absolute; bottom: -1px; right: -1px; width: 15px; height: 15px; border-bottom: 2px solid #D4AF37; border-right: 2px solid #D4AF37; z-index: 11;"></div>

![Portrait.jpg](/img/user/Images/Portrait.jpg)

</div>

<div style="flex: 1; min-width: 300px;">
<h4 style="color: #D4AF37; border-bottom: 1px solid #333; padding-bottom: 8px; margin: 0 0 20px 0; font-size: 18px; letter-spacing: 2px; text-transform: uppercase;">Biometric Data</h4>
<table style="width: 100%; border-collapse: collapse; font-size: 16px; color: #ddd;">
<tr style="border-bottom: 1px solid #222;"><td style="padding: 12px 5px; color: #888; width: 40%;">Designation</td><td style="font-weight: bold; color: #fff;">Ithika Zorath</td></tr>
<tr style="border-bottom: 1px solid #222;"><td style="padding: 12px 5px; color: #888;">Bio-Tech Status</td><td style="color: #7DF9FF; text-shadow: 0 0 8px rgba(125,249,255,0.4);">Capsuleer [ ACTIVE ]</td></tr>
<tr style="border-bottom: 1px solid #222;"><td style="padding: 12px 5px; color: #888;">Genetic Origin</td><td style="color: #bbb;">Nafomeh III (Somi)</td></tr>
<tr style="border-bottom: 1px solid #222;"><td style="padding: 12px 5px; color: #888;">Allegiance</td><td style="color: #D4AF37; font-weight: bold;">House Tash-Murkon</td></tr>
</table>
</div>
</div>

<h4 style="color: #555; border-bottom: 1px solid #222; padding-bottom: 8px; margin: 0 0 15px 0; font-size: 14px; letter-spacing: 2px; text-transform: uppercase;">Index Manager</h4>

<div style="border: 1px solid #333; background: #08080a; margin-bottom: 40px; box-shadow: inset 0 0 10px rgba(0,0,0,0.8);">

<div style="background: rgba(212, 175, 55, 0.05); padding: 8px 12px; border-bottom: 1px solid #222; color: #D4AF37; font-size: 13px; letter-spacing: 1px;">
<strong>SYS.LANG // ENGLISH</strong>
</div>

<div style="padding: 8px 15px 8px 25px; display: flex; align-items: center; gap: 8px; border-bottom: 1px solid #1a1a1a; background: rgba(255,255,255,0.02);">
<span style="font-size: 10px; color: #888;">▼</span> <span style="font-size: 14px;">📁</span> <strong style="color: #e0e0e0; font-size: 14px; letter-spacing: 1px;">MIO ARCHIVES</strong>
</div>

<div class="eve-row">
<div style="flex: 2; display: flex; align-items: center; gap: 8px;">
<span style="color: #7DF9FF; font-size: 14px;">📄</span>

[[ARCHIVES MIO/EN - ARCHIVES OF HOUSE TASH-MURKON\|EN - ARCHIVES OF HOUSE TASH-MURKON]]

</div>
<div style="flex: 1; color: #888; font-size: 12px; letter-spacing: 1px;">Security: CLASSIFIED</div>
<div style="flex: 1; color: #888; font-size: 12px; letter-spacing: 1px; text-align: right;">Size: 2.4 TB</div>
</div>


<div style="background: rgba(212, 175, 55, 0.05); padding: 8px 12px; border-bottom: 1px solid #222; border-top: 1px solid #333; color: #D4AF37; font-size: 13px; letter-spacing: 1px;">
<strong>SYS.LANG // FRANÇAIS</strong>
</div>

<div style="padding: 8px 15px 8px 25px; display: flex; align-items: center; gap: 8px; border-bottom: 1px solid #1a1a1a; background: rgba(255,255,255,0.02);">
<span style="font-size: 10px; color: #888;">▼</span> <span style="font-size: 14px;">📁</span> <strong style="color: #e0e0e0; font-size: 14px; letter-spacing: 1px;">ARCHIVES MIO</strong>
</div>

<div class="eve-row">
<div style="flex: 2; display: flex; align-items: center; gap: 8px;">
<span style="color: #7DF9FF; font-size: 14px;">📄</span>

[[ARCHIVES MIO/FR - ARCHIVES OF HOUSE TASH-MURKON\|FR - ARCHIVES OF HOUSE TASH-MURKON]]

</div>
<div style="flex: 1; color: #888; font-size: 12px; letter-spacing: 1px;">Sécurité: CLASSIFIÉ</div>
<div style="flex: 1; color: #888; font-size: 12px; letter-spacing: 1px; text-align: right;">Taille: 2.4 TB</div>
</div>

</div>

<h4 style="color: #555; border-bottom: 1px solid #222; padding-bottom: 8px; margin: 0 0 20px 0; font-size: 14px; letter-spacing: 2px; text-transform: uppercase;">External Live Feeds</h4>
<div style="display: flex; gap: 30px; flex-wrap: wrap;">
<a href="https://zkillboard.com/character/2124123129/" target="_blank" class="eve-btn eve-btn-red" style="flex: 1; min-width: 250px;">
<span style="display: block; color: #ff4d4d; font-size: 11px; margin-bottom: 8px; letter-spacing: 2px;">COMBAT REGISTRY</span>
<span style="display: block; color: #fff; font-size: 18px; letter-spacing: 1px; font-weight: bold;">[ BLOOD TITHE METRICS ]</span>
</a>
<a href="https://abysstracker.com/u/ithika-zorath" target="_blank" class="eve-btn eve-btn-cyan" style="flex: 1; min-width: 250px;">
<span style="display: block; color: #7DF9FF; font-size: 11px; margin-bottom: 8px; letter-spacing: 2px;">DEADSPACE ANOMALIES</span>
<span style="display: block; color: #fff; font-size: 18px; letter-spacing: 1px; font-weight: bold;">[ ABYSSAL TELEMETRY ]</span>
</a>
</div>

</div> </div> </div> ```