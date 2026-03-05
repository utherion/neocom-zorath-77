---
{"dg-publish":true,"permalink":"/neocom-zorath-77/","tags":["gardenEntry"],"created":"2026-02-28T21:09:16.622+01:00"}
---


<style>
@import url('https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Electrolize&family=Share+Tech+Mono&family=Cinzel:wght@400;600;700&display=swap');

/* ── SCOPE TOTAL sous #neocom-root pour ne pas polluer Digital Garden ── */

#neocom-root {
  --g: #C8A84B;
  --g2: #6B5520;
  --g3: rgba(200,168,75,0.12);
  --c: #4FC3F7;
  --c2: #0D2A38;
  --r: #CF3B3B;
  --r2: #FF4444;
  --bg: #060709;
  --bg2: rgba(10,12,18,0.98);
  --b1: #1A1D26;
  --b2: #262930;
  --t1: #D0D0D8;
  --t2: #888A98;
  --t3: #404455;
  --t4: #252730;
  --fu: 'Electrolize', monospace;
  --fd: 'Share Tech Mono', monospace;
  --fl: 'Cinzel', serif;
  --fb: 'Rajdhani', sans-serif;

  all: initial;
  display: block;
  font-family: var(--fb);
  background: var(--bg);
  color: var(--t2);
  max-width: 1080px;
  margin: 0 auto;
  position: relative;
  box-sizing: border-box;
}

#neocom-root *, #neocom-root *::before, #neocom-root *::after {
  box-sizing: border-box;
}

/* BG grid */
#neocom-root::before {
  content: '';
  position: fixed;
  inset: 0;
  background-image:
    linear-gradient(rgba(200,168,75,0.012) 1px, transparent 1px),
    linear-gradient(90deg, rgba(200,168,75,0.012) 1px, transparent 1px);
  background-size: 44px 44px;
  pointer-events: none;
  z-index: 0;
}

/* ── TOP BAR ── */
#neocom-root .topbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 7px 16px;
  background: linear-gradient(180deg, #0E1018, #08090E);
  border: 1px solid var(--b1);
  border-bottom: 2px solid var(--g2);
  gap: 16px;
  flex-wrap: wrap;
  position: relative;
  z-index: 10;
}

#neocom-root .topbar-logo {
  display: flex;
  align-items: center;
  gap: 9px;
  font-family: var(--fl);
  font-size: 10px;
  letter-spacing: 3.5px;
  color: var(--g);
  text-shadow: 0 0 14px rgba(200,168,75,0.35);
  text-transform: uppercase;
}

#neocom-root .topbar-logo img {
  width: 18px;
  height: 18px;
  filter: drop-shadow(0 0 6px rgba(200,168,75,0.7));
}

#neocom-root .topbar-nav {
  display: flex;
  align-items: center;
  gap: 2px;
}

#neocom-root .topbar-nav a {
  padding: 4px 13px;
  font-family: var(--fu);
  font-size: 8px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--t3);
  border: 1px solid transparent;
  transition: all 0.2s;
  text-decoration: none !important;
  cursor: pointer;
}

#neocom-root .topbar-nav a:hover {
  color: var(--t2);
  border-color: var(--b2);
  background: rgba(255,255,255,0.025);
}

#neocom-root .topbar-nav a.active {
  color: var(--g);
  border-color: var(--g2);
  background: var(--g3);
}

#neocom-root .topbar-clock {
  font-family: var(--fd);
  font-size: 9px;
  color: var(--t3);
  letter-spacing: 2px;
  white-space: nowrap;
}

/* ── MAIN WINDOW ── */
#neocom-root .win {
  position: relative;
  background: var(--bg2);
  border: 1px solid var(--b2);
  border-top: 2px solid var(--g2);
  box-shadow: 0 20px 60px rgba(0,0,0,0.95), inset 0 0 80px rgba(0,0,0,0.4);
  overflow: hidden;
  margin-top: 0;
}

/* Corner notch */
#neocom-root .win::before {
  content: '';
  position: absolute;
  top: 0; right: 0;
  border-style: solid;
  border-width: 0 18px 18px 0;
  border-color: transparent var(--g2) transparent transparent;
  z-index: 30;
}

/* CRT scanlines */
#neocom-root .win::after {
  content: '';
  position: absolute;
  inset: 0;
  background: repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(0,0,0,0.055) 2px, rgba(0,0,0,0.055) 4px);
  pointer-events: none;
  z-index: 50;
  opacity: 0.5;
}

/* Win titlebar */
#neocom-root .win-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 8px 16px;
  background: linear-gradient(180deg, #13151E 0%, #09090E 100%);
  border-bottom: 1px solid var(--b1);
  position: relative;
  z-index: 10;
  gap: 12px;
}

#neocom-root .win-bar::after {
  content: '';
  position: absolute;
  bottom: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, var(--g2) 35%, var(--g2) 65%, transparent);
  opacity: 0.45;
}

#neocom-root .win-bar-left {
  display: flex;
  align-items: center;
  gap: 9px;
}

#neocom-root .win-bar-left img {
  width: 16px; height: 16px;
  filter: drop-shadow(0 0 4px rgba(200,168,75,0.5));
}

#neocom-root .win-bar-title {
  font-family: var(--fu);
  font-size: 9px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: #A0A0AE;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

#neocom-root .status-pill {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 3px 10px;
  border: 1px solid rgba(79,195,247,0.18);
  background: rgba(79,195,247,0.03);
  font-family: var(--fd);
  font-size: 8px;
  letter-spacing: 2px;
  color: var(--c);
  flex-shrink: 0;
}

#neocom-root .status-dot {
  width: 5px; height: 5px;
  border-radius: 50%;
  background: var(--c);
  box-shadow: 0 0 6px var(--c);
  animation: nc-blink 1.8s ease-in-out infinite alternate;
}

@keyframes nc-blink {
  from { opacity: 1; box-shadow: 0 0 6px var(--c); }
  to   { opacity: 0.25; box-shadow: none; }
}

/* ── BODY FLEX ── */
#neocom-root .win-body {
  display: flex;
  align-items: stretch;
  position: relative;
  z-index: 1;
  min-height: 400px;
}

/* ── TERMINAL SIDEBAR ── */
#neocom-root .term-col {
  width: 175px;
  flex-shrink: 0;
  background: #000;
  border-right: 1px solid #0C0E14;
  position: relative;
  overflow: hidden;
  height: 100%;
  -webkit-mask-image: linear-gradient(to bottom, transparent 0%, black 6%, black 94%, transparent 100%);
  mask-image: linear-gradient(to bottom, transparent 0%, black 6%, black 94%, transparent 100%);
}

#neocom-root .term-scroll {
  position: absolute;
  top: 0; left: 0; right: 0;
  padding: 14px 12px;
  animation: nc-scroll 20s linear infinite;
}

@keyframes nc-scroll {
  0%   { transform: translateY(0); }
  100% { transform: translateY(-50%); }
}

#neocom-root .tl {
  display: block;
  font-family: var(--fd);
  font-size: 8.5px;
  line-height: 1.75;
  letter-spacing: 0.3px;
  color: rgba(79,195,247,0.45);
  text-shadow: 0 0 4px rgba(79,195,247,0.25);
}
#neocom-root .tl.w { color: rgba(207,59,59,0.65); text-shadow: 0 0 4px rgba(207,59,59,0.25); }
#neocom-root .tl.g { color: rgba(200,168,75,0.65); text-shadow: 0 0 4px rgba(200,168,75,0.25); }
#neocom-root .tl.d { color: rgba(79,195,247,0.18); }

/* ── MAIN CONTENT ── */
#neocom-root .content {
  flex: 1;
  padding: 22px 26px;
  min-width: 0;
  background: radial-gradient(ellipse at 15% 0%, rgba(200,168,75,0.02) 0%, transparent 55%);
}

/* ── SECTION LABEL ── */
#neocom-root .sl {
  display: flex;
  align-items: center;
  gap: 8px;
  font-family: var(--fu);
  font-size: 8.5px;
  letter-spacing: 3.5px;
  text-transform: uppercase;
  color: var(--t3);
  padding-bottom: 7px;
  border-bottom: 1px solid var(--b1);
  margin-bottom: 13px;
}
#neocom-root .sl::before {
  content: '';
  display: inline-block;
  width: 6px; height: 6px;
  background: var(--g2);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
  flex-shrink: 0;
}

/* ── DIVIDER ── */
#neocom-root .divider {
  display: flex;
  align-items: center;
  gap: 10px;
  margin: 18px 0;
}
#neocom-root .divider::before { content: ''; flex: 1; height: 1px; background: linear-gradient(90deg, transparent, var(--b2)); }
#neocom-root .divider::after  { content: ''; flex: 1; height: 1px; background: linear-gradient(90deg, var(--b2), transparent); }
#neocom-root .divider-gem {
  width: 6px; height: 6px;
  background: var(--g2);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
}

/* ── NEURAL SYNC ── */
#neocom-root .sync {
  position: relative;
  border: 1px solid #141C28;
  background: rgba(0,6,16,0.55);
  padding: 9px 13px 18px;
  margin-bottom: 18px;
  font-family: var(--fd);
  font-size: 8.5px;
  letter-spacing: 1.5px;
  color: var(--t4);
  overflow: hidden;
}
#neocom-root .sync::before {
  content: '';
  position: absolute;
  top: 0; left: 0;
  border-style: solid;
  border-width: 9px 9px 0 0;
  border-color: var(--c2) transparent transparent transparent;
}
#neocom-root .sync-hd {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 7px;
}
#neocom-root .sync-cmd { color: var(--c2); }
#neocom-root .sync-status { position: relative; height: 13px; width: 210px; }
#neocom-root .sync-wait {
  position: absolute; right: 0; top: 0;
  color: var(--g);
  text-shadow: 0 0 5px rgba(200,168,75,0.4);
  animation: nc-fadeout 2.4s ease forwards;
}
#neocom-root .sync-ok {
  position: absolute; right: 0; top: 0;
  color: var(--c);
  text-shadow: 0 0 5px rgba(79,195,247,0.5);
  opacity: 0;
  animation: nc-fadein 2.4s ease forwards;
}
@keyframes nc-fadeout { 0%,75%{opacity:1}100%{opacity:0} }
@keyframes nc-fadein  { 0%,75%{opacity:0}100%{opacity:1} }

#neocom-root .sync-track {
  height: 2px;
  background: #060C18;
  overflow: hidden;
}
#neocom-root .sync-fill {
  height: 100%;
  width: 0;
  background: linear-gradient(90deg, transparent, var(--c) 60%, rgba(79,195,247,0.3));
  box-shadow: 0 0 8px var(--c);
  animation: nc-fill 2s ease-out forwards;
}
@keyframes nc-fill { 0%{width:0} 100%{width:100%} }

#neocom-root .sync-wf {
  position: absolute;
  bottom: 5px; right: 10px;
  display: flex;
  align-items: flex-end;
  gap: 2px;
  height: 11px;
}
#neocom-root .wfb {
  width: 2px;
  background: var(--c);
  box-shadow: 0 0 3px var(--c);
  border-radius: 1px;
}

/* ── ALERT ── */
#neocom-root .alert {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 14px;
  padding: 11px 15px;
  border-left: 3px solid var(--r);
  background: rgba(18,0,0,0.5);
  margin-bottom: 18px;
  animation: nc-alert 2.8s ease-in-out infinite;
}
@keyframes nc-alert {
  0%,100% { background:rgba(18,0,0,0.5); border-left-color:var(--r); box-shadow:none; }
  50%      { background:rgba(36,0,0,0.7); border-left-color:var(--r2); box-shadow:inset 0 0 18px rgba(207,59,59,0.12), 0 0 10px rgba(207,59,59,0.08); }
}
#neocom-root .alert-title {
  display: flex;
  align-items: center;
  gap: 7px;
  font-family: var(--fu);
  font-size: 9px;
  letter-spacing: 3px;
  color: var(--r2);
  text-transform: uppercase;
  margin-bottom: 5px;
}
#neocom-root .alert-body {
  font-family: var(--fb);
  font-size: 13px;
  color: #A8A8B0;
  line-height: 1.4;
  margin: 0;
}
#neocom-root .alert img {
  filter: drop-shadow(0 0 12px rgba(207,59,59,0.8));
  flex-shrink: 0;
}

/* ── BIO CARD ── */
#neocom-root .bio {
  display: flex;
  border: 1px solid var(--b2);
  border-top: 2px solid var(--g2);
  background: rgba(0,0,0,0.5);
  margin-bottom: 18px;
  overflow: hidden;
}
#neocom-root .bio-port {
  position: relative;
  width: 175px;
  height: 175px;
  flex-shrink: 0;
  background: #000;
  overflow: hidden;
  border-right: 1px solid #181400;
}
#neocom-root .bio-port img {
  width: 100%; height: 100%;
  object-fit: cover;
  object-position: top center;
  display: block;
}
#neocom-root .bio-scan {
  position: absolute;
  left: 0; width: 100%; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(79,195,247,0.7) 40%, rgba(255,255,255,0.85) 50%, rgba(79,195,247,0.7) 60%, transparent);
  box-shadow: 0 0 8px rgba(79,195,247,0.5), 0 -3px 6px rgba(79,195,247,0.15), 0 3px 6px rgba(79,195,247,0.15);
  animation: nc-scan 3.2s cubic-bezier(0.4,0,0.2,1) infinite;
  z-index: 10;
}
@keyframes nc-scan {
  0%  {top:0%;opacity:0}
  5%  {opacity:1}
  95% {opacity:1}
  100%{top:100%;opacity:0}
}
#neocom-root .bio-grad {
  position: absolute;
  bottom: 0; left: 0; right: 0; height: 50px;
  background: linear-gradient(transparent, rgba(0,0,0,0.95));
  z-index: 5;
}
#neocom-root .bio-lbl {
  position: absolute;
  bottom: 5px; left: 8px;
  font-family: var(--fd);
  font-size: 7px;
  color: rgba(107,85,32,0.75);
  letter-spacing: 2px;
  z-index: 15;
}
#neocom-root .bio-data {
  padding: 14px 20px;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
#neocom-root .bio-data-title {
  font-family: var(--fl);
  font-size: 7.5px;
  letter-spacing: 4px;
  color: var(--g);
  text-transform: uppercase;
  border-bottom: 1px solid rgba(200,168,75,0.1);
  padding-bottom: 7px;
  margin-bottom: 9px;
  opacity: 0.75;
}
#neocom-root .bio-table {
  width: 100%;
  border-collapse: collapse;
}
#neocom-root .bio-table tr {
  border-bottom: 1px solid rgba(200,168,75,0.05);
}
#neocom-root .bio-table tr:last-child { border-bottom: none; }
#neocom-root .bio-table td {
  padding: 5px 0;
  border: none;
  vertical-align: middle;
}
#neocom-root .bio-table .k {
  font-family: var(--fu);
  font-size: 7.5px;
  letter-spacing: 2px;
  color: var(--t3);
  text-transform: uppercase;
  width: 105px;
  white-space: nowrap;
}
#neocom-root .bio-table .vn {
  font-family: var(--fb);
  font-size: 20px;
  font-weight: 700;
  color: #EBEBF0;
  letter-spacing: 0.5px;
}
#neocom-root .bio-table .vt {
  font-family: var(--fd);
  font-size: 11px;
  color: var(--c);
}
#neocom-root .bio-table .vt span { color: rgba(79,195,247,0.3); margin-left: 5px; }
#neocom-root .bio-table .vd { font-family: var(--fb); font-size: 13px; color: #808090; }
#neocom-root .bio-table .vg { font-family: var(--fl); font-size: 13px; color: var(--g); }
#neocom-root .bio-table .vm { font-family: var(--fd); font-size: 10px; color: var(--t3); letter-spacing: 1px; }

/* ── INDEX ── */
#neocom-root .idx {
  border: 1px solid var(--b2);
  background: rgba(0,0,0,0.62);
  margin-bottom: 18px;
  overflow: hidden;
}
#neocom-root .idx-lh {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 5px 13px;
  background: linear-gradient(90deg, rgba(200,168,75,0.07), rgba(200,168,75,0.015) 70%, transparent);
  border-bottom: 1px solid rgba(200,168,75,0.12);
  font-family: var(--fu);
  font-size: 8.5px;
  letter-spacing: 3px;
  color: var(--g);
}
#neocom-root .idx-lh .gem {
  width: 6px; height: 6px;
  background: var(--g2);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
}
#neocom-root .idx-fh {
  display: flex;
  align-items: center;
  gap: 7px;
  padding: 5px 13px 5px 18px;
  border-bottom: 1px solid rgba(255,255,255,0.035);
  background: rgba(255,255,255,0.004);
  font-family: var(--fu);
  font-size: 9px;
  letter-spacing: 2px;
  color: var(--t3);
  text-transform: uppercase;
}
#neocom-root .idx-row {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 8px 13px 8px 28px;
  border-bottom: 1px solid rgba(255,255,255,0.022);
  border-left: 3px solid transparent;
  cursor: pointer;
  transition: background 0.15s, border-left-color 0.15s;
  text-decoration: none !important;
  color: inherit;
}
#neocom-root .idx-row:hover {
  background: rgba(79,195,247,0.022);
  border-left-color: rgba(79,195,247,0.28);
}
#neocom-root .idx-row:last-child { border-bottom: none; }
#neocom-root .idx-name {
  flex: 1;
  font-family: var(--fb);
  font-size: 13px;
  color: #B8B8C4;
  text-decoration: none !important;
}
#neocom-root .idx-row:hover .idx-name { color: var(--c); }
#neocom-root .badge {
  font-family: var(--fd);
  font-size: 7.5px;
  letter-spacing: 1.5px;
  padding: 2px 6px;
  white-space: nowrap;
}
#neocom-root .badge.r { border: 1px solid var(--r); color: var(--r); }
#neocom-root .badge.g { border: 1px solid var(--g2); color: var(--g); }
#neocom-root .idx-meta {
  font-family: var(--fd);
  font-size: 8.5px;
  color: var(--t3);
  letter-spacing: 1px;
  text-align: right;
  white-space: nowrap;
  min-width: 65px;
}
#neocom-root .idx-sep { border-top: 1px solid rgba(200,168,75,0.08); }

/* ── KILLBOARD ── */
#neocom-root .kb {
  border: 1px solid var(--b2);
  background: rgba(0,0,0,0.58);
  margin-bottom: 18px;
  overflow: hidden;
}
#neocom-root .kb-hd {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 7px 13px;
  background: linear-gradient(90deg, rgba(207,59,59,0.07), transparent);
  border-bottom: 1px solid rgba(207,59,59,0.12);
  gap: 10px;
}
#neocom-root .kb-hd-l { display: flex; align-items: center; gap: 7px; }
#neocom-root .kb-dot {
  width: 5px; height: 5px;
  border-radius: 50%;
  background: var(--r2);
  box-shadow: 0 0 5px var(--r2);
  animation: nc-blink-r 1.5s ease-in-out infinite alternate;
}
@keyframes nc-blink-r {
  from { opacity:1; box-shadow:0 0 5px var(--r2); }
  to   { opacity:0.2; box-shadow:none; }
}
#neocom-root .kb-title {
  font-family: var(--fu);
  font-size: 8.5px;
  letter-spacing: 2px;
  color: var(--r2);
  text-transform: uppercase;
}
#neocom-root .kb-hd-r { display: flex; align-items: center; gap: 9px; }
#neocom-root .kb-hd-r img { border: 1px solid #1A1A1A; }
#neocom-root .kb-hd-r a {
  font-family: var(--fd);
  font-size: 8px;
  color: var(--t3);
  text-decoration: none !important;
  letter-spacing: 1px;
}
#neocom-root .kb-hd-r a:hover { color: var(--t2); }

#neocom-root .kb-stats {
  display: flex;
  background: rgba(0,0,0,0.38);
  border-bottom: 1px solid var(--b1);
}
#neocom-root .kb-stat {
  flex: 1;
  text-align: center;
  padding: 9px 6px;
  border-right: 1px solid var(--b1);
}
#neocom-root .kb-stat:last-child { border-right: none; }
#neocom-root .kb-sv {
  display: block;
  font-family: var(--fd);
  font-size: 15px;
  margin-bottom: 2px;
}
#neocom-root .kb-sv.g  { color: var(--g); }
#neocom-root .kb-sv.r  { color: var(--r2); }
#neocom-root .kb-sv.c  { color: var(--c); }
#neocom-root .kb-sl {
  display: block;
  font-family: var(--fu);
  font-size: 7.5px;
  letter-spacing: 2px;
  color: var(--t3);
  text-transform: uppercase;
}

#neocom-root .kb-list {
  max-height: 270px;
  overflow-y: auto;
}
#neocom-root .kb-list::-webkit-scrollbar { width: 3px; }
#neocom-root .kb-list::-webkit-scrollbar-track { background: #000; }
#neocom-root .kb-list::-webkit-scrollbar-thumb { background: var(--b2); }

#neocom-root .kb-row {
  display: flex;
  align-items: center;
  gap: 9px;
  padding: 7px 13px;
  border-bottom: 1px solid rgba(255,255,255,0.025);
  border-left: 3px solid var(--b1);
  cursor: pointer;
  transition: background 0.15s;
  animation: nc-fadeslide 0.3s ease both;
}
#neocom-root .kb-row:hover { background: rgba(200,168,75,0.025); }
#neocom-root .kb-row:last-child { border-bottom: none; }

@keyframes nc-fadeslide {
  from { opacity:0; transform:translateX(-4px); }
  to   { opacity:1; transform:translateX(0); }
}

#neocom-root .kb-thumb {
  width: 36px; height: 36px;
  flex-shrink: 0;
  border: 1px solid #181818;
  background: #000;
  overflow: hidden;
}
#neocom-root .kb-thumb img { width:100%; height:100%; display:block; object-fit:cover; }

#neocom-root .kb-info { flex:1; min-width:0; }
#neocom-root .kb-vname {
  font-family: var(--fb);
  font-size: 13px;
  font-weight: 600;
  color: #D8D8E0;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
#neocom-root .kb-sub {
  font-family: var(--fd);
  font-size: 8.5px;
  margin-top: 2px;
  display: flex;
  gap: 9px;
  flex-wrap: wrap;
}
#neocom-root .kb-sub .isk  { color: var(--g); }
#neocom-root .kb-sub .time { color: var(--t3); }

#neocom-root .kb-badge {
  font-family: var(--fd);
  font-size: 7.5px;
  letter-spacing: 1.5px;
  padding: 2px 6px;
  flex-shrink: 0;
}
#neocom-root .kb-badge.kill { color:var(--g);  border:1px solid rgba(200,168,75,0.28); background:rgba(200,168,75,0.03); }
#neocom-root .kb-badge.loss { color:var(--r2); border:1px solid rgba(207,59,59,0.28);  background:rgba(207,59,59,0.03); }

#neocom-root .kb-empty {
  text-align: center;
  padding: 28px;
  font-family: var(--fd);
  font-size: 8.5px;
  color: var(--t4);
  letter-spacing: 3px;
}

/* ── FEEDS ── */
#neocom-root .feeds { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }

#neocom-root .feed-btn {
  display: block;
  padding: 13px 15px;
  border: 1px solid var(--b2);
  background: rgba(5,6,10,0.9);
  text-decoration: none !important;
  position: relative;
  overflow: hidden;
  transition: all 0.25s;
  clip-path: polygon(0 0, calc(100% - 9px) 0, 100% 9px, 100% 100%, 9px 100%, 0 calc(100% - 9px));
}
#neocom-root .feed-btn::before {
  content: '';
  position: absolute;
  top: 0; left: -100%;
  width: 100%; height: 1px;
  transition: left 0.35s;
}
#neocom-root .feed-btn:hover::before { left: 100%; }
#neocom-root .feed-btn.fr { border-top-color:#3A1515; border-bottom-color:#3A1515; }
#neocom-root .feed-btn.fr:hover { border-color:rgba(207,59,59,0.45); background:rgba(207,59,59,0.035); }
#neocom-root .feed-btn.fr::before { background:linear-gradient(90deg,transparent,rgba(207,59,59,0.35),transparent); }
#neocom-root .feed-btn.fc { border-top-color:#0A1E28; border-bottom-color:#0A1E28; }
#neocom-root .feed-btn.fc:hover { border-color:rgba(79,195,247,0.38); background:rgba(79,195,247,0.035); }
#neocom-root .feed-btn.fc::before { background:linear-gradient(90deg,transparent,rgba(79,195,247,0.35),transparent); }

#neocom-root .feed-sub {
  display: block;
  font-family: var(--fu);
  font-size: 8px;
  letter-spacing: 3px;
  text-transform: uppercase;
  margin-bottom: 5px;
  opacity: 0.65;
}
#neocom-root .feed-btn.fr .feed-sub { color: var(--r2); }
#neocom-root .feed-btn.fc .feed-sub { color: var(--c); }
#neocom-root .feed-title {
  display: block;
  font-family: var(--fl);
  font-size: 11px;
  letter-spacing: 2px;
  font-weight: 600;
  color: #CCCCDA;
}

/* ── FOOTER ── */
#neocom-root .footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 7px 15px;
  border: 1px solid var(--b1);
  border-top: 1px solid var(--b2);
  background: rgba(0,0,0,0.55);
  margin-top: 18px;
}
#neocom-root .footer span {
  font-family: var(--fd);
  font-size: 7.5px;
  letter-spacing: 2px;
  color: var(--t4);
}

/* ── RESPONSIVE ── */
@media (max-width: 700px) {
  #neocom-root .win-body { flex-direction: column; }
  #neocom-root .term-col { width:100%; height:70px; border-right:none; border-bottom:1px solid var(--b1); }
  #neocom-root .content { padding:14px; }
  #neocom-root .bio { flex-direction:column; }
  #neocom-root .bio-port { width:100%; height:140px; }
  #neocom-root .feeds { grid-template-columns:1fr; }
  #neocom-root .topbar { flex-direction:column; gap:6px; }
  #neocom-root .topbar-nav { flex-wrap:wrap; }
}
</style>

<div id="neocom-root">

<!-- TOP BAR -->
<div class="topbar">
  <div class="topbar-logo">
    <img src="https://image.eveonline.com/Corporation/1000082_128.png" alt="MIO">
    MIO &nbsp;//&nbsp; Secure Info Terminal &nbsp;//&nbsp; Node 77-A
  </div>
  <nav class="topbar-nav">
    <a href="#" class="active">Character</a>
    <a href="#" >Archives</a>
    <a href="#">Combat</a>
    <a href="#">Feeds</a>
  </nav>
  <div class="topbar-clock" id="nc-clock">YC128 // --:--:-- UTC</div>
</div>

<!-- MAIN WINDOW -->
<div class="win">

  <!-- Titlebar -->
  <div class="win-bar">
    <div class="win-bar-left">
      <img src="https://image.eveonline.com/Corporation/1000082_128.png" alt="">
      <span class="win-bar-title">MIO // Secure_Info_Terminal // Node 77-A // Access Level: ALPHA-CLEAR</span>
    </div>
    <div class="status-pill">
      <span class="status-dot"></span>
      LINK SECURE
    </div>
  </div>

  <!-- Body -->
  <div class="win-body">

    <!-- Terminal sidebar -->
    <div class="term-col">
      <div class="term-scroll">
        <span class="tl">&gt; CONNECTING_TO_NODE_77-A...</span>
        <span class="tl">&gt; ESTABLISHING_NEURAL_LINK...</span>
        <span class="tl">&gt; AUTH_REQUEST_SENT...</span>
        <span class="tl w">* WAITING_FOR_RESPONSE *</span>
        <span class="tl">&gt; MIO_AUTH_RECEIVED...</span>
        <span class="tl">&gt; SECURE_CHANNEL_ALPHA-7</span>
        <span class="tl d">ANALYZING_FIREWALL_3...</span>
        <span class="tl">&gt; INJECTING_EXPLOIT...</span>
        <span class="tl">&gt; FIREWALL_BYPASSED...</span>
        <span class="tl w">&gt; WARNING:ELEVATION!</span>
        <span class="tl w">&gt; WARNING:ELEVATION!</span>
        <span class="tl">&gt; RE-ROUTING_TRACE...</span>
        <span class="tl d">PACKET_SNIFFING_ON...</span>
        <span class="tl">&gt; EXTRACTING_SIG...</span>
        <span class="tl g">&gt; SUCCESS_ID:ZORATH</span>
        <span class="tl w">&gt; TRACE_INBOUND!</span>
        <span class="tl w">&gt; MIO_PURGE_INIT *</span>
        <span class="tl">&gt; BREACH_SECTOR-G</span>
        <span class="tl d">DATA_MINING_ACTIVE</span>
        <span class="tl">&gt; REBOOT_SEQ_7722</span>
        <span class="tl">&gt; MEMORY_WIPE_OK</span>
        <span class="tl d">SIG_VERIFY_LOOP...</span>
        <span class="tl">&gt; NODE_77A_ALIVE</span>
        <!-- duplicate for seamless loop -->
        <span class="tl">&gt; CONNECTING_TO_NODE_77-A...</span>
        <span class="tl">&gt; ESTABLISHING_NEURAL_LINK...</span>
        <span class="tl">&gt; AUTH_REQUEST_SENT...</span>
        <span class="tl w">* WAITING_FOR_RESPONSE *</span>
        <span class="tl">&gt; MIO_AUTH_RECEIVED...</span>
        <span class="tl">&gt; SECURE_CHANNEL_ALPHA-7</span>
        <span class="tl d">ANALYZING_FIREWALL_3...</span>
        <span class="tl">&gt; INJECTING_EXPLOIT...</span>
        <span class="tl">&gt; FIREWALL_BYPASSED...</span>
        <span class="tl w">&gt; WARNING:ELEVATION!</span>
        <span class="tl w">&gt; WARNING:ELEVATION!</span>
        <span class="tl">&gt; RE-ROUTING_TRACE...</span>
        <span class="tl d">PACKET_SNIFFING_ON...</span>
        <span class="tl">&gt; EXTRACTING_SIG...</span>
        <span class="tl g">&gt; SUCCESS_ID:ZORATH</span>
        <span class="tl w">&gt; TRACE_INBOUND!</span>
        <span class="tl w">&gt; MIO_PURGE_INIT *</span>
        <span class="tl">&gt; BREACH_SECTOR-G</span>
        <span class="tl d">DATA_MINING_ACTIVE</span>
        <span class="tl">&gt; REBOOT_SEQ_7722</span>
        <span class="tl">&gt; MEMORY_WIPE_OK</span>
        <span class="tl d">SIG_VERIFY_LOOP...</span>
        <span class="tl">&gt; NODE_77A_ALIVE</span>
      </div>
    </div>

    <!-- Content -->
    <div class="content">

      <!-- Neural Sync -->
      <div class="sync">
        <div class="sync-hd">
          <span class="sync-cmd">&gt; INITIALIZING NEURAL PATHWAYS...</span>
          <div class="sync-status">
            <span class="sync-wait">SCANNING PILOT SIGNATURE [ WAIT ]</span>
            <span class="sync-ok">SIGNATURE MATCHED [ SYNC 100% ]</span>
          </div>
        </div>
        <div class="sync-track"><div class="sync-fill"></div></div>
        <div class="sync-wf" id="nc-wf"></div>
      </div>

      <!-- Alert -->
      <div class="alert">
        <div>
          <div class="alert-title">
            <svg width="13" height="13" viewBox="0 0 16 16" fill="none">
              <path d="M8 1.5L14.5 13.5H1.5L8 1.5Z" stroke="#FF4444" stroke-width="1.2" fill="rgba(255,68,68,0.1)"/>
              <line x1="8" y1="6" x2="8" y2="10" stroke="#FF4444" stroke-width="1.5"/>
              <circle cx="8" cy="12" r="0.9" fill="#FF4444"/>
            </svg>
            RESTRICTED ACCESS PROTOCOL
          </div>
          <p class="alert-body">Monitoring active. Any synaptic deviation is logged by the Ministry of Internal Order.</p>
        </div>
        <img src="https://image.eveonline.com/Corporation/1000082_128.png" width="46" height="46" alt="MIO">
      </div>

      <!-- Biometric -->
      <div class="sl">Biometric Data</div>
      <div class="bio">
        <div class="bio-port">
          <div class="bio-scan"></div>
          <img src="https://images.evetech.net/characters/2124123129/portrait?size=512" alt="Ithika Zorath">
          <div class="bio-grad"></div>
          <div class="bio-lbl">MIO // CAPSULEER</div>
        </div>
        <div class="bio-data">
          <div class="bio-data-title">Identification Records</div>
          <table class="bio-table">
            <tr><td class="k">Designation</td><td class="vn">Ithika Zorath</td></tr>
            <tr><td class="k">Bio-Tech</td><td class="vt">Capsuleer <span>[ ACTIVE ]</span></td></tr>
            <tr><td class="k">Origin</td><td class="vd">Nafomeh III</td></tr>
            <tr><td class="k">Allegiance</td><td class="vg">House Tash-Murkon</td></tr>
            <tr><td class="k">Timestamp</td><td class="vm">YC128.02</td></tr>
          </table>
        </div>
      </div>

      <!-- Index Manager -->
      <div class="sl">Index Manager</div>
      <div class="idx">

        <!-- EN -->
        <div class="idx-lh"><span class="gem"></span>SYS.LANG // ENGLISH</div>
        <div class="idx-fh">
          <svg width="11" height="11" viewBox="0 0 14 14"><path d="M1 3.5L1 12L13 12L13 3.5L7 3.5L6 1.5L1 1.5Z" fill="#141418" stroke="#2A2D38" stroke-width="0.8"/></svg>
          MIO Archives
        </div>
        <a href="/notes/en-archives-of-house-tash-murkon" class="idx-row">
          <svg width="12" height="12" viewBox="0 0 14 14"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#061420" stroke="#4FC3F7" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#4FC3F7" stroke-width="0.6" opacity="0.7"/><line x1="3" y1="6" x2="8" y2="6" stroke="#4FC3F7" stroke-width="0.5" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#4FC3F7" stroke-width="0.5" opacity="0.4"/></svg>
          <span class="idx-name">EN — ARCHIVES OF HOUSE TASH-MURKON</span>
          <span class="badge r">CLASSIFIED</span>
          <span class="idx-meta">2.4 TB</span>
        </a>
        <a href="/notes/en-logbook-02-yc128" class="idx-row">
          <svg width="12" height="12" viewBox="0 0 14 14"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#100E04" stroke="#C8A84B" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#C8A84B" stroke-width="0.6" opacity="0.7"/><line x1="3" y1="6" x2="8" y2="6" stroke="#C8A84B" stroke-width="0.5" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#C8A84B" stroke-width="0.5" opacity="0.4"/></svg>
          <span class="idx-name">EN — Logbook 02-YC128</span>
          <span class="badge g">RESTRICTED</span>
          <span class="idx-meta">02 / YC128</span>
        </a>

        <!-- FR -->
        <div class="idx-lh idx-sep"><span class="gem"></span>SYS.LANG // FRANÇAIS</div>
        <div class="idx-fh">
          <svg width="11" height="11" viewBox="0 0 14 14"><path d="M1 3.5L1 12L13 12L13 3.5L7 3.5L6 1.5L1 1.5Z" fill="#141418" stroke="#2A2D38" stroke-width="0.8"/></svg>
          Archives MIO
        </div>
        <a href="/notes/fr-archives-of-house-tash-murkon" class="idx-row">
          <svg width="12" height="12" viewBox="0 0 14 14"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#061420" stroke="#4FC3F7" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#4FC3F7" stroke-width="0.6" opacity="0.7"/><line x1="3" y1="6" x2="8" y2="6" stroke="#4FC3F7" stroke-width="0.5" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#4FC3F7" stroke-width="0.5" opacity="0.4"/></svg>
          <span class="idx-name">FR — ARCHIVES OF HOUSE TASH-MURKON</span>
          <span class="badge r">CLASSIFIÉ</span>
          <span class="idx-meta">2.4 TB</span>
        </a>
        <a href="/notes/fr-journal-de-bord-02-yc128" class="idx-row">
          <svg width="12" height="12" viewBox="0 0 14 14"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#100E04" stroke="#C8A84B" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#C8A84B" stroke-width="0.6" opacity="0.7"/><line x1="3" y1="6" x2="8" y2="6" stroke="#C8A84B" stroke-width="0.5" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#C8A84B" stroke-width="0.5" opacity="0.4"/></svg>
          <span class="idx-name">FR — Journal de bord 02-YC128</span>
          <span class="badge g">RESTREINT</span>
          <span class="idx-meta">02 / YC128</span>
        </a>

      </div>

      <div class="divider"><div class="divider-gem"></div></div>

      <!-- Killboard -->
      <div class="sl">Combat Registry // Live Feed</div>
      <div class="kb">
        <div class="kb-hd">
          <div class="kb-hd-l">
            <span class="kb-dot"></span>
            <span class="kb-title">Blood_Tithe_Metrics // Ithika Zorath</span>
          </div>
          <div class="kb-hd-r">
            <img src="https://images.evetech.net/characters/2124123129/portrait?size=32" width="20" height="20" alt="">
            <a href="https://zkillboard.com/character/2124123129/" target="_blank">VIEW ALL →</a>
          </div>
        </div>
        <div class="kb-stats">
          <div class="kb-stat"><span class="kb-sv g" id="nc-kills">—</span><span class="kb-sl">Kills</span></div>
          <div class="kb-stat"><span class="kb-sv r" id="nc-losses">—</span><span class="kb-sl">Losses</span></div>
          <div class="kb-stat"><span class="kb-sv c" id="nc-danger">—</span><span class="kb-sl">Danger</span></div>
          <div class="kb-stat"><span class="kb-sv g" id="nc-isk">—</span><span class="kb-sl">ISK Destroyed</span></div>
        </div>
        <div class="kb-list" id="nc-kblist">
          <div class="kb-empty">⟳ RETRIEVING DATA...</div>
        </div>
      </div>

      <div class="divider"><div class="divider-gem"></div></div>

      <!-- External Feeds -->
      <div class="sl">External Live Feeds</div>
      <div class="feeds">
        <a href="https://zkillboard.com/character/2124123129/" target="_blank" class="feed-btn fr">
          <span class="feed-sub">Combat Registry</span>
          <span class="feed-title">[ Blood Tithe Metrics ]</span>
        </a>
        <a href="https://abysstracker.com/u/ithika-zorath" target="_blank" class="feed-btn fc">
          <span class="feed-sub">Deadspace Anomalies</span>
          <span class="feed-title">[ Abyssal Telemetry ]</span>
        </a>
      </div>

      <!-- Footer -->
      <div class="footer">
        <span>MIO // SECURE TERMINAL // NODE 77-A // ACCESS ALPHA-CLEAR</span>
        <span>YC128.02 — ITHIKA ZORATH</span>
      </div>

    </div><!-- /content -->
  </div><!-- /win-body -->
</div><!-- /win -->
</div><!-- /neocom-root -->

<script>
(function(){
  /* Clock */
  function eveTime(){
    var n=new Date(),h=String(n.getUTCHours()).padStart(2,'0'),m=String(n.getUTCMinutes()).padStart(2,'0'),s=String(n.getUTCSeconds()).padStart(2,'0');
    return 'YC128 // '+h+':'+m+':'+s+' UTC';
  }
  var clk=document.getElementById('nc-clock');
  if(clk){setInterval(function(){clk.textContent=eveTime();},1000);clk.textContent=eveTime();}

  /* Waveform */
  var wf=document.getElementById('nc-wf');
  if(wf){
    var st=document.createElement('style');
    st.textContent='@keyframes ncwv{from{height:15%}to{height:100%}}';
    document.head.appendChild(st);
    [0.6,0.8,0.5,0.9,0.7,0.55,0.75].forEach(function(sp,i){
      var b=document.createElement('div');
      b.className='wfb';
      b.style.cssText='animation:ncwv '+sp+'s ease-in-out '+(i*0.12)+'s infinite alternate;height:15%';
      wf.appendChild(b);
    });
  }

  /* Killboard */
  var CID=2124123129;
  function isk(v){if(v>=1e9)return(v/1e9).toFixed(1)+' B';if(v>=1e6)return(v/1e6).toFixed(1)+' M';if(v>=1e3)return(v/1e3).toFixed(1)+' K';return v.toFixed(0);}
  function ago(d){var s=Math.floor((Date.now()-new Date(d))/1000);if(s<60)return s+'s';if(s<3600)return Math.floor(s/60)+'m';if(s<86400)return Math.floor(s/3600)+'h';return Math.floor(s/86400)+'d';}
  function scolor(s){return s>=0.5?'#4FC870':s>=0.1?'#E8A020':'#CF3B3B';}

  fetch('https://zkillboard.com/api/stats/characterID/'+CID+'/')
    .then(function(r){return r.json();})
    .then(function(s){
      document.getElementById('nc-kills').textContent=s.shipsDestroyed||0;
      document.getElementById('nc-losses').textContent=s.shipsLost||0;
      var dr=s.dangerRatio||0;
      var de=document.getElementById('nc-danger');
      de.textContent=dr+'%';
      de.style.color=dr>50?'#CF3B3B':'#4FC3F7';
      document.getElementById('nc-isk').textContent=isk(s.iskDestroyed||0);
    }).catch(function(){});

  fetch('https://zkillboard.com/api/kills/characterID/'+CID+'/')
    .then(function(r){return r.json();})
    .then(function(kills){
      var list=document.getElementById('nc-kblist');
      if(!Array.isArray(kills)||!kills.length){list.innerHTML='<div class="kb-empty">// NO ENGAGEMENTS RECORDED</div>';return;}
      list.innerHTML='';
      kills.slice(0,8).forEach(function(k,i){
        var row=document.createElement('div');
        row.className='kb-row';
        row.style.animationDelay=(i*0.07)+'s';
        row.style.borderLeftColor='#1A1D26';
        row.innerHTML='<div class="kb-thumb"><img src="https://images.evetech.net/types/670/render?size=64" alt=""></div><div class="kb-info"><div class="kb-vname" style="color:#484858;">Loading...</div></div><span class="kb-badge kill">KILL</span>';
        row.addEventListener('click',function(){window.open('https://zkillboard.com/kill/'+k.killmail_id+'/','_blank');});
        list.appendChild(row);

        fetch('https://esi.evetech.net/latest/killmails/'+k.killmail_id+'/'+k.zkb.hash+'/')
          .then(function(r){return r.json();})
          .then(function(km){
            return Promise.all([
              fetch('https://esi.evetech.net/latest/universe/types/'+km.victim.ship_type_id+'/?language=en').then(function(r){return r.json();}),
              fetch('https://esi.evetech.net/latest/universe/systems/'+km.solar_system_id+'/').then(function(r){return r.json();}),
              km.victim.character_id?fetch('https://esi.evetech.net/latest/characters/'+km.victim.character_id+'/').then(function(r){return r.json();}):Promise.resolve({name:'Unknown'})
            ]).then(function(res){
              var ship=res[0],sys=res[1],vic=res[2];
              var isKill=km.attackers&&km.attackers.some(function(a){return a.character_id===CID;});
              var sec=sys.security_status||0;
              row.querySelector('.kb-thumb img').src='https://images.evetech.net/types/'+km.victim.ship_type_id+'/render?size=64';
              row.querySelector('.kb-info').innerHTML=
                '<div class="kb-vname">'+(vic.name||'Unknown')+'<span style="font-size:11px;color:#404450;font-family:Rajdhani,sans-serif;"> — '+(ship.name||'?')+'</span></div>'+
                '<div class="kb-sub"><span style="color:'+scolor(sec)+';">'+sys.name+' ('+sec.toFixed(1)+')</span><span class="isk">'+isk(k.zkb.totalValue||0)+' ISK</span><span class="time">'+ago(km.killmail_time)+'</span></div>';
              var b=row.querySelector('.kb-badge');
              if(isKill){b.textContent='KILL';b.className='kb-badge kill';row.style.borderLeftColor='rgba(200,168,75,0.45)';}
              else{b.textContent='LOSS';b.className='kb-badge loss';row.style.borderLeftColor='rgba(207,59,59,0.45)';}
            });
          }).catch(function(){});
      });
    }).catch(function(){
      document.getElementById('nc-kblist').innerHTML='<div class="kb-empty">✗ CONNECTION FAILED</div>';
    });
})();
</script>