---
{"dg-publish":true,"permalink":"/neocom-zorath-77/","tags":["gardenEntry"],"created":"2026-02-28T21:09:16.622+01:00"}
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Electrolize&family=Share+Tech+Mono&family=Cinzel:wght@400;600&display=swap');

:root {
    --file-line-width: 1050px !important;
    --line-width: 1050px !important;
    --content-width: 1050px !important;
    --eve-gold:        #D4AF37;
    --eve-gold-dim:    #8B6914;
    --eve-gold-glow:   rgba(212, 175, 55, 0.25);
    --eve-cyan:        #7DF9FF;
    --eve-cyan-dim:    #2a6b70;
    --eve-red:         #ff4d4d;
    --eve-red-dim:     #522;
    --eve-bg:          #010102;
    --eve-bg-panel:    rgba(8, 9, 12, 0.96);
    --eve-border:      #2a2a2e;
    --eve-border-dim:  #1a1a1e;
    --font-ui:         'Electrolize', monospace;
    --font-data:       'Share Tech Mono', monospace;
    --font-lore:       'Cinzel', serif;
    --font-body:       'Rajdhani', sans-serif;
}

#page-content, .content, .dg-content-container,
.markdown-preview-sizer, .markdown-preview-view, .markdown-rendered {
    max-width: 1050px !important; width: 100% !important;
    margin-left: auto !important; margin-right: auto !important;
    padding-left: 0 !important; padding-right: 0 !important; float: none !important;
}
body, .markdown-preview-view, .markdown-rendered {
    background-color: var(--eve-bg) !important;
    font-family: var(--font-body) !important; color: #b3b3b3 !important;
}
.eve-window {
    background: var(--eve-bg-panel); border: 1px solid var(--eve-border);
    box-shadow: 0 15px 50px rgba(0,0,0,1), inset 0 0 40px rgba(0,0,0,0.8);
    width: 100%; max-width: 1050px; margin: 0 auto !important;
    border-top: 2px solid var(--eve-gold); font-family: var(--font-body);
    position: relative; overflow: hidden; display: block;
}
.eve-window::before {
    content: ""; position: absolute; top: 0; right: 0; width: 0; height: 0;
    border-style: solid; border-width: 0 22px 22px 0;
    border-color: transparent var(--eve-gold) transparent transparent; z-index: 20;
}
.eve-window::after {
    content: ""; position: absolute; top: 0; left: 0; right: 0; bottom: 0;
    background: linear-gradient(rgba(18,16,16,0) 50%, rgba(0,0,0,0.18) 50%),
                linear-gradient(90deg, rgba(255,0,0,0.02), rgba(0,255,255,0.015));
    background-size: 100% 3px, 3px 100%; pointer-events: none; opacity: 0.5; z-index: 50;
}
.eve-window-header {
    background: linear-gradient(to bottom, #1e1e22, #0a0a0d);
    padding: 9px 18px; border-bottom: 1px solid #111;
    display: flex; justify-content: space-between; align-items: center;
    position: relative; z-index: 10; box-shadow: 0 3px 12px rgba(0,0,0,0.9);
}
.eve-window-header::after {
    content: ""; position: absolute; bottom: 0; left: 0; right: 0; height: 1px;
    background: linear-gradient(90deg, transparent, var(--eve-gold), transparent); opacity: 0.4;
}
.eve-header-title {
    display: flex; align-items: center; gap: 10px; font-family: var(--font-ui);
    font-size: 12px; color: #c8c8c8; letter-spacing: 3px; text-transform: uppercase;
}
.eve-header-title img { filter: drop-shadow(0 0 6px rgba(212,175,55,0.9)); }
.eve-status-pill {
    display: flex; align-items: center; gap: 7px; font-family: var(--font-data);
    font-size: 10px; color: var(--eve-cyan); letter-spacing: 2px;
    background: rgba(125,249,255,0.04); border: 1px solid rgba(125,249,255,0.15); padding: 3px 10px;
}
.eve-status-dot {
    width: 6px; height: 6px; background: var(--eve-cyan); border-radius: 50%;
    box-shadow: 0 0 8px var(--eve-cyan); animation: pulseAlert 1.4s infinite alternate;
}
.eve-main-flex { display: flex; align-items: stretch; position: relative; z-index: 1; }
.eve-terminal-left {
    width: 190px; flex-shrink: 0; background: #000; border-right: 1px solid #1a1a1e;
    position: relative; overflow: hidden; font-family: var(--font-data); color: var(--eve-cyan);
    box-shadow: inset -8px 0 16px rgba(0,0,0,0.9);
    -webkit-mask-image: linear-gradient(to bottom, transparent 0%, black 8%, black 92%, transparent 100%);
    mask-image: linear-gradient(to bottom, transparent 0%, black 8%, black 92%, transparent 100%);
}
.eve-terminal-scroll {
    position: absolute; top: 0; left: 12px; right: 8px; animation: scrollHack 16s linear infinite;
}
.eve-terminal-scroll p {
    margin: 0; padding: 2px 0; font-size: 10px; line-height: 1.4;
    text-shadow: 0 0 5px rgba(125,249,255,0.7); opacity: 0.8; letter-spacing: 0.3px;
}
.eve-content {
    flex: 1; padding: 28px 32px; position: relative; min-width: 0;
    background: radial-gradient(ellipse at 30% 20%, rgba(20,18,10,0.6) 0%, rgba(0,0,0,0.85) 100%);
}
.eve-section-label {
    font-family: var(--font-ui); font-size: 10px; letter-spacing: 3px; text-transform: uppercase;
    color: #555; border-bottom: 1px solid var(--eve-border); padding-bottom: 7px;
    margin: 0 0 16px 0; display: flex; align-items: center; gap: 8px;
}
.eve-section-label::before {
    content: ""; display: inline-block; width: 8px; height: 8px;
    background: var(--eve-gold-dim); clip-path: polygon(50% 0%,100% 50%,50% 100%,0% 50%);
}
.eve-alert-pulse {
    animation: pulseAlert 2.2s infinite; border-left: 4px solid var(--eve-red);
    padding: 14px 18px; margin-bottom: 28px;
    display: flex; justify-content: space-between; align-items: center; gap: 18px; position: relative;
}
.eve-alert-pulse::after {
    content: ""; position: absolute; bottom: 0; right: 0; width: 0; height: 0;
    border-style: solid; border-width: 10px 10px 0 0;
    border-color: transparent var(--eve-red-dim) transparent transparent; opacity: 0.6;
}
.eve-alert-title {
    font-family: var(--font-ui); color: var(--eve-red); font-size: 13px; letter-spacing: 3px;
    text-transform: uppercase; margin: 0 0 5px 0; display: flex; align-items: center; gap: 8px;
}
.eve-alert-body { font-family: var(--font-body); font-size: 14px; margin: 0; color: #ccc; }
.eve-table { width: 100%; border-collapse: collapse; font-family: var(--font-body); margin-bottom: 0; }
.eve-table tr { border-bottom: 1px solid rgba(212,175,55,0.1); transition: all 0.15s ease; }
.eve-table tr:hover {
    background: linear-gradient(90deg, rgba(212,175,55,0.07) 0%, transparent 100%);
    border-left: 2px solid var(--eve-gold); transform: translateX(2px);
}
.eve-table td { padding: 9px 10px; }
.eve-table td:first-child {
    font-family: var(--font-ui); color: #555; width: 38%;
    text-transform: uppercase; font-size: 10px; letter-spacing: 2px;
}
.eve-table td:last-child {
    font-family: var(--font-body); color: #e8e8e8; font-weight: 500;
    font-size: 14px; word-break: break-word;
}
.eve-index-container {
    border: 1px solid var(--eve-border); background: rgba(0,0,0,0.7);
    box-shadow: inset 0 0 30px rgba(0,0,0,0.9);
}
.eve-lang-header {
    background: linear-gradient(90deg, rgba(212,175,55,0.12), rgba(212,175,55,0.02) 60%, transparent);
    padding: 7px 14px; border-bottom: 1px solid rgba(212,175,55,0.2);
    display: flex; align-items: center; gap: 8px;
}
.eve-lang-header-text {
    font-family: var(--font-ui); color: var(--eve-gold); font-size: 10px; letter-spacing: 3px; text-transform: uppercase;
}
.eve-lang-icon {
    width: 9px; height: 9px; border: 1px solid var(--eve-gold-dim);
    clip-path: polygon(50% 0%,100% 50%,50% 100%,0% 50%); background: var(--eve-gold-dim); flex-shrink: 0;
}
.eve-folder-header {
    padding: 7px 14px 7px 20px; display: flex; align-items: center; gap: 7px;
    border-bottom: 1px solid var(--eve-border-dim); background: rgba(255,255,255,0.008);
}
.eve-folder-chevron { font-size: 8px; color: #555; font-family: var(--font-ui); }
.eve-folder-name { font-family: var(--font-ui); color: #999; font-size: 11px; letter-spacing: 2px; text-transform: uppercase; }
.eve-row {
    padding: 8px 14px 8px 35px; display: flex; align-items: center;
    border-bottom: 1px solid rgba(255,255,255,0.025); transition: all 0.15s;
    position: relative; flex-wrap: wrap;
}
.eve-row::before {
    content: "▶"; position: absolute; left: 13px; font-size: 7px;
    color: #333; transition: 0.15s; font-family: var(--font-ui);
}
.eve-row:hover {
    background: linear-gradient(90deg, rgba(125,249,255,0.04) 0%, transparent 80%);
    padding-left: 40px; border-left: 1px solid rgba(125,249,255,0.2);
}
.eve-row:hover::before { color: var(--eve-cyan); text-shadow: 0 0 5px var(--eve-cyan); }
.eve-row p { margin: 0; padding: 0; display: flex; align-items: center; }
.eve-file-icon { width: 13px; height: 13px; flex-shrink: 0; margin-right: 9px; }
a.internal-link {
    font-family: var(--font-body); color: #d0d0d0 !important; text-decoration: none !important;
    font-size: 13px; transition: 0.15s; font-weight: 500; letter-spacing: 0.3px;
}
a.internal-link:hover { color: var(--eve-cyan) !important; text-shadow: 0 0 6px rgba(125,249,255,0.5); }
.eve-badge {
    font-family: var(--font-data); font-size: 9px; letter-spacing: 1.5px;
    padding: 1px 5px; border: 1px solid currentColor; opacity: 0.85;
}
.eve-meta { font-family: var(--font-data); font-size: 10px; color: #3a3a3a; letter-spacing: 1px; }
.eve-btn {
    display: block; padding: 13px 16px; border: 1px solid #2a2a2e; text-align: center;
    text-decoration: none !important; transition: 0.25s; background: rgba(8,8,10,0.9);
    position: relative; overflow: hidden;
    clip-path: polygon(0 0, calc(100% - 10px) 0, 100% 10px, 100% 100%, 10px 100%, 0 calc(100% - 10px));
}
.eve-btn::before {
    content: ""; position: absolute; top: 0; left: -100%; width: 40%; height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
    transform: skewX(-15deg); transition: 0.4s;
}
.eve-btn:hover::before { left: 150%; }
.eve-btn-label {
    font-family: var(--font-ui); font-size: 9px; letter-spacing: 3px; text-transform: uppercase;
    margin-bottom: 7px; display: block; position: relative; z-index: 2;
}
.eve-btn-title {
    font-family: var(--font-lore); font-size: 13px; letter-spacing: 2px; font-weight: 600;
    display: block; position: relative; z-index: 2; color: #e0e0e0;
}
.eve-btn-red { border-top: 1px solid #4a1a1a; border-bottom: 1px solid #4a1a1a; }
.eve-btn-red:hover { border-color: rgba(255,77,77,0.6); background: rgba(255,77,77,0.06); box-shadow: 0 0 20px rgba(255,77,77,0.12); }
.eve-btn-cyan { border-top: 1px solid #0a2a2e; border-bottom: 1px solid #0a2a2e; }
.eve-btn-cyan:hover { border-color: rgba(125,249,255,0.4); background: rgba(125,249,255,0.05); box-shadow: 0 0 20px rgba(125,249,255,0.1); }
.eve-sync-block {
    border: 1px solid #1a1e22; background: rgba(0,12,20,0.5);
    padding: 12px 14px 26px 14px; margin-bottom: 24px; font-family: var(--font-data);
    font-size: 10px; letter-spacing: 1px; position: relative; box-shadow: inset 0 0 15px rgba(0,255,255,0.03);
}
.eve-sync-block::before {
    content: ""; position: absolute; top: 0; left: 0; width: 0; height: 0; border-style: solid;
    border-width: 12px 12px 0 0; border-color: var(--eve-cyan-dim) transparent transparent transparent; opacity: 0.5;
}
.sync-bar-container { width: 100%; height: 2px; background: #0a1015; margin-top: 10px; position: relative; overflow: hidden; }
.sync-bar-fill {
    height: 100%; background: linear-gradient(90deg, transparent, var(--eve-cyan), rgba(125,249,255,0.3));
    width: 100%; animation: loadingBar 2s ease-out forwards; box-shadow: 0 0 8px var(--eve-cyan);
}
.ai-waveform-container {
    display: flex; align-items: flex-end; gap: 2px; height: 14px;
    position: absolute; bottom: 8px; right: 12px; opacity: 0.8;
}
.waveform-bar { width: 2px; background-color: var(--eve-cyan); box-shadow: 0 0 5px var(--eve-cyan); border-radius: 1px; }
.eve-profile-frame {
    border: 1px solid #3a3a3e; padding: 4px; background: #000;
    position: relative; box-shadow: 0 8px 25px rgba(0,0,0,0.9); flex-shrink: 0;
}
.eve-profile-frame::before {
    content: ""; position: absolute; top: -1px; left: -1px; width: 16px; height: 16px;
    border-top: 2px solid var(--eve-gold); border-left: 2px solid var(--eve-gold); z-index: 11;
}
.eve-profile-frame::after {
    content: ""; position: absolute; bottom: -1px; right: -1px; width: 16px; height: 16px;
    border-bottom: 2px solid var(--eve-gold); border-right: 2px solid var(--eve-gold); z-index: 11;
}
.scan-line {
    position: absolute; left: 0; width: 100%; height: 1px;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.6), transparent);
    box-shadow: 0 0 8px rgba(255,255,255,0.4), 0 -4px 10px rgba(255,100,100,0.5), 0 4px 10px rgba(255,100,100,0.5);
    z-index: 10; animation: scanMove 2.8s cubic-bezier(0.4,0,0.2,1) infinite; pointer-events: none;
}
.eve-killboard { border: 1px solid var(--eve-border); background: rgba(0,0,0,0.6); margin-bottom: 28px; overflow: hidden; }
.eve-killboard-header {
    background: linear-gradient(90deg, rgba(255,77,77,0.1), transparent);
    padding: 8px 14px; border-bottom: 1px solid rgba(255,77,77,0.2);
    display: flex; justify-content: space-between; align-items: center;
}
.eve-kill-row {
    display: flex; align-items: center; gap: 10px; padding: 9px 14px;
    border-bottom: 1px solid rgba(255,255,255,0.03); border-left: 3px solid transparent;
    transition: all 0.15s; cursor: pointer;
}
.eve-kill-row:hover { background: rgba(212,175,55,0.04); }
.eve-kill-ship { width: 36px; height: 36px; flex-shrink: 0; border: 1px solid #222; background: #000; overflow: hidden; }
.eve-kill-ship img { width: 100%; height: 100%; object-fit: cover; opacity: 0.85; }
.eve-divider { display: flex; align-items: center; gap: 10px; margin: 24px 0; }
.eve-divider::before { content: ""; flex: 1; height: 1px; background: linear-gradient(90deg, transparent, var(--eve-border)); }
.eve-divider::after  { content: ""; flex: 1; height: 1px; background: linear-gradient(90deg, var(--eve-border), transparent); }
.eve-divider-icon { width: 8px; height: 8px; background: var(--eve-gold-dim); clip-path: polygon(50% 0%,100% 50%,50% 100%,0% 50%); }

@keyframes scrollHack  { 0% { transform: translateY(0); }    100% { transform: translateY(-50%); } }
@keyframes scanMove    { 0% { top: 0%; opacity: 0; } 8% { opacity: 1; } 92% { opacity: 1; } 100% { top: 100%; opacity: 0; } }
@keyframes waveform    { 0%, 100% { height: 15%; } 50% { height: 100%; } }
@keyframes loadingBar  { 0% { width: 0%; } 100% { width: 100%; } }
@keyframes hideText    { 0%, 99% { opacity: 1; } 100% { opacity: 0; } }
@keyframes showText    { 0%, 99% { opacity: 0; } 100% { opacity: 1; } }
@keyframes pulseAlert  {
    0%,100% { border-color: var(--eve-red); box-shadow: 0 0 8px rgba(255,77,77,0.15); background-color: rgba(25,0,0,0.5); }
    50%      { border-color: #ff1a1a; box-shadow: inset 0 0 25px rgba(255,0,0,0.4), 0 0 20px rgba(255,0,0,0.5); background-color: rgba(45,0,0,0.75); }
}
@keyframes fadeSlideIn { from { opacity:0; transform: translateX(-6px); } to { opacity:1; transform: translateX(0); } }

@media (min-width: 769px) { .eve-window { min-width: 850px !important; } }
@media (max-width: 768px) {
    .eve-main-flex { flex-direction: column; }
    .eve-terminal-left { width: 100%; height: 100px; border-right: none; border-bottom: 1px solid #1a1a1e; }
    .eve-content { padding: 16px 14px; }
    .eve-window-header { flex-direction: column; gap: 8px; padding: 12px !important; }
    .eve-alert-pulse { flex-direction: column-reverse; text-align: center; }
    .eve-two-col { flex-direction: column !important; }
    .eve-table td:first-child { display: block; padding-bottom: 2px; }
    .eve-table td:last-child  { display: block; padding-top: 2px; padding-bottom: 10px; }
    .eve-row { flex-direction: column; align-items: flex-start; gap: 4px; }
    .eve-row div { text-align: left !important; }
}
</style>

<div class="eve-window">

<div class="eve-window-header">
  <div class="eve-header-title">
    <img src="https://image.eveonline.com/Corporation/1000082_128.png" width="16">
    MIO // SECURE_INFO_TERMINAL // NODE 77-A
  </div>
  <div class="eve-status-pill">
    <span class="eve-status-dot"></span> LINK SECURE
  </div>
</div>

<div class="eve-main-flex">

<div class="eve-terminal-left">
  <div class="eve-terminal-scroll">
    <p>> CONNECTING_TO_NODE_77-A...</p>
    <p>> ESTABLISHING_NEURAL_LINK...</p>
    <p>> AUTH_REQUEST_SENT...</p>
    <p style="color:#ff4d4d;">*WAITING_FOR_RESPONSE*</p>
    <p>> MIO_AUTH_RECEIVED...</p>
    <p>> SECURE_CHANNEL_ALPHA-7</p>
    <p>ANALYZING_FIREWALL_LAYER_3...</p>
    <p>> INJECTING_EXPLOIT_VECTOR...</p>
    <p>> FIREWALL_BYPASSED...</p>
    <p style="color:#ff4d4d;font-weight:bold;">> WARNING:ELEVATION_DETECTED!</p>
    <p style="color:#ff4d4d;font-weight:bold;">> WARNING:ELEVATION_DETECTED!</p>
    <p>> RE-ROUTING_TRACE_DETECTION...</p>
    <p>PACKET_SNIFFING_ACTIVE...</p>
    <p>> EXTRACTING_SIGNATURE...</p>
    <p style="color:#D4AF37;">> SUCCESS!_ID:ZORATH_ITHIKA</p>
    <p style="color:#ff4d4d;">> WARNING:TRACE_INBOUND!</p>
    <p style="color:#ff4d4d;">> *MIO_PURGE_INITIATED*</p>
    <p>> SECURITY_BREACH_SECTOR-G</p>
    <p>DATA_MINING_ACTIVE...</p>
    <p>> CONNECTING_TO_NODE_77-A...</p>
    <p>> ESTABLISHING_NEURAL_LINK...</p>
    <p>> AUTH_REQUEST_SENT...</p>
    <p style="color:#ff4d4d;">*WAITING_FOR_RESPONSE*</p>
    <p>> MIO_AUTH_RECEIVED...</p>
    <p>> SECURE_CHANNEL_ALPHA-7</p>
    <p>ANALYZING_FIREWALL_LAYER_3...</p>
    <p>> INJECTING_EXPLOIT_VECTOR...</p>
    <p>> FIREWALL_BYPASSED...</p>
    <p style="color:#ff4d4d;font-weight:bold;">> WARNING:ELEVATION_DETECTED!</p>
    <p style="color:#ff4d4d;font-weight:bold;">> WARNING:ELEVATION_DETECTED!</p>
    <p>> RE-ROUTING_TRACE_DETECTION...</p>
    <p>PACKET_SNIFFING_ACTIVE...</p>
    <p>> EXTRACTING_SIGNATURE...</p>
    <p style="color:#D4AF37;">> SUCCESS!_ID:ZORATH_ITHIKA</p>
    <p style="color:#ff4d4d;">> WARNING:TRACE_INBOUND!</p>
    <p style="color:#ff4d4d;">> *MIO_PURGE_INITIATED*</p>
    <p>> SECURITY_BREACH_SECTOR-G</p>
    <p>DATA_MINING_ACTIVE...</p>
  </div>
</div>

<div class="eve-content">

  <!-- NEURAL SYNC -->
  <div class="eve-sync-block">
    <div style="display:flex;justify-content:space-between;align-items:flex-start;flex-wrap:wrap;gap:10px;">
      <div style="color:#3a5060;font-family:var(--font-data);font-size:10px;">> INITIALIZING NEURAL PATHWAYS...</div>
      <div style="position:relative;width:230px;height:14px;">
        <div style="animation:hideText 2s forwards;position:absolute;right:0;top:0;color:var(--eve-gold);font-family:var(--font-data);font-size:10px;letter-spacing:1px;text-shadow:0 0 5px var(--eve-gold);width:100%;text-align:right;">SCANNING PILOT SIGNATURE [ WAIT ]</div>
        <div style="animation:showText 2s forwards;opacity:0;position:absolute;right:0;top:0;color:var(--eve-cyan);font-family:var(--font-data);font-size:10px;letter-spacing:1px;font-weight:bold;text-shadow:0 0 6px var(--eve-cyan);width:100%;text-align:right;">SIGNATURE MATCHED [ SYNC 100% ]</div>
      </div>
    </div>
    <div class="sync-bar-container"><div class="sync-bar-fill"></div></div>
    <div class="ai-waveform-container">
      <div class="waveform-bar" style="animation:waveform 0.6s infinite 0.1s;"></div>
      <div class="waveform-bar" style="animation:waveform 0.8s infinite 0.3s;"></div>
      <div class="waveform-bar" style="animation:waveform 0.5s infinite 0.2s;"></div>
      <div class="waveform-bar" style="animation:waveform 0.9s infinite 0.5s;"></div>
      <div class="waveform-bar" style="animation:waveform 0.7s infinite 0.4s;"></div>
    </div>
  </div>

  <!-- ALERTE -->
  <div class="eve-alert-pulse">
    <div>
      <div class="eve-alert-title">
        <svg width="14" height="14" viewBox="0 0 16 16" fill="none" style="position:relative;top:1px;flex-shrink:0;">
          <path d="M8 1 L15 14 L1 14 Z" stroke="#ff4d4d" stroke-width="1.2" fill="rgba(255,77,77,0.1)"/>
          <line x1="8" y1="6" x2="8" y2="10" stroke="#ff4d4d" stroke-width="1.5"/>
          <circle cx="8" cy="12" r="0.8" fill="#ff4d4d"/>
        </svg>
        RESTRICTED ACCESS PROTOCOL
      </div>
      <p class="eve-alert-body">Monitoring active. Any synaptic deviation is logged by the Ministry of Internal Order.</p>
    </div>
    <img src="https://image.eveonline.com/Corporation/1000082_128.png" width="52" style="filter:drop-shadow(0 0 12px #ff0000);flex-shrink:0;">
  </div>

  <!-- BLOC PRINCIPAL : PROFIL GAUCHE + INDEX DROITE -->
  <div class="eve-two-col" style="display:flex;gap:24px;align-items:flex-start;margin-bottom:28px;">

    <!-- COLONNE GAUCHE : Portrait + Bio -->
    <div style="width:210px;flex-shrink:0;">
      <div class="eve-section-label" style="margin-bottom:12px;">Biometric Data</div>
      <div class="eve-profile-frame" style="width:100%;margin-bottom:14px;">
        <div class="scan-line"></div>

![Portrait.jpg](/img/user/Images/Portrait.jpg)

      </div>
      <table class="eve-table">
        <tr><td>Callsign</td><td>Ithika Zorath</td></tr>
        <tr><td>Status</td><td style="color:var(--eve-cyan);font-family:var(--font-data);font-size:12px;">Capsuleer <span style="color:#4a8a8e;">[ ACTIVE ]</span></td></tr>
        <tr><td>Origin</td><td style="color:#aaa;">Nafomeh III</td></tr>
        <tr><td>House</td><td style="color:var(--eve-gold);font-family:var(--font-lore);font-size:12px;">Tash-Murkon</td></tr>
        <tr><td>Year</td><td style="color:#666;font-family:var(--font-data);font-size:12px;">YC128</td></tr>
      </table>
    </div>

    <!-- COLONNE DROITE : Index -->
    <div style="flex:1;min-width:0;">
      <div class="eve-section-label" style="margin-bottom:12px;">Index Manager</div>
      <div class="eve-index-container">

        <div class="eve-lang-header">
          <span class="eve-lang-icon"></span>
          <span class="eve-lang-header-text">SYS.LANG // ENGLISH</span>
        </div>
        <div class="eve-folder-header">
          <span class="eve-folder-chevron">▼</span>
          <svg width="12" height="12" viewBox="0 0 13 13" style="flex-shrink:0;"><path d="M1 3.5 L1 12 L12 12 L12 3.5 L6 3.5 L5 1.5 L1 1.5 Z" fill="#1a1a1e" stroke="#444" stroke-width="0.8"/></svg>
          <span class="eve-folder-name">MIO Archives</span>
        </div>
        <div class="eve-row">
          <div style="flex:2;display:flex;align-items:center;">
            <svg class="eve-file-icon" viewBox="0 0 14 14"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#0a1520" stroke="#7DF9FF" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#7DF9FF" stroke-width="0.6" opacity="0.6"/><line x1="3" y1="6" x2="8" y2="6" stroke="#7DF9FF" stroke-width="0.6" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#7DF9FF" stroke-width="0.6" opacity="0.4"/></svg>

[[ARCHIVES MIO/EN - ARCHIVES OF HOUSE TASH-MURKON\|EN - ARCHIVES OF HOUSE TASH-MURKON]]

          </div>
          <div style="flex:1;"><span class="eve-badge" style="color:var(--eve-red);">CLASSIFIED</span></div>
          <div style="flex:1;text-align:right;" class="eve-meta">2.4 TB</div>
        </div>
        <div class="eve-row">
          <div style="flex:2;display:flex;align-items:center;">
            <svg class="eve-file-icon" viewBox="0 0 14 14"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#12100a" stroke="#D4AF37" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#D4AF37" stroke-width="0.6" opacity="0.7"/><line x1="3" y1="6" x2="8" y2="6" stroke="#D4AF37" stroke-width="0.6" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#D4AF37" stroke-width="0.6" opacity="0.4"/></svg>

[[ARCHIVES MIO/EN - Logbook 02-YC128\|EN - Logbook 02-YC128]]

          </div>
          <div style="flex:1;"><span class="eve-badge" style="color:var(--eve-gold);">RESTRICTED</span></div>
          <div style="flex:1;text-align:right;" class="eve-meta">02 / YC128</div>
        </div>

        <div class="eve-lang-header" style="border-top:1px solid rgba(212,175,55,0.1);">
          <span class="eve-lang-icon"></span>
          <span class="eve-lang-header-text">SYS.LANG // FRANÇAIS</span>
        </div>
        <div class="eve-folder-header">
          <span class="eve-folder-chevron">▼</span>
          <svg width="12" height="12" viewBox="0 0 13 13" style="flex-shrink:0;"><path d="M1 3.5 L1 12 L12 12 L12 3.5 L6 3.5 L5 1.5 L1 1.5 Z" fill="#1a1a1e" stroke="#444" stroke-width="0.8"/></svg>
          <span class="eve-folder-name">Archives MIO</span>
        </div>
        <div class="eve-row">
          <div style="flex:2;display:flex;align-items:center;">
            <svg class="eve-file-icon" viewBox="0 0 14 14"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#0a1520" stroke="#7DF9FF" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#7DF9FF" stroke-width="0.6" opacity="0.6"/><line x1="3" y1="6" x2="8" y2="6" stroke="#7DF9FF" stroke-width="0.6" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#7DF9FF" stroke-width="0.6" opacity="0.4"/></svg>

[[ARCHIVES MIO/FR - ARCHIVES OF HOUSE TASH-MURKON\|FR - ARCHIVES OF HOUSE TASH-MURKON]]

          </div>
          <div style="flex:1;"><span class="eve-badge" style="color:var(--eve-red);">CLASSIFIÉ</span></div>
          <div style="flex:1;text-align:right;" class="eve-meta">2.4 TB</div>
        </div>
        <div class="eve-row">
          <div style="flex:2;display:flex;align-items:center;">
            <svg class="eve-file-icon" viewBox="0 0 14 14"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#12100a" stroke="#D4AF37" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#D4AF37" stroke-width="0.6" opacity="0.7"/><line x1="3" y1="6" x2="8" y2="6" stroke="#D4AF37" stroke-width="0.6" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#D4AF37" stroke-width="0.6" opacity="0.4"/></svg>

[[ARCHIVES MIO/FR - Journal de bord 02-YC128\|FR - Journal de bord 02-YC128]]

          </div>
          <div style="flex:1;"><span class="eve-badge" style="color:var(--eve-gold);">RESTREINT</span></div>
          <div style="flex:1;text-align:right;" class="eve-meta">02 / YC128</div>
        </div>

      </div>
    </div>

  </div><!-- /two-col -->

  <!-- SÉPARATEUR -->
  <div class="eve-divider"><div class="eve-divider-icon"></div></div>

  <!-- KILLBOARD -->
  <div class="eve-section-label">Combat Registry // Live Feed</div>
  <div class="eve-killboard" id="eve-killboard">
    <div class="eve-killboard-header">
      <div style="display:flex;align-items:center;gap:8px;">
        <span style="width:5px;height:5px;background:var(--eve-red);border-radius:50%;box-shadow:0 0 6px var(--eve-red);display:inline-block;animation:pulseAlert 1.5s infinite alternate;"></span>
        <span style="font-family:var(--font-ui);font-size:10px;color:var(--eve-red);letter-spacing:2px;">BLOOD_TITHE_METRICS // ITHIKA ZORATH</span>
      </div>
      <div style="display:flex;align-items:center;gap:10px;">
        <img src="https://images.evetech.net/characters/2124123129/portrait?size=32" style="width:22px;height:22px;border:1px solid #333;" onerror="this.style.display='none'">
        <a href="https://zkillboard.com/character/2124123129/" target="_blank" style="font-family:var(--font-data);font-size:9px;color:#444;text-decoration:none;letter-spacing:1px;">VIEW ALL →</a>
      </div>
    </div>
    <div style="display:flex;border-bottom:1px solid #111;background:rgba(0,0,0,0.5);">
      <div style="flex:1;padding:10px;text-align:center;border-right:1px solid #111;">
        <div id="kb-kills" style="font-family:var(--font-data);font-size:15px;color:var(--eve-gold);">—</div>
        <div style="font-family:var(--font-ui);font-size:9px;color:#333;margin-top:2px;letter-spacing:2px;">KILLS</div>
      </div>
      <div style="flex:1;padding:10px;text-align:center;border-right:1px solid #111;">
        <div id="kb-losses" style="font-family:var(--font-data);font-size:15px;color:var(--eve-red);">—</div>
        <div style="font-family:var(--font-ui);font-size:9px;color:#333;margin-top:2px;letter-spacing:2px;">PERTES</div>
      </div>
      <div style="flex:1;padding:10px;text-align:center;border-right:1px solid #111;">
        <div id="kb-danger" style="font-family:var(--font-data);font-size:15px;color:var(--eve-cyan);">—</div>
        <div style="font-family:var(--font-ui);font-size:9px;color:#333;margin-top:2px;letter-spacing:2px;">DANGER</div>
      </div>
      <div style="flex:1;padding:10px;text-align:center;">
        <div id="kb-isk" style="font-family:var(--font-data);font-size:15px;color:var(--eve-gold);">—</div>
        <div style="font-family:var(--font-ui);font-size:9px;color:#333;margin-top:2px;letter-spacing:2px;">ISK DÉTRUIT</div>
      </div>
    </div>
    <div id="kb-list" style="min-height:80px;max-height:260px;overflow-y:auto;">
      <div style="text-align:center;padding:30px;font-family:var(--font-data);font-size:10px;color:#2a2a2a;letter-spacing:2px;">⟳ RÉCUPÉRATION DES DONNÉES...</div>
    </div>
  </div>

  <!-- SÉPARATEUR -->
  <div class="eve-divider"><div class="eve-divider-icon"></div></div>

  <!-- EXTERNAL FEEDS -->
  <div class="eve-section-label">External Live Feeds</div>
  <div style="display:flex;gap:16px;flex-wrap:wrap;">
    <a href="https://zkillboard.com/character/2124123129/" target="_blank" class="eve-btn eve-btn-red" style="flex:1;min-width:180px;">
      <span class="eve-btn-label" style="color:var(--eve-red);">Combat Registry</span>
      <span class="eve-btn-title">[ Blood Tithe Metrics ]</span>
    </a>
    <a href="https://abysstracker.com/u/ithika-zorath" target="_blank" class="eve-btn eve-btn-cyan" style="flex:1;min-width:180px;">
      <span class="eve-btn-label" style="color:var(--eve-cyan);">Deadspace Anomalies</span>
      <span class="eve-btn-title">[ Abyssal Telemetry ]</span>
    </a>
  </div>

</div>
</div>
</div>

<script>
(function(){
  const CID = 2124123129;
  function isk(v){if(v>=1e9)return(v/1e9).toFixed(1)+' B';if(v>=1e6)return(v/1e6).toFixed(1)+' M';if(v>=1e3)return(v/1e3).toFixed(1)+' K';return v.toFixed(0);}
  function ago(d){const s=Math.floor((Date.now()-new Date(d))/1000);if(s<60)return s+'s';if(s<3600)return Math.floor(s/60)+'m';if(s<86400)return Math.floor(s/3600)+'h';return Math.floor(s/86400)+'d';}
  function sc(s){if(s>=0.5)return'#4dff91';if(s>=0.1)return'#ff9900';return'#ff4d4d';}

  fetch('https://zkillboard.com/api/stats/characterID/'+CID+'/').then(r=>r.json()).then(s=>{
    document.getElementById('kb-kills').textContent=s.shipsDestroyed||0;
    document.getElementById('kb-losses').textContent=s.shipsLost||0;
    const dr=s.dangerRatio||0;
    document.getElementById('kb-danger').textContent=dr+'%';
    document.getElementById('kb-danger').style.color=dr>50?'#ff4d4d':'#7DF9FF';
    document.getElementById('kb-isk').textContent=isk(s.iskDestroyed||0);
  }).catch(()=>{});

  fetch('https://zkillboard.com/api/kills/characterID/'+CID+'/').then(r=>r.json()).then(kills=>{
    const list=document.getElementById('kb-list');
    if(!Array.isArray(kills)||kills.length===0){list.innerHTML='<div style="text-align:center;padding:30px;font-family:monospace;font-size:10px;color:#1e1e1e;letter-spacing:2px;">// AUCUN ENGAGEMENT ENREGISTRÉ</div>';return;}
    list.innerHTML='';
    kills.slice(0,8).forEach(function(k,i){
      var row=document.createElement('div');
      row.className='eve-kill-row';
      row.style.cssText='display:flex;align-items:center;gap:10px;padding:9px 14px;border-bottom:1px solid rgba(255,255,255,0.03);border-left:3px solid #333;cursor:pointer;animation:fadeSlideIn 0.3s ease '+(i*0.06)+'s both;';
      row.innerHTML='<div class="eve-kill-ship"><img src="https://images.evetech.net/types/670/render?size=64"></div><div style="flex:1;min-width:0;font-family:var(--font-data);font-size:10px;color:#333;letter-spacing:1px;">Loading...</div><div style="font-family:var(--font-data);font-size:9px;color:#D4AF37;padding:1px 5px;border:1px solid #2a2a00;background:rgba(212,175,55,0.05);flex-shrink:0;">KILL</div>';
      row.onclick=function(){window.open('https://zkillboard.com/kill/'+k.killmail_id+'/','_blank');};
      list.appendChild(row);
      fetch('https://esi.evetech.net/latest/killmails/'+k.killmail_id+'/'+k.zkb.hash+'/').then(r=>r.json()).then(function(km){
        Promise.all([
          fetch('https://esi.evetech.net/latest/universe/types/'+km.victim.ship_type_id+'/?language=en').then(r=>r.json()),
          fetch('https://esi.evetech.net/latest/universe/systems/'+km.solar_system_id+'/').then(r=>r.json()),
          km.victim.character_id?fetch('https://esi.evetech.net/latest/characters/'+km.victim.character_id+'/').then(r=>r.json()):Promise.resolve({name:'Unknown'})
        ]).then(function(res){
          var ship=res[0],sys=res[1],vic=res[2];
          var isKill=km.attackers&&km.attackers.some(function(a){return a.character_id===CID;});
          var sec=sys.security_status||0;
          row.querySelector('.eve-kill-ship img').src='https://images.evetech.net/types/'+km.victim.ship_type_id+'/render?size=64';
          row.querySelector('div[style*="flex:1"]').innerHTML=
            '<div style="display:flex;align-items:center;gap:6px;margin-bottom:3px;flex-wrap:wrap;">'+
            '<span style="font-family:Rajdhani,sans-serif;font-size:13px;font-weight:600;color:#e0e0e0;">'+(vic.name||'Unknown')+'</span>'+
            '<span style="font-family:Electrolize,monospace;font-size:10px;color:#444;">—</span>'+
            '<span style="font-family:Rajdhani,sans-serif;font-size:12px;color:#777;">'+(ship.name||'Unknown')+'</span>'+
            '</div>'+
            '<div style="display:flex;align-items:center;gap:8px;flex-wrap:wrap;">'+
            '<span style="font-family:\'Share Tech Mono\',monospace;font-size:10px;color:'+sc(sec)+';">'+sys.name+' ('+sec.toFixed(1)+')</span>'+
            '<span style="font-family:\'Share Tech Mono\',monospace;font-size:10px;color:#D4AF37;">'+isk(k.zkb.totalValue||0)+' ISK</span>'+
            '<span style="font-family:\'Share Tech Mono\',monospace;font-size:10px;color:#333;">'+ago(km.killmail_time)+'</span>'+
            '</div>';
          row.querySelector('div[style*="border:1px solid"]').textContent=isKill?'KILL':'LOSS';
          row.querySelector('div[style*="border:1px solid"]').style.color=isKill?'#D4AF37':'#ff4d4d';
          row.querySelector('div[style*="border:1px solid"]').style.borderColor=isKill?'#2a2a00':'#2a0000';
          row.querySelector('div[style*="border:1px solid"]').style.background=isKill?'rgba(212,175,55,0.05)':'rgba(255,77,77,0.05)';
          row.style.borderLeftColor=isKill?'#D4AF37':'#ff4d4d';
        }).catch(function(){});
      }).catch(function(){});
    });
  }).catch(function(){
    document.getElementById('kb-list').innerHTML='<div style="text-align:center;padding:30px;font-family:monospace;font-size:10px;color:#2a2a2a;letter-spacing:2px;">✗ CONNEXION ÉCHOUÉE // ZKILLBOARD UNREACHABLE</div>';
  });
})();
</script>