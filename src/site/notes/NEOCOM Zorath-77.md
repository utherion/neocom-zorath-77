---
{"dg-publish":true,"permalink":"/neocom-zorath-77/","tags":["gardenEntry"],"created":"2026-02-28T21:09:16.622+01:00"}
---

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NEOCOM // ITHIKA ZORATH // NODE 77-A</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Electrolize&family=Share+Tech+Mono&family=Cinzel:wght@400;600;700&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════════════════
   EVE ONLINE NEOCOM — ITHIKA ZORATH — NODE 77-A
   Production-grade faithful UI recreation
═══════════════════════════════════════════════ */

:root {
  /* Core palette */
  --eve-bg:          #080a0d;
  --eve-bg-deep:     #040507;
  --eve-panel:       rgba(10,12,18,0.97);
  --eve-panel-light: rgba(16,18,26,0.95);

  /* Gold hierarchy */
  --gold:       #C8A84B;
  --gold-bright:#E8C86A;
  --gold-dim:   #6B5520;
  --gold-glow:  rgba(200,168,75,0.18);

  /* Cyan / tech */
  --cyan:       #4FC3F7;
  --cyan-dim:   #1A4A5C;
  --cyan-glow:  rgba(79,195,247,0.15);

  /* Red / alert */
  --red:        #CF3B3B;
  --red-bright: #FF4444;
  --red-dim:    #3A1010;
  --red-glow:   rgba(207,59,59,0.2);

  /* Borders & dividers */
  --border:     #1E2028;
  --border-mid: #2A2D38;
  --border-hi:  #3A3D4A;

  /* Text */
  --text-primary:   #D8D8E0;
  --text-secondary: #8A8D9A;
  --text-dim:       #404355;
  --text-label:     #5A5D6E;

  /* Fonts */
  --font-ui:   'Electrolize', monospace;
  --font-data: 'Share Tech Mono', monospace;
  --font-lore: 'Cinzel', serif;
  --font-body: 'Rajdhani', sans-serif;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html, body {
  background: var(--eve-bg-deep);
  font-family: var(--font-body);
  color: var(--text-secondary);
  min-height: 100vh;
  overflow-x: hidden;
}

/* ── BACKGROUND GRID ── */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  background-image:
    linear-gradient(rgba(200,168,75,0.015) 1px, transparent 1px),
    linear-gradient(90deg, rgba(200,168,75,0.015) 1px, transparent 1px);
  background-size: 40px 40px;
  pointer-events: none;
  z-index: 0;
}

/* ══════════════════════════════════════════════
   LAYOUT SHELL
══════════════════════════════════════════════ */
.neocom-shell {
  position: relative;
  z-index: 1;
  max-width: 1100px;
  margin: 0 auto;
  padding: 24px 16px 60px;
}

/* ══════════════════════════════════════════════
   WINDOW — base component
══════════════════════════════════════════════ */
.win {
  position: relative;
  background: var(--eve-panel);
  border: 1px solid var(--border-mid);
  border-top: 2px solid var(--gold-dim);
  box-shadow:
    0 0 0 1px rgba(0,0,0,0.8),
    0 20px 60px rgba(0,0,0,0.9),
    inset 0 0 60px rgba(0,0,0,0.5);
  overflow: hidden;
}

/* Corner notch */
.win::before {
  content: '';
  position: absolute;
  top: 0; right: 0;
  width: 0; height: 0;
  border-style: solid;
  border-width: 0 20px 20px 0;
  border-color: transparent var(--gold-dim) transparent transparent;
  z-index: 30;
}

/* CRT scanlines overlay */
.win::after {
  content: '';
  position: absolute;
  inset: 0;
  background:
    repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(0,0,0,0.06) 2px,
      rgba(0,0,0,0.06) 4px
    );
  pointer-events: none;
  z-index: 50;
  opacity: 0.6;
}

/* ── Window titlebar ── */
.win-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 8px 16px;
  background: linear-gradient(180deg, #14161E 0%, #0A0C12 100%);
  border-bottom: 1px solid var(--border);
  position: relative;
  z-index: 10;
  gap: 12px;
}
.win-bar::after {
  content: '';
  position: absolute;
  bottom: 0; left: 0; right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent 0%, var(--gold-dim) 30%, var(--gold-dim) 70%, transparent 100%);
  opacity: 0.5;
}

.win-bar-left {
  display: flex;
  align-items: center;
  gap: 10px;
  min-width: 0;
}

.win-bar-icon {
  width: 18px;
  height: 18px;
  flex-shrink: 0;
  filter: drop-shadow(0 0 4px rgba(200,168,75,0.6));
}

.win-bar-title {
  font-family: var(--font-ui);
  font-size: 10px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: #B0B0BC;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.win-bar-controls {
  display: flex;
  align-items: center;
  gap: 6px;
  flex-shrink: 0;
}

/* ── Status pill ── */
.status-pill {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 3px 10px;
  border: 1px solid rgba(79,195,247,0.2);
  background: rgba(79,195,247,0.04);
  font-family: var(--font-data);
  font-size: 9px;
  letter-spacing: 2px;
  color: var(--cyan);
}

.status-dot {
  width: 5px;
  height: 5px;
  border-radius: 50%;
  background: var(--cyan);
  box-shadow: 0 0 6px var(--cyan);
  animation: blink 1.6s ease-in-out infinite alternate;
}

@keyframes blink {
  from { opacity: 1; box-shadow: 0 0 6px var(--cyan); }
  to   { opacity: 0.3; box-shadow: 0 0 2px var(--cyan); }
}

/* ── Section label ── */
.sec-label {
  display: flex;
  align-items: center;
  gap: 8px;
  font-family: var(--font-ui);
  font-size: 9px;
  letter-spacing: 3.5px;
  text-transform: uppercase;
  color: var(--text-dim);
  padding-bottom: 8px;
  border-bottom: 1px solid var(--border);
  margin-bottom: 14px;
}
.sec-label::before {
  content: '';
  display: inline-block;
  width: 7px; height: 7px;
  background: var(--gold-dim);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
  flex-shrink: 0;
}

/* ── Divider ── */
.eve-divider {
  display: flex;
  align-items: center;
  gap: 12px;
  margin: 20px 0;
}
.eve-divider::before,
.eve-divider::after {
  content: '';
  flex: 1;
  height: 1px;
}
.eve-divider::before { background: linear-gradient(90deg, transparent, var(--border-mid)); }
.eve-divider::after  { background: linear-gradient(90deg, var(--border-mid), transparent); }
.eve-divider-gem {
  width: 7px; height: 7px;
  background: var(--gold-dim);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
}

/* ══════════════════════════════════════════════
   TOP NAV BAR — NEOCOM-style
══════════════════════════════════════════════ */
.neocom-topbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 6px 16px;
  background: linear-gradient(180deg, #0E1018 0%, #080A10 100%);
  border: 1px solid var(--border-mid);
  border-bottom: 2px solid var(--gold-dim);
  margin-bottom: 2px;
  gap: 20px;
  flex-wrap: wrap;
}

.neocom-logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-family: var(--font-lore);
  font-size: 11px;
  letter-spacing: 4px;
  color: var(--gold);
  text-shadow: 0 0 12px rgba(200,168,75,0.4);
  text-transform: uppercase;
}
.neocom-logo img {
  filter: drop-shadow(0 0 8px rgba(200,168,75,0.7));
}

.neocom-nav {
  display: flex;
  align-items: center;
  gap: 2px;
}
.neocom-nav-item {
  padding: 5px 14px;
  font-family: var(--font-ui);
  font-size: 9px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--text-dim);
  cursor: pointer;
  border: 1px solid transparent;
  transition: all 0.2s;
  text-decoration: none;
}
.neocom-nav-item:hover {
  color: var(--text-secondary);
  border-color: var(--border-mid);
  background: rgba(255,255,255,0.03);
}
.neocom-nav-item.active {
  color: var(--gold);
  border-color: var(--gold-dim);
  background: var(--gold-glow);
}

.neocom-time {
  font-family: var(--font-data);
  font-size: 10px;
  color: var(--text-dim);
  letter-spacing: 2px;
}

/* ══════════════════════════════════════════════
   TERMINAL COLUMN (left sidebar)
══════════════════════════════════════════════ */
.terminal-col {
  width: 180px;
  flex-shrink: 0;
  background: #000;
  border-right: 1px solid #0E1018;
  position: relative;
  overflow: hidden;
  -webkit-mask-image: linear-gradient(to bottom, transparent 0%, black 5%, black 95%, transparent 100%);
  mask-image: linear-gradient(to bottom, transparent 0%, black 5%, black 95%, transparent 100%);
}

.terminal-scroll {
  position: absolute;
  top: 0; left: 0; right: 0;
  padding: 14px 12px;
  animation: terminal-scroll 18s linear infinite;
}

@keyframes terminal-scroll {
  0%   { transform: translateY(0); }
  100% { transform: translateY(-50%); }
}

.terminal-line {
  display: block;
  font-family: var(--font-data);
  font-size: 9px;
  line-height: 1.7;
  letter-spacing: 0.5px;
  color: rgba(79,195,247,0.5);
  text-shadow: 0 0 4px rgba(79,195,247,0.3);
}
.terminal-line.warn { color: rgba(207,59,59,0.7); text-shadow: 0 0 4px rgba(207,59,59,0.3); }
.terminal-line.ok   { color: rgba(200,168,75,0.7); text-shadow: 0 0 4px rgba(200,168,75,0.3); }
.terminal-line.dim  { color: rgba(79,195,247,0.2); }

/* ══════════════════════════════════════════════
   CONTENT AREA
══════════════════════════════════════════════ */
.main-flex {
  display: flex;
  align-items: stretch;
  position: relative;
  z-index: 1;
  min-height: 300px;
}

.main-content {
  flex: 1;
  padding: 24px 28px;
  min-width: 0;
  background: radial-gradient(ellipse at 20% 0%, rgba(200,168,75,0.025) 0%, transparent 60%);
}

/* ══════════════════════════════════════════════
   NEURAL SYNC BLOCK
══════════════════════════════════════════════ */
.sync-block {
  position: relative;
  border: 1px solid #1A2030;
  background: rgba(0,8,18,0.6);
  padding: 10px 14px 20px;
  margin-bottom: 20px;
  font-family: var(--font-data);
  font-size: 9px;
  letter-spacing: 1.5px;
  color: var(--text-dim);
  overflow: hidden;
}
.sync-block::before {
  content: '';
  position: absolute;
  top: 0; left: 0;
  width: 0; height: 0;
  border-style: solid;
  border-width: 10px 10px 0 0;
  border-color: var(--cyan-dim) transparent transparent transparent;
}

.sync-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 8px;
}

.sync-status {
  position: relative;
  width: 220px;
  height: 14px;
}
.sync-status-wait {
  position: absolute;
  right: 0; top: 0;
  font-size: 9px;
  color: var(--gold);
  letter-spacing: 1px;
  text-shadow: 0 0 6px rgba(200,168,75,0.5);
  animation: fade-out-in 2.5s ease forwards;
}
.sync-status-ok {
  position: absolute;
  right: 0; top: 0;
  font-size: 9px;
  color: var(--cyan);
  letter-spacing: 1px;
  font-weight: 600;
  text-shadow: 0 0 6px rgba(79,195,247,0.6);
  opacity: 0;
  animation: fade-in-delay 2.5s ease forwards;
}

@keyframes fade-out-in {
  0%, 80% { opacity: 1; }
  100% { opacity: 0; }
}
@keyframes fade-in-delay {
  0%, 80% { opacity: 0; }
  100% { opacity: 1; }
}

.sync-bar-track {
  height: 2px;
  background: #080E18;
  overflow: hidden;
}
.sync-bar-fill {
  height: 100%;
  width: 0;
  background: linear-gradient(90deg, transparent 0%, var(--cyan) 60%, rgba(79,195,247,0.4) 100%);
  box-shadow: 0 0 8px var(--cyan);
  animation: sync-fill 2.2s ease-out forwards;
}
@keyframes sync-fill {
  0%   { width: 0; }
  100% { width: 100%; }
}

.sync-waveform {
  position: absolute;
  bottom: 6px; right: 12px;
  display: flex;
  align-items: flex-end;
  gap: 2px;
  height: 12px;
}
.wave-bar {
  width: 2px;
  background: var(--cyan);
  box-shadow: 0 0 4px var(--cyan);
  border-radius: 1px;
}

/* ══════════════════════════════════════════════
   ALERT BLOCK
══════════════════════════════════════════════ */
.alert-block {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
  padding: 12px 16px;
  border-left: 3px solid var(--red);
  background: rgba(20,0,0,0.5);
  margin-bottom: 20px;
  animation: alert-pulse 2.5s ease-in-out infinite;
}

@keyframes alert-pulse {
  0%, 100% { background: rgba(20,0,0,0.5); border-left-color: var(--red); box-shadow: none; }
  50%       { background: rgba(40,0,0,0.7); border-left-color: var(--red-bright); box-shadow: inset 0 0 20px rgba(207,59,59,0.15), 0 0 12px rgba(207,59,59,0.1); }
}

.alert-icon {
  display: flex;
  align-items: center;
  gap: 8px;
  font-family: var(--font-ui);
  font-size: 10px;
  letter-spacing: 3px;
  color: var(--red-bright);
  text-transform: uppercase;
  margin-bottom: 5px;
}

.alert-text {
  font-family: var(--font-body);
  font-size: 13px;
  color: #B0B0B8;
  line-height: 1.4;
}

/* ══════════════════════════════════════════════
   BIOMETRIC CARD
══════════════════════════════════════════════ */
.bio-card {
  display: flex;
  border: 1px solid var(--border-mid);
  border-top: 2px solid var(--gold-dim);
  background: rgba(0,0,0,0.5);
  margin-bottom: 20px;
  overflow: hidden;
}

/* Portrait */
.bio-portrait {
  position: relative;
  width: 180px;
  height: 180px;
  flex-shrink: 0;
  background: #000;
  overflow: hidden;
  border-right: 1px solid #1A1A0A;
}
.bio-portrait img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top center;
  display: block;
}
.bio-portrait-scan {
  position: absolute;
  left: 0; width: 100%;
  height: 1px;
  background: linear-gradient(90deg, transparent 0%, rgba(79,195,247,0.8) 40%, rgba(255,255,255,0.9) 50%, rgba(79,195,247,0.8) 60%, transparent 100%);
  box-shadow: 0 0 8px rgba(79,195,247,0.6), 0 -3px 8px rgba(79,195,247,0.2), 0 3px 8px rgba(79,195,247,0.2);
  animation: scan-move 3s cubic-bezier(0.4,0,0.2,1) infinite;
  z-index: 10;
}
@keyframes scan-move {
  0%   { top: 0%; opacity: 0; }
  5%   { opacity: 1; }
  95%  { opacity: 1; }
  100% { top: 100%; opacity: 0; }
}
.bio-portrait-gradient {
  position: absolute;
  bottom: 0; left: 0; right: 0;
  height: 50px;
  background: linear-gradient(transparent, rgba(0,0,0,0.95));
  z-index: 5;
}
.bio-portrait-label {
  position: absolute;
  bottom: 6px; left: 8px;
  font-family: var(--font-data);
  font-size: 7px;
  color: rgba(107,85,32,0.8);
  letter-spacing: 2px;
  z-index: 15;
}

/* Data table */
.bio-data {
  padding: 16px 22px;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.bio-data-title {
  font-family: var(--font-lore);
  font-size: 8px;
  letter-spacing: 4px;
  color: var(--gold);
  text-transform: uppercase;
  border-bottom: 1px solid rgba(200,168,75,0.12);
  padding-bottom: 8px;
  margin-bottom: 10px;
  opacity: 0.8;
}

.bio-table {
  width: 100%;
  border-collapse: collapse;
}
.bio-table tr {
  border-bottom: 1px solid rgba(200,168,75,0.06);
}
.bio-table tr:last-child { border-bottom: none; }
.bio-table td {
  padding: 5px 0;
  border: none !important;
  vertical-align: middle;
}
.bio-table .key {
  font-family: var(--font-ui);
  font-size: 8px;
  letter-spacing: 2px;
  color: var(--text-dim);
  text-transform: uppercase;
  width: 110px;
  white-space: nowrap;
}
.bio-table .val-name {
  font-family: var(--font-body);
  font-size: 20px;
  font-weight: 700;
  color: #ECECF0;
  letter-spacing: 1px;
}
.bio-table .val-tech {
  font-family: var(--font-data);
  font-size: 11px;
  color: var(--cyan);
}
.bio-table .val-tech span {
  color: rgba(79,195,247,0.35);
  margin-left: 6px;
}
.bio-table .val-default {
  font-family: var(--font-body);
  font-size: 13px;
  color: #888;
}
.bio-table .val-gold {
  font-family: var(--font-lore);
  font-size: 13px;
  color: var(--gold);
}
.bio-table .val-dim {
  font-family: var(--font-data);
  font-size: 10px;
  color: var(--text-dim);
  letter-spacing: 1px;
}

/* ══════════════════════════════════════════════
   INDEX / FILE BROWSER
══════════════════════════════════════════════ */
.index-panel {
  border: 1px solid var(--border-mid);
  background: rgba(0,0,0,0.65);
  margin-bottom: 20px;
  overflow: hidden;
}

.idx-lang-header {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 6px 14px;
  background: linear-gradient(90deg, rgba(200,168,75,0.08), rgba(200,168,75,0.02) 70%, transparent);
  border-bottom: 1px solid rgba(200,168,75,0.15);
  font-family: var(--font-ui);
  font-size: 9px;
  letter-spacing: 3px;
  color: var(--gold);
}
.idx-lang-header .gem {
  width: 7px; height: 7px;
  background: var(--gold-dim);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
}

.idx-folder-header {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 5px 14px 5px 20px;
  border-bottom: 1px solid rgba(255,255,255,0.04);
  background: rgba(255,255,255,0.005);
  font-family: var(--font-ui);
  font-size: 10px;
  letter-spacing: 2px;
  color: var(--text-label);
  text-transform: uppercase;
}

.idx-file-row {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 8px 14px 8px 30px;
  border-bottom: 1px solid rgba(255,255,255,0.025);
  border-left: 3px solid transparent;
  cursor: pointer;
  transition: background 0.15s, border-left-color 0.15s;
  text-decoration: none;
  color: inherit;
}
.idx-file-row:hover {
  background: rgba(79,195,247,0.025);
  border-left-color: rgba(79,195,247,0.3);
}
.idx-file-row:last-child { border-bottom: none; }

.idx-file-name {
  flex: 1;
  font-family: var(--font-body);
  font-size: 13px;
  color: #C0C0CC;
  text-decoration: none;
}
.idx-file-row:hover .idx-file-name { color: var(--cyan); }

.idx-badge {
  font-family: var(--font-data);
  font-size: 8px;
  letter-spacing: 1.5px;
  padding: 2px 6px;
  white-space: nowrap;
}
.idx-badge.red   { border: 1px solid var(--red); color: var(--red); }
.idx-badge.gold  { border: 1px solid var(--gold-dim); color: var(--gold); }

.idx-meta {
  font-family: var(--font-data);
  font-size: 9px;
  color: var(--text-dim);
  letter-spacing: 1px;
  text-align: right;
  white-space: nowrap;
  min-width: 70px;
}

.idx-lang-sep {
  border-top: 1px solid rgba(200,168,75,0.1);
}

/* ══════════════════════════════════════════════
   KILLBOARD
══════════════════════════════════════════════ */
.kb-panel {
  border: 1px solid var(--border-mid);
  background: rgba(0,0,0,0.6);
  margin-bottom: 20px;
  overflow: hidden;
}

.kb-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 8px 14px;
  background: linear-gradient(90deg, rgba(207,59,59,0.08), transparent);
  border-bottom: 1px solid rgba(207,59,59,0.15);
  gap: 10px;
}

.kb-header-left {
  display: flex;
  align-items: center;
  gap: 8px;
}

.kb-live-dot {
  width: 5px; height: 5px;
  border-radius: 50%;
  background: var(--red-bright);
  box-shadow: 0 0 6px var(--red-bright);
  animation: blink-red 1.4s ease-in-out infinite alternate;
}
@keyframes blink-red {
  from { opacity: 1; box-shadow: 0 0 6px var(--red-bright); }
  to   { opacity: 0.3; box-shadow: none; }
}

.kb-header-title {
  font-family: var(--font-ui);
  font-size: 9px;
  letter-spacing: 2px;
  color: var(--red-bright);
  text-transform: uppercase;
}

.kb-stats-row {
  display: flex;
  background: rgba(0,0,0,0.4);
  border-bottom: 1px solid var(--border);
}
.kb-stat {
  flex: 1;
  text-align: center;
  padding: 10px 8px;
  border-right: 1px solid var(--border);
}
.kb-stat:last-child { border-right: none; }
.kb-stat-val {
  font-family: var(--font-data);
  font-size: 16px;
  font-weight: normal;
  display: block;
  margin-bottom: 3px;
}
.kb-stat-val.gold  { color: var(--gold); }
.kb-stat-val.red   { color: var(--red-bright); }
.kb-stat-val.cyan  { color: var(--cyan); }
.kb-stat-label {
  font-family: var(--font-ui);
  font-size: 8px;
  letter-spacing: 2px;
  color: var(--text-dim);
  text-transform: uppercase;
}

.kb-list {
  max-height: 280px;
  overflow-y: auto;
}
.kb-list::-webkit-scrollbar { width: 3px; }
.kb-list::-webkit-scrollbar-track { background: #000; }
.kb-list::-webkit-scrollbar-thumb { background: var(--border-mid); }

.kb-row {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 8px 14px;
  border-bottom: 1px solid rgba(255,255,255,0.03);
  border-left: 3px solid var(--border);
  cursor: pointer;
  transition: background 0.15s;
  animation: fade-slide 0.3s ease both;
}
.kb-row:hover { background: rgba(200,168,75,0.03); }
.kb-row:last-child { border-bottom: none; }

@keyframes fade-slide {
  from { opacity: 0; transform: translateX(-4px); }
  to   { opacity: 1; transform: translateX(0); }
}

.kb-ship-thumb {
  width: 38px; height: 38px;
  flex-shrink: 0;
  border: 1px solid #1A1A1A;
  background: #000;
  overflow: hidden;
}
.kb-ship-thumb img {
  width: 100%; height: 100%;
  display: block;
  object-fit: cover;
}

.kb-row-info { flex: 1; min-width: 0; }
.kb-victim-name {
  font-family: var(--font-body);
  font-size: 13px;
  font-weight: 600;
  color: #E0E0E8;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
.kb-row-sub {
  font-family: var(--font-data);
  font-size: 9px;
  margin-top: 2px;
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
}
.kb-sec { }
.kb-isk { color: var(--gold); }
.kb-time { color: var(--text-dim); }

.kb-badge {
  font-family: var(--font-data);
  font-size: 8px;
  letter-spacing: 1.5px;
  padding: 2px 6px;
  flex-shrink: 0;
}
.kb-badge.kill { color: var(--gold); border: 1px solid rgba(200,168,75,0.3); background: rgba(200,168,75,0.04); }
.kb-badge.loss { color: var(--red-bright); border: 1px solid rgba(207,59,59,0.3); background: rgba(207,59,59,0.04); }

.kb-empty {
  text-align: center;
  padding: 30px;
  font-family: var(--font-data);
  font-size: 9px;
  color: var(--text-dim);
  letter-spacing: 3px;
}

/* ══════════════════════════════════════════════
   CLONES SECTION
══════════════════════════════════════════════ */
.clone-panel {
  border: 1px solid var(--border-mid);
  background: rgba(0,0,0,0.55);
  margin-bottom: 20px;
  overflow: hidden;
}

.clone-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 8px 14px;
  background: linear-gradient(90deg, rgba(79,195,247,0.06), transparent);
  border-bottom: 1px solid rgba(79,195,247,0.12);
}

.clone-row {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 10px 14px;
  border-bottom: 1px solid rgba(255,255,255,0.04);
  border-left: 3px solid var(--cyan-dim);
  transition: background 0.15s;
}
.clone-row:hover { background: rgba(79,195,247,0.03); }
.clone-row:last-child { border-bottom: none; }

.clone-portrait {
  width: 32px; height: 32px;
  border: 1px solid var(--border-mid);
  background: #0A1218;
  overflow: hidden;
  flex-shrink: 0;
}
.clone-portrait img { width: 100%; height: 100%; object-fit: cover; display: block; }

.clone-info { flex: 1; }
.clone-name {
  font-family: var(--font-data);
  font-size: 11px;
  color: #C0C8D0;
  letter-spacing: 1px;
}
.clone-location {
  font-family: var(--font-data);
  font-size: 9px;
  color: var(--text-dim);
  letter-spacing: 1px;
  margin-top: 2px;
}
.clone-implants {
  font-family: var(--font-data);
  font-size: 9px;
  color: var(--text-dim);
  font-style: italic;
  margin-top: 2px;
}

.clone-actions {
  display: flex;
  gap: 6px;
}

.btn-eve {
  padding: 4px 12px;
  font-family: var(--font-ui);
  font-size: 8px;
  letter-spacing: 2px;
  text-transform: uppercase;
  border: 1px solid var(--border-mid);
  background: rgba(255,255,255,0.04);
  color: var(--text-secondary);
  cursor: pointer;
  transition: all 0.15s;
  white-space: nowrap;
}
.btn-eve:hover {
  border-color: var(--cyan-dim);
  color: var(--cyan);
  background: var(--cyan-glow);
}
.btn-eve.danger:hover {
  border-color: var(--red-dim);
  color: var(--red-bright);
  background: var(--red-glow);
}

/* ══════════════════════════════════════════════
   EXTERNAL FEEDS BUTTONS
══════════════════════════════════════════════ */
.feeds-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
}

.feed-btn {
  display: block;
  padding: 14px 16px;
  border: 1px solid var(--border-mid);
  background: rgba(6,8,14,0.9);
  text-decoration: none;
  position: relative;
  overflow: hidden;
  transition: all 0.25s;
  clip-path: polygon(0 0, calc(100% - 10px) 0, 100% 10px, 100% 100%, 10px 100%, 0 calc(100% - 10px));
}
.feed-btn::before {
  content: '';
  position: absolute;
  top: 0; left: -100%;
  width: 100%; height: 1px;
  transition: left 0.3s;
}
.feed-btn:hover::before { left: 100%; }

.feed-btn.red-theme {
  border-top-color: #3A1818;
  border-bottom-color: #3A1818;
}
.feed-btn.red-theme:hover {
  border-color: rgba(207,59,59,0.5);
  background: rgba(207,59,59,0.04);
}
.feed-btn.red-theme::before { background: linear-gradient(90deg, transparent, rgba(207,59,59,0.4), transparent); }

.feed-btn.cyan-theme {
  border-top-color: #0A2028;
  border-bottom-color: #0A2028;
}
.feed-btn.cyan-theme:hover {
  border-color: rgba(79,195,247,0.4);
  background: rgba(79,195,247,0.04);
}
.feed-btn.cyan-theme::before { background: linear-gradient(90deg, transparent, rgba(79,195,247,0.4), transparent); }

.feed-btn-sublabel {
  display: block;
  font-family: var(--font-ui);
  font-size: 8px;
  letter-spacing: 3px;
  text-transform: uppercase;
  margin-bottom: 6px;
}
.red-theme .feed-btn-sublabel  { color: var(--red-bright); opacity: 0.7; }
.cyan-theme .feed-btn-sublabel { color: var(--cyan); opacity: 0.7; }

.feed-btn-title {
  display: block;
  font-family: var(--font-lore);
  font-size: 12px;
  letter-spacing: 2px;
  font-weight: 600;
  color: #D0D0D8;
}

/* ══════════════════════════════════════════════
   STATS ROW (wallet / sec status / SP)
══════════════════════════════════════════════ */
.stats-bar {
  display: flex;
  gap: 1px;
  margin-bottom: 20px;
}
.stat-cell {
  flex: 1;
  padding: 10px 14px;
  background: rgba(0,0,0,0.5);
  border: 1px solid var(--border);
  border-top: 1px solid var(--border-mid);
  text-align: center;
}
.stat-cell-val {
  display: block;
  font-family: var(--font-data);
  font-size: 13px;
  color: var(--gold);
  margin-bottom: 3px;
  letter-spacing: 1px;
}
.stat-cell-val.cyan  { color: var(--cyan); }
.stat-cell-val.green { color: #4FC870; }
.stat-cell-lbl {
  display: block;
  font-family: var(--font-ui);
  font-size: 8px;
  letter-spacing: 2px;
  color: var(--text-dim);
  text-transform: uppercase;
}

/* ══════════════════════════════════════════════
   FOOTER
══════════════════════════════════════════════ */
.eve-footer {
  border: 1px solid var(--border);
  border-top: 1px solid var(--border-mid);
  background: rgba(0,0,0,0.6);
  padding: 8px 16px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 20px;
}
.footer-text {
  font-family: var(--font-data);
  font-size: 8px;
  letter-spacing: 2px;
  color: var(--text-dim);
}

/* ══════════════════════════════════════════════
   FILE ICON SVG
══════════════════════════════════════════════ */
.file-icon-cyan { filter: drop-shadow(0 0 2px rgba(79,195,247,0.4)); }
.file-icon-gold { filter: drop-shadow(0 0 2px rgba(200,168,75,0.3)); }
.folder-icon { filter: none; }

/* ══════════════════════════════════════════════
   RESPONSIVE
══════════════════════════════════════════════ */
@media (max-width: 768px) {
  .main-flex { flex-direction: column; }
  .terminal-col { width: 100%; height: 80px; border-right: none; border-bottom: 1px solid var(--border); }
  .main-content { padding: 16px; }
  .neocom-topbar { flex-direction: column; gap: 8px; }
  .bio-card { flex-direction: column; }
  .bio-portrait { width: 100%; height: 150px; }
  .feeds-grid { grid-template-columns: 1fr; }
  .stats-bar { flex-wrap: wrap; }
  .neocom-nav { flex-wrap: wrap; }
}
</style>
</head>
<body>

<div class="neocom-shell">

  <!-- ══ TOP NAV ══ -->
  <div class="neocom-topbar">
    <div class="neocom-logo">
      <img src="https://image.eveonline.com/Corporation/1000082_128.png" width="20" height="20" alt="MIO">
      MIO &nbsp;//&nbsp; Secure Info Terminal &nbsp;//&nbsp; Node 77-A
    </div>
    <nav class="neocom-nav">
      <a href="#" class="neocom-nav-item active">Character</a>
      <a href="#" class="neocom-nav-item">Archives</a>
      <a href="#" class="neocom-nav-item">Combat</a>
      <a href="#" class="neocom-nav-item">Clones</a>
      <a href="#" class="neocom-nav-item">Feeds</a>
    </nav>
    <div class="neocom-time" id="eve-clock">YC128 // INITIALIZING...</div>
  </div>

  <!-- ══ MAIN WINDOW ══ -->
  <div class="win">

    <!-- Titlebar -->
    <div class="win-bar">
      <div class="win-bar-left">
        <img class="win-bar-icon" src="https://image.eveonline.com/Corporation/1000082_128.png" alt="">
        <span class="win-bar-title">MIO // Secure_Info_Terminal // Node 77-A // Access Level: ALPHA-CLEAR</span>
      </div>
      <div class="win-bar-controls">
        <div class="status-pill">
          <span class="status-dot"></span>
          LINK SECURE
        </div>
      </div>
    </div>

    <!-- Body -->
    <div class="main-flex">

      <!-- ── TERMINAL SIDEBAR ── -->
      <div class="terminal-col">
        <div class="terminal-scroll">
          <!-- Repeated twice for seamless loop -->
          <span class="terminal-line">&gt; CONNECTING_TO_NODE_77-A...</span>
          <span class="terminal-line">&gt; ESTABLISHING_NEURAL_LINK...</span>
          <span class="terminal-line">&gt; AUTH_REQUEST_SENT...</span>
          <span class="terminal-line warn">* WAITING_FOR_RESPONSE *</span>
          <span class="terminal-line">&gt; MIO_AUTH_RECEIVED...</span>
          <span class="terminal-line">&gt; SECURE_CHANNEL_ALPHA-7</span>
          <span class="terminal-line dim">ANALYZING_FIREWALL_3...</span>
          <span class="terminal-line">&gt; INJECTING_EXPLOIT...</span>
          <span class="terminal-line">&gt; FIREWALL_BYPASSED...</span>
          <span class="terminal-line warn">&gt; WARNING:ELEVATION!</span>
          <span class="terminal-line warn">&gt; WARNING:ELEVATION!</span>
          <span class="terminal-line">&gt; RE-ROUTING_TRACE...</span>
          <span class="terminal-line dim">PACKET_SNIFFING_ON...</span>
          <span class="terminal-line">&gt; EXTRACTING_SIG...</span>
          <span class="terminal-line ok">&gt; SUCCESS_ID:ZORATH</span>
          <span class="terminal-line warn">&gt; TRACE_INBOUND!</span>
          <span class="terminal-line warn">&gt; MIO_PURGE_INIT *</span>
          <span class="terminal-line">&gt; BREACH_SECTOR-G</span>
          <span class="terminal-line dim">DATA_MINING_ACTIVE</span>
          <span class="terminal-line">&gt; REBOOT_SEQ_7722</span>
          <span class="terminal-line">&gt; MEMORY_WIPE_OK</span>
          <span class="terminal-line dim">SIG_VERIFY_LOOP...</span>
          <span class="terminal-line">&gt; NODE_77A_ALIVE</span>
          <!-- duplicate -->
          <span class="terminal-line">&gt; CONNECTING_TO_NODE_77-A...</span>
          <span class="terminal-line">&gt; ESTABLISHING_NEURAL_LINK...</span>
          <span class="terminal-line">&gt; AUTH_REQUEST_SENT...</span>
          <span class="terminal-line warn">* WAITING_FOR_RESPONSE *</span>
          <span class="terminal-line">&gt; MIO_AUTH_RECEIVED...</span>
          <span class="terminal-line">&gt; SECURE_CHANNEL_ALPHA-7</span>
          <span class="terminal-line dim">ANALYZING_FIREWALL_3...</span>
          <span class="terminal-line">&gt; INJECTING_EXPLOIT...</span>
          <span class="terminal-line">&gt; FIREWALL_BYPASSED...</span>
          <span class="terminal-line warn">&gt; WARNING:ELEVATION!</span>
          <span class="terminal-line warn">&gt; WARNING:ELEVATION!</span>
          <span class="terminal-line">&gt; RE-ROUTING_TRACE...</span>
          <span class="terminal-line dim">PACKET_SNIFFING_ON...</span>
          <span class="terminal-line">&gt; EXTRACTING_SIG...</span>
          <span class="terminal-line ok">&gt; SUCCESS_ID:ZORATH</span>
          <span class="terminal-line warn">&gt; TRACE_INBOUND!</span>
          <span class="terminal-line warn">&gt; MIO_PURGE_INIT *</span>
          <span class="terminal-line">&gt; BREACH_SECTOR-G</span>
          <span class="terminal-line dim">DATA_MINING_ACTIVE</span>
          <span class="terminal-line">&gt; REBOOT_SEQ_7722</span>
          <span class="terminal-line">&gt; MEMORY_WIPE_OK</span>
          <span class="terminal-line dim">SIG_VERIFY_LOOP...</span>
          <span class="terminal-line">&gt; NODE_77A_ALIVE</span>
        </div>
      </div>

      <!-- ── MAIN CONTENT ── -->
      <div class="main-content">

        <!-- Neural Sync -->
        <div class="sync-block">
          <div class="sync-header">
            <span style="color:var(--cyan-dim);font-size:9px;">&gt; INITIALIZING NEURAL PATHWAYS...</span>
            <div class="sync-status">
              <span class="sync-status-wait">SCANNING PILOT SIGNATURE [ WAIT ]</span>
              <span class="sync-status-ok">SIGNATURE MATCHED [ SYNC 100% ]</span>
            </div>
          </div>
          <div class="sync-bar-track">
            <div class="sync-bar-fill"></div>
          </div>
          <div class="sync-waveform" id="waveform"></div>
        </div>

        <!-- Alert -->
        <div class="alert-block">
          <div>
            <div class="alert-icon">
              <svg width="13" height="13" viewBox="0 0 16 16" fill="none">
                <path d="M8 1.5L14.5 13.5H1.5L8 1.5Z" stroke="#FF4444" stroke-width="1.2" fill="rgba(255,68,68,0.1)"/>
                <line x1="8" y1="6" x2="8" y2="10" stroke="#FF4444" stroke-width="1.5"/>
                <circle cx="8" cy="12" r="0.9" fill="#FF4444"/>
              </svg>
              RESTRICTED ACCESS PROTOCOL
            </div>
            <p class="alert-text">Monitoring active. Any synaptic deviation is logged by the Ministry of Internal Order.</p>
          </div>
          <img src="https://image.eveonline.com/Corporation/1000082_128.png" width="48" height="48"
               style="filter:drop-shadow(0 0 14px rgba(207,59,59,0.9));flex-shrink:0;" alt="MIO">
        </div>

        <!-- ── BIOMETRIC CARD ── -->
        <div class="sec-label">Biometric Data</div>
        <div class="bio-card">
          <div class="bio-portrait">
            <div class="bio-portrait-scan"></div>
            <img src="https://images.evetech.net/characters/2124123129/portrait?size=512" alt="Ithika Zorath">
            <div class="bio-portrait-gradient"></div>
            <div class="bio-portrait-label">MIO // CAPSULEER</div>
          </div>
          <div class="bio-data">
            <div class="bio-data-title">Identification Records</div>
            <table class="bio-table">
              <tr>
                <td class="key">Designation</td>
                <td class="val-name">Ithika Zorath</td>
              </tr>
              <tr>
                <td class="key">Bio-Tech</td>
                <td class="val-tech">Capsuleer <span>[ ACTIVE ]</span></td>
              </tr>
              <tr>
                <td class="key">Origin</td>
                <td class="val-default">Nafomeh III</td>
              </tr>
              <tr>
                <td class="key">Allegiance</td>
                <td class="val-gold">House Tash-Murkon</td>
              </tr>
              <tr>
                <td class="key">Timestamp</td>
                <td class="val-dim">YC128.02</td>
              </tr>
            </table>
          </div>
        </div>

        <!-- ── INDEX MANAGER ── -->
        <div class="sec-label">Index Manager</div>
        <div class="index-panel">

          <!-- EN -->
          <div class="idx-lang-header">
            <span class="gem"></span>
            SYS.LANG // ENGLISH
          </div>
          <div class="idx-folder-header">
            <svg width="11" height="11" viewBox="0 0 14 14" class="folder-icon">
              <path d="M1 3.5L1 12L13 12L13 3.5L7 3.5L6 1.5L1 1.5Z" fill="#141418" stroke="#3A3D4A" stroke-width="0.8"/>
            </svg>
            MIO Archives
          </div>
          <a href="/notes/en-archives-of-house-tash-murkon" class="idx-file-row">
            <svg width="12" height="12" viewBox="0 0 14 14" class="file-icon-cyan">
              <rect x="1" y="1" width="9" height="12" rx="0.5" fill="#061420" stroke="#4FC3F7" stroke-width="0.8"/>
              <line x1="3" y1="4" x2="8" y2="4" stroke="#4FC3F7" stroke-width="0.6" opacity="0.7"/>
              <line x1="3" y1="6" x2="8" y2="6" stroke="#4FC3F7" stroke-width="0.5" opacity="0.4"/>
              <line x1="3" y1="8" x2="6" y2="8" stroke="#4FC3F7" stroke-width="0.5" opacity="0.4"/>
            </svg>
            <span class="idx-file-name">EN — ARCHIVES OF HOUSE TASH-MURKON</span>
            <span class="idx-badge red">CLASSIFIED</span>
            <span class="idx-meta">2.4 TB</span>
          </a>
          <a href="/notes/en-logbook-02-yc128" class="idx-file-row">
            <svg width="12" height="12" viewBox="0 0 14 14" class="file-icon-gold">
              <rect x="1" y="1" width="9" height="12" rx="0.5" fill="#100E04" stroke="#C8A84B" stroke-width="0.8"/>
              <line x1="3" y1="4" x2="8" y2="4" stroke="#C8A84B" stroke-width="0.6" opacity="0.7"/>
              <line x1="3" y1="6" x2="8" y2="6" stroke="#C8A84B" stroke-width="0.5" opacity="0.4"/>
              <line x1="3" y1="8" x2="6" y2="8" stroke="#C8A84B" stroke-width="0.5" opacity="0.4"/>
            </svg>
            <span class="idx-file-name">EN — Logbook 02-YC128</span>
            <span class="idx-badge gold">RESTRICTED</span>
            <span class="idx-meta">02 / YC128</span>
          </a>
          <!-- 
            OBSIDIAN : pour ajouter de nouvelles entrées, duplique un bloc <a> ci-dessus.
            Le href doit correspondre au slug généré par Digital Garden :
            le nom de ta note Obsidian en minuscules, espaces remplacés par des tirets,
            précédé de /notes/
            Ex : note "EN - Logbook 03-YC128" → href="/notes/en-logbook-03-yc128"
          -->

          <!-- FR -->
          <div class="idx-lang-header idx-lang-sep">
            <span class="gem"></span>
            SYS.LANG // FRANÇAIS
          </div>
          <div class="idx-folder-header">
            <svg width="11" height="11" viewBox="0 0 14 14" class="folder-icon">
              <path d="M1 3.5L1 12L13 12L13 3.5L7 3.5L6 1.5L1 1.5Z" fill="#141418" stroke="#3A3D4A" stroke-width="0.8"/>
            </svg>
            Archives MIO
          </div>
          <a href="/notes/fr-archives-of-house-tash-murkon" class="idx-file-row">
            <svg width="12" height="12" viewBox="0 0 14 14" class="file-icon-cyan">
              <rect x="1" y="1" width="9" height="12" rx="0.5" fill="#061420" stroke="#4FC3F7" stroke-width="0.8"/>
              <line x1="3" y1="4" x2="8" y2="4" stroke="#4FC3F7" stroke-width="0.6" opacity="0.7"/>
              <line x1="3" y1="6" x2="8" y2="6" stroke="#4FC3F7" stroke-width="0.5" opacity="0.4"/>
              <line x1="3" y1="8" x2="6" y2="8" stroke="#4FC3F7" stroke-width="0.5" opacity="0.4"/>
            </svg>
            <span class="idx-file-name">FR — ARCHIVES OF HOUSE TASH-MURKON</span>
            <span class="idx-badge red">CLASSIFIÉ</span>
            <span class="idx-meta">2.4 TB</span>
          </a>
          <a href="/notes/fr-journal-de-bord-02-yc128" class="idx-file-row">
            <svg width="12" height="12" viewBox="0 0 14 14" class="file-icon-gold">
              <rect x="1" y="1" width="9" height="12" rx="0.5" fill="#100E04" stroke="#C8A84B" stroke-width="0.8"/>
              <line x1="3" y1="4" x2="8" y2="4" stroke="#C8A84B" stroke-width="0.6" opacity="0.7"/>
              <line x1="3" y1="6" x2="8" y2="6" stroke="#C8A84B" stroke-width="0.5" opacity="0.4"/>
              <line x1="3" y1="8" x2="6" y2="8" stroke="#C8A84B" stroke-width="0.5" opacity="0.4"/>
            </svg>
            <span class="idx-file-name">FR — Journal de bord 02-YC128</span>
            <span class="idx-badge gold">RESTREINT</span>
            <span class="idx-meta">02 / YC128</span>
          </a>

        </div>

        <div class="eve-divider"><div class="eve-divider-gem"></div></div>

        <!-- ── KILLBOARD ── -->
        <div class="sec-label">Combat Registry // Live Feed</div>
        <div class="kb-panel">
          <div class="kb-header">
            <div class="kb-header-left">
              <span class="kb-live-dot"></span>
              <span class="kb-header-title">Blood_Tithe_Metrics // Ithika Zorath</span>
            </div>
            <div style="display:flex;align-items:center;gap:10px;">
              <img src="https://images.evetech.net/characters/2124123129/portrait?size=32" width="20" height="20"
                   style="border:1px solid #222;" alt="">
              <a href="https://zkillboard.com/character/2124123129/" target="_blank"
                 style="font-family:var(--font-data);font-size:8px;color:var(--text-dim);text-decoration:none;letter-spacing:1px;">
                VIEW ALL →
              </a>
            </div>
          </div>

          <div class="kb-stats-row">
            <div class="kb-stat">
              <span class="kb-stat-val gold" id="kb-kills">—</span>
              <span class="kb-stat-label">Kills</span>
            </div>
            <div class="kb-stat">
              <span class="kb-stat-val red" id="kb-losses">—</span>
              <span class="kb-stat-label">Losses</span>
            </div>
            <div class="kb-stat">
              <span class="kb-stat-val cyan" id="kb-danger">—</span>
              <span class="kb-stat-label">Danger</span>
            </div>
            <div class="kb-stat">
              <span class="kb-stat-val gold" id="kb-isk">—</span>
              <span class="kb-stat-label">ISK Destroyed</span>
            </div>
          </div>

          <div class="kb-list" id="kb-list">
            <div class="kb-empty">⟳ RETRIEVING DATA...</div>
          </div>
        </div>

        <div class="eve-divider"><div class="eve-divider-gem"></div></div>

        <!-- ── EXTERNAL FEEDS ── -->
        <div class="sec-label">External Live Feeds</div>
        <div class="feeds-grid">
          <a href="https://zkillboard.com/character/2124123129/" target="_blank" class="feed-btn red-theme">
            <span class="feed-btn-sublabel">Combat Registry</span>
            <span class="feed-btn-title">[ Blood Tithe Metrics ]</span>
          </a>
          <a href="https://abysstracker.com/u/ithika-zorath" target="_blank" class="feed-btn cyan-theme">
            <span class="feed-btn-sublabel">Deadspace Anomalies</span>
            <span class="feed-btn-title">[ Abyssal Telemetry ]</span>
          </a>
        </div>

        <!-- Footer -->
        <div class="eve-footer">
          <span class="footer-text">MIO // SECURE TERMINAL // NODE 77-A // ACCESS ALPHA-CLEAR</span>
          <span class="footer-text" id="footer-ts">YC128.02 — ITHIKA ZORATH</span>
        </div>

      </div><!-- /main-content -->
    </div><!-- /main-flex -->
  </div><!-- /win -->
</div><!-- /shell -->

<script>
/* ─── EVE CLOCK ─── */
(function() {
  function eveTime() {
    const now = new Date();
    const h = String(now.getUTCHours()).padStart(2,'0');
    const m = String(now.getUTCMinutes()).padStart(2,'0');
    const s = String(now.getUTCSeconds()).padStart(2,'0');
    return 'YC128 // ' + h + ':' + m + ':' + s + ' UTC';
  }
  const clk = document.getElementById('eve-clock');
  if (clk) {
    setInterval(function(){ clk.textContent = eveTime(); }, 1000);
    clk.textContent = eveTime();
  }
})();

/* ─── WAVEFORM ─── */
(function() {
  const wf = document.getElementById('waveform');
  if (!wf) return;
  const delays = [0.1, 0.3, 0.2, 0.5, 0.4, 0.15, 0.35];
  const speeds = [0.6, 0.8, 0.5, 0.9, 0.7, 0.55, 0.75];
  delays.forEach(function(d, i) {
    const bar = document.createElement('div');
    bar.className = 'wave-bar';
    bar.style.animation = 'wave-anim ' + speeds[i] + 's ease-in-out ' + d + 's infinite alternate';
    bar.style.height = '20%';
    wf.appendChild(bar);
  });
  const style = document.createElement('style');
  style.textContent = '@keyframes wave-anim { from { height: 15%; } to { height: 100%; } }';
  document.head.appendChild(style);
})();

/* ─── KILLBOARD ─── */
(function() {
  var CID = 2124123129;

  function fmtISK(v) {
    if (v >= 1e9) return (v/1e9).toFixed(1) + ' B';
    if (v >= 1e6) return (v/1e6).toFixed(1) + ' M';
    if (v >= 1e3) return (v/1e3).toFixed(1) + ' K';
    return v.toFixed(0);
  }

  function timeAgo(d) {
    var s = Math.floor((Date.now() - new Date(d)) / 1000);
    if (s < 60)    return s + 's ago';
    if (s < 3600)  return Math.floor(s/60) + 'm ago';
    if (s < 86400) return Math.floor(s/3600) + 'h ago';
    return Math.floor(s/86400) + 'd ago';
  }

  function secColor(s) {
    if (s >= 0.5) return '#4FC870';
    if (s >= 0.1) return '#F0A020';
    return '#CF3B3B';
  }

  // Stats
  fetch('https://zkillboard.com/api/stats/characterID/' + CID + '/')
    .then(function(r){ return r.json(); })
    .then(function(s){
      document.getElementById('kb-kills').textContent   = s.shipsDestroyed || 0;
      document.getElementById('kb-losses').textContent  = s.shipsLost || 0;
      var dr = s.dangerRatio || 0;
      var dangerEl = document.getElementById('kb-danger');
      dangerEl.textContent = dr + '%';
      dangerEl.style.color = dr > 50 ? '#CF3B3B' : '#4FC3F7';
      document.getElementById('kb-isk').textContent     = fmtISK(s.iskDestroyed || 0);
    })
    .catch(function(){});

  // Kill list
  fetch('https://zkillboard.com/api/kills/characterID/' + CID + '/')
    .then(function(r){ return r.json(); })
    .then(function(kills){
      var list = document.getElementById('kb-list');
      if (!Array.isArray(kills) || kills.length === 0) {
        list.innerHTML = '<div class="kb-empty">// NO ENGAGEMENTS RECORDED</div>';
        return;
      }
      list.innerHTML = '';

      kills.slice(0, 8).forEach(function(k, i) {
        var row = document.createElement('div');
        row.className = 'kb-row';
        row.style.animationDelay = (i * 0.07) + 's';
        row.style.borderLeftColor = '#1E2028';
        row.innerHTML =
          '<div class="kb-ship-thumb"><img src="https://images.evetech.net/types/670/render?size=64" alt=""></div>' +
          '<div class="kb-row-info"><div class="kb-victim-name" style="color:#606070;">Loading...</div></div>' +
          '<span class="kb-badge kill">KILL</span>';
        row.addEventListener('click', function(){ window.open('https://zkillboard.com/kill/' + k.killmail_id + '/', '_blank'); });
        list.appendChild(row);

        fetch('https://esi.evetech.net/latest/killmails/' + k.killmail_id + '/' + k.zkb.hash + '/')
          .then(function(r){ return r.json(); })
          .then(function(km){
            return Promise.all([
              fetch('https://esi.evetech.net/latest/universe/types/' + km.victim.ship_type_id + '/?language=en').then(function(r){ return r.json(); }),
              fetch('https://esi.evetech.net/latest/universe/systems/' + km.solar_system_id + '/').then(function(r){ return r.json(); }),
              km.victim.character_id
                ? fetch('https://esi.evetech.net/latest/characters/' + km.victim.character_id + '/').then(function(r){ return r.json(); })
                : Promise.resolve({ name: 'Unknown' })
            ]).then(function(res){
              var ship = res[0], sys = res[1], vic = res[2];
              var isKill = km.attackers && km.attackers.some(function(a){ return a.character_id === CID; });
              var sec = sys.security_status || 0;

              row.querySelector('.kb-ship-thumb img').src =
                'https://images.evetech.net/types/' + km.victim.ship_type_id + '/render?size=64';

              row.querySelector('.kb-row-info').innerHTML =
                '<div class="kb-victim-name">' + (vic.name || 'Unknown') + ' &nbsp;<span style="font-size:11px;color:var(--text-dim);font-family:var(--font-body);">— ' + (ship.name || '?') + '</span></div>' +
                '<div class="kb-row-sub">' +
                  '<span class="kb-sec" style="color:' + secColor(sec) + ';">' + sys.name + ' (' + sec.toFixed(1) + ')</span>' +
                  '<span class="kb-isk">' + fmtISK(k.zkb.totalValue || 0) + ' ISK</span>' +
                  '<span class="kb-time">' + timeAgo(km.killmail_time) + '</span>' +
                '</div>';

              var badge = row.querySelector('.kb-badge');
              if (isKill) {
                badge.textContent = 'KILL';
                badge.className = 'kb-badge kill';
                row.style.borderLeftColor = 'rgba(200,168,75,0.5)';
              } else {
                badge.textContent = 'LOSS';
                badge.className = 'kb-badge loss';
                row.style.borderLeftColor = 'rgba(207,59,59,0.5)';
              }
            });
          })
          .catch(function(){});
      });
    })
    .catch(function(){
      document.getElementById('kb-list').innerHTML = '<div class="kb-empty">✗ CONNECTION FAILED</div>';
    });
})();
</script>
</body>
</html>    box-shadow: inset -8px 0 16px rgba(0,0,0,0.9);
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
    padding: 14px 18px; margin-bottom: 24px;
    display: flex; justify-content: space-between; align-items: center; gap: 18px; position: relative;
}
.eve-alert-title {
    font-family: var(--font-ui); color: var(--eve-red); font-size: 13px; letter-spacing: 3px;
    text-transform: uppercase; margin: 0 0 5px 0; display: flex; align-items: center; gap: 8px;
}
.eve-alert-body { font-family: var(--font-body); font-size: 14px; margin: 0; color: #ccc; }

/* KILLBOARD */
.eve-killboard { border: 1px solid var(--eve-border); background: rgba(0,0,0,0.6); margin-bottom: 24px; overflow: hidden; }
.eve-killboard-header {
    background: linear-gradient(90deg, rgba(255,77,77,0.1), transparent);
    padding: 8px 14px; border-bottom: 1px solid rgba(255,77,77,0.2);
    display: flex; justify-content: space-between; align-items: center;
}
.eve-kill-row {
    display: flex; align-items: center; gap: 10px; padding: 9px 14px;
    border-bottom: 1px solid rgba(255,255,255,0.03); border-left: 3px solid #333;
    cursor: pointer; transition: background 0.15s;
}
.eve-kill-row:hover { background: rgba(212,175,55,0.04); }
.eve-kill-ship { width: 36px; height: 36px; flex-shrink: 0; border: 1px solid #222; background: #000; overflow: hidden; }
.eve-kill-ship img { width: 36px; height: 36px; display: block; object-fit: cover; }

/* BOUTONS */
.eve-btn {
    display: block; padding: 13px 16px; border: 1px solid #2a2a2e; text-align: center;
    text-decoration: none !important; transition: 0.25s; background: rgba(8,8,10,0.9);
    position: relative; overflow: hidden;
    clip-path: polygon(0 0, calc(100% - 10px) 0, 100% 10px, 100% 100%, 10px 100%, 0 calc(100% - 10px));
}
.eve-btn-label { font-family: var(--font-ui); font-size: 9px; letter-spacing: 3px; text-transform: uppercase; margin-bottom: 7px; display: block; }
.eve-btn-title { font-family: var(--font-lore); font-size: 13px; letter-spacing: 2px; font-weight: 600; display: block; color: #e0e0e0; }
.eve-btn-red { border-top: 1px solid #4a1a1a; border-bottom: 1px solid #4a1a1a; }
.eve-btn-red:hover { border-color: rgba(255,77,77,0.6); background: rgba(255,77,77,0.06); }
.eve-btn-cyan { border-top: 1px solid #0a2a2e; border-bottom: 1px solid #0a2a2e; }
.eve-btn-cyan:hover { border-color: rgba(125,249,255,0.4); background: rgba(125,249,255,0.05); }

/* SYNC */
.eve-sync-block {
    border: 1px solid #1a1e22; background: rgba(0,12,20,0.5);
    padding: 12px 14px 26px 14px; margin-bottom: 24px; font-family: var(--font-data);
    font-size: 10px; letter-spacing: 1px; position: relative;
}
.eve-sync-block::before {
    content: ""; position: absolute; top: 0; left: 0; width: 0; height: 0; border-style: solid;
    border-width: 12px 12px 0 0; border-color: var(--eve-cyan-dim) transparent transparent transparent; opacity: 0.5;
}
.sync-bar-container { width: 100%; height: 2px; background: #0a1015; margin-top: 10px; overflow: hidden; position: relative; }
.sync-bar-fill { height: 100%; background: linear-gradient(90deg, transparent, var(--eve-cyan), rgba(125,249,255,0.3)); width: 100%; animation: loadingBar 2s ease-out forwards; box-shadow: 0 0 8px var(--eve-cyan); }
.ai-waveform-container { display: flex; align-items: flex-end; gap: 2px; height: 14px; position: absolute; bottom: 8px; right: 12px; opacity: 0.8; }
.waveform-bar { width: 2px; background-color: var(--eve-cyan); box-shadow: 0 0 5px var(--eve-cyan); border-radius: 1px; }

/* SCAN LINE */
.scan-line {
    position: absolute; left: 0; width: 100%; height: 1px;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.6), transparent);
    box-shadow: 0 0 8px rgba(255,255,255,0.4), 0 -4px 10px rgba(255,100,100,0.5), 0 4px 10px rgba(255,100,100,0.5);
    z-index: 10; animation: scanMove 2.8s cubic-bezier(0.4,0,0.2,1) infinite; pointer-events: none;
}

/* DIVIDER */
.eve-divider { display: flex; align-items: center; gap: 10px; margin: 22px 0; }
.eve-divider::before { content: ""; flex: 1; height: 1px; background: linear-gradient(90deg, transparent, var(--eve-border)); }
.eve-divider::after  { content: ""; flex: 1; height: 1px; background: linear-gradient(90deg, var(--eve-border), transparent); }
.eve-divider-icon { width: 8px; height: 8px; background: var(--eve-gold-dim); clip-path: polygon(50% 0%,100% 50%,50% 100%,0% 50%); }

/* INDEX ROWS — styles appliqués sur les <tr> directement */
.eve-index-table { width: 100%; border-collapse: collapse; }
.eve-index-table td { border-left: none !important; border-right: none !important; border-top: none !important; }
.eve-index-table, .eve-index-table tr, .eve-index-table td { border-color: transparent; }
.eve-index-table tr.lang-hdr td { background: linear-gradient(90deg,rgba(212,175,55,0.12),rgba(212,175,55,0.02) 60%,transparent); padding: 7px 14px; border-bottom: 1px solid rgba(212,175,55,0.2); border-top: none; border-left: none; border-right: none; font-family: var(--font-ui); color: var(--eve-gold); font-size: 10px; letter-spacing: 3px; }
.eve-index-table tr.folder-hdr td { padding: 6px 14px 6px 20px; border-bottom: 1px solid #1a1a1e; border-top: none; border-left: none; border-right: none; background: rgba(255,255,255,0.006); font-family: var(--font-ui); color: #888; font-size: 11px; letter-spacing: 2px; text-transform: uppercase; }
.eve-index-table tr.file-row td { padding: 9px 8px; border-bottom: 1px solid rgba(255,255,255,0.025); border-top: none; border-left: none; border-right: none; }
.eve-index-table tr.file-row { border-left: 3px solid transparent; transition: 0.15s; }
.eve-index-table tr.file-row:hover { background: rgba(125,249,255,0.03); border-left-color: rgba(125,249,255,0.25); }
.eve-index-table tr.lang-sep td { border-top: 1px solid rgba(212,175,55,0.1); }
.eve-index-table a { font-family: var(--font-body); color: #ccc !important; font-size: 13px; text-decoration: none !important; }
.eve-index-table a:hover { color: var(--eve-cyan) !important; }
.eve-badge-red { font-family: var(--font-data); font-size: 9px; letter-spacing: 1.5px; padding: 1px 5px; border: 1px solid var(--eve-red); color: var(--eve-red); white-space: nowrap; }
.eve-badge-gold { font-family: var(--font-data); font-size: 9px; letter-spacing: 1.5px; padding: 1px 5px; border: 1px solid var(--eve-gold); color: var(--eve-gold); white-space: nowrap; }
.eve-meta { font-family: var(--font-data); font-size: 10px; color: #333; letter-spacing: 1px; white-space: nowrap; text-align: right; }

/* ANIMATIONS */
@keyframes scrollHack  { 0% { transform: translateY(0); }    100% { transform: translateY(-50%); } }
@keyframes scanMove    { 0% { top: 0%; opacity: 0; } 8% { opacity: 1; } 92% { opacity: 1; } 100% { top: 100%; opacity: 0; } }
@keyframes waveform    { 0%, 100% { height: 15%; } 50% { height: 100%; } }
@keyframes loadingBar  { 0% { width: 0%; } 100% { width: 100%; } }
@keyframes hideText    { 0%, 99% { opacity: 1; } 100% { opacity: 0; } }
@keyframes showText    { 0%, 99% { opacity: 0; } 100% { opacity: 1; } }
@keyframes fadeSlideIn { from { opacity:0; transform: translateX(-6px); } to { opacity:1; transform: translateX(0); } }
@keyframes pulseAlert  {
    0%,100% { border-color: var(--eve-red); box-shadow: 0 0 8px rgba(255,77,77,0.15); background-color: rgba(25,0,0,0.5); }
    50%      { border-color: #ff1a1a; box-shadow: inset 0 0 25px rgba(255,0,0,0.4), 0 0 20px rgba(255,0,0,0.5); background-color: rgba(45,0,0,0.75); }
}

@media (max-width: 768px) {
    .eve-main-flex { flex-direction: column; }
    .eve-terminal-left { width: 100%; height: 90px; border-right: none; border-bottom: 1px solid #1a1a1e; }
    .eve-content { padding: 16px 14px; }
    .eve-window-header { flex-direction: column; gap: 8px; }
    .eve-alert-pulse { flex-direction: column-reverse; text-align: center; }
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
      <div style="color:#3a5060;">> INITIALIZING NEURAL PATHWAYS...</div>
      <div style="position:relative;width:230px;height:14px;">
        <div style="animation:hideText 2s forwards;position:absolute;right:0;top:0;color:var(--eve-gold);font-size:10px;letter-spacing:1px;text-shadow:0 0 5px var(--eve-gold);width:100%;text-align:right;">SCANNING PILOT SIGNATURE [ WAIT ]</div>
        <div style="animation:showText 2s forwards;opacity:0;position:absolute;right:0;top:0;color:var(--eve-cyan);font-size:10px;letter-spacing:1px;font-weight:bold;text-shadow:0 0 6px var(--eve-cyan);width:100%;text-align:right;">SIGNATURE MATCHED [ SYNC 100% ]</div>
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

  <!-- ═══════════════════════════════════
       PROFIL BIOMÉTRIQUE — carte horizontale
       ═══════════════════════════════════ -->
  <div class="eve-section-label">Biometric Data</div>
  <div style="border:1px solid #2a2a2e;border-top:2px solid #8B6914;background:rgba(0,0,0,0.55);margin-bottom:24px;overflow:hidden;">
    <table width="100%" border="0" cellpadding="0" cellspacing="0" style="border-collapse:collapse;">
      <tr style="border:none;">
        <td width="190" style="padding:0;vertical-align:top;border-right:1px solid #1e1a0a;">
          <div style="position:relative;width:190px;height:190px;overflow:hidden;background:#000;">
            <div class="scan-line"></div>
            <img src="https://images.evetech.net/characters/2124123129/portrait?size=512" width="190" height="190" style="display:block;object-fit:cover;object-position:top center;">
            <div style="position:absolute;bottom:0;left:0;right:0;height:45px;background:linear-gradient(to top,rgba(0,0,0,0.9),transparent);"></div>
            <div style="position:absolute;bottom:6px;left:8px;font-family:'Share Tech Mono',monospace;font-size:8px;color:#8B6914;letter-spacing:2px;">MIO // CAPSULEER</div>
          </div>
        </td>
        <td style="padding:18px 24px;vertical-align:middle;">
          <div style="font-family:'Cinzel',serif;color:#D4AF37;font-size:9px;letter-spacing:4px;text-transform:uppercase;border-bottom:1px solid rgba(212,175,55,0.15);padding-bottom:8px;margin-bottom:12px;">Identification Records</div>
          <table width="100%" border="0" cellpadding="0" cellspacing="0" style="border-collapse:collapse;">
            <tr><td width="120" style="font-family:'Electrolize',monospace;color:#444;font-size:9px;letter-spacing:2px;text-transform:uppercase;padding:6px 0;border:none;border-bottom:1px solid rgba(212,175,55,0.08);">Designation</td><td style="font-family:'Rajdhani',sans-serif;color:#f0f0f0;font-size:18px;font-weight:700;letter-spacing:1px;padding:6px 0;border:none;border-bottom:1px solid rgba(212,175,55,0.08);">Ithika Zorath</td></tr>
            <tr><td style="font-family:'Electrolize',monospace;color:#444;font-size:9px;letter-spacing:2px;text-transform:uppercase;padding:6px 0;border:none;border-bottom:1px solid rgba(212,175,55,0.08);">Bio-Tech</td><td style="font-family:'Share Tech Mono',monospace;color:#7DF9FF;font-size:12px;padding:6px 0;border:none;border-bottom:1px solid rgba(212,175,55,0.08);">Capsuleer <span style="color:#3a7a7e;">[ ACTIVE ]</span></td></tr>
            <tr><td style="font-family:'Electrolize',monospace;color:#444;font-size:9px;letter-spacing:2px;text-transform:uppercase;padding:6px 0;border:none;border-bottom:1px solid rgba(212,175,55,0.08);">Origin</td><td style="font-family:'Rajdhani',sans-serif;color:#999;font-size:14px;padding:6px 0;border:none;border-bottom:1px solid rgba(212,175,55,0.08);">Nafomeh III</td></tr>
            <tr><td style="font-family:'Electrolize',monospace;color:#444;font-size:9px;letter-spacing:2px;text-transform:uppercase;padding:6px 0;border:none;border-bottom:1px solid rgba(212,175,55,0.08);">Allegiance</td><td style="font-family:'Cinzel',serif;color:#D4AF37;font-size:14px;padding:6px 0;border:none;border-bottom:1px solid rgba(212,175,55,0.08);">House Tash-Murkon</td></tr>
            <tr><td style="font-family:'Electrolize',monospace;color:#444;font-size:9px;letter-spacing:2px;text-transform:uppercase;padding:6px 0;border:none;">Timestamp</td><td style="font-family:'Share Tech Mono',monospace;color:#333;font-size:11px;padding:6px 0;letter-spacing:1px;border:none;">YC128.02</td></tr>
          </table>
        </td>
      </tr>
    </table>
  </div>

  <!-- ═══════════════════════════════════
       INDEX MANAGER — pleine largeur
       ═══════════════════════════════════ -->
  <div class="eve-section-label">Index Manager</div>
  <div style="border:1px solid #2a2a2e;background:rgba(0,0,0,0.7);margin-bottom:24px;">
    <table class="eve-index-table">
      <!-- EN -->
      <tr class="lang-hdr"><td colspan="3"><span style="display:inline-block;width:8px;height:8px;background:#8B6914;clip-path:polygon(50% 0%,100% 50%,50% 100%,0% 50%);margin-right:8px;vertical-align:middle;"></span>SYS.LANG // ENGLISH</td></tr>
      <tr class="folder-hdr"><td colspan="3"><span style="font-size:8px;color:#555;margin-right:6px;">▼</span><svg width="12" height="12" viewBox="0 0 13 13" style="vertical-align:middle;margin-right:6px;"><path d="M1 3.5 L1 12 L12 12 L12 3.5 L6 3.5 L5 1.5 L1 1.5 Z" fill="#1a1a1e" stroke="#444" stroke-width="0.8"/></svg>MIO Archives</td></tr>
      <tr class="file-row">
        <td style="width:30px;padding-left:30px;"><span style="font-size:7px;color:#2a2a2a;">▶</span></td>
        <td><svg width="13" height="13" viewBox="0 0 14 14" style="vertical-align:middle;margin-right:8px;"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#0a1520" stroke="#7DF9FF" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#7DF9FF" stroke-width="0.6" opacity="0.6"/><line x1="3" y1="6" x2="8" y2="6" stroke="#7DF9FF" stroke-width="0.6" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#7DF9FF" stroke-width="0.6" opacity="0.4"/></svg><a href="/notes/en-archives-of-house-tash-murkon">EN — ARCHIVES OF HOUSE TASH-MURKON</a></td>
        <td style="text-align:right;padding-right:14px;white-space:nowrap;"><span style="font-family:'Share Tech Mono',monospace;font-size:9px;letter-spacing:1.5px;padding:2px 6px;border:1px solid #ff4d4d;color:#ff4d4d;white-space:nowrap;">CLASSIFIED</span> <span class="eve-meta" style="display:inline-block;margin-left:10px;">2.4 TB</span></td>
      </tr>
      <tr class="file-row">
        <td style="width:30px;padding-left:30px;"><span style="font-size:7px;color:#2a2a2a;">▶</span></td>
        <td><svg width="13" height="13" viewBox="0 0 14 14" style="vertical-align:middle;margin-right:8px;"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#12100a" stroke="#D4AF37" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#D4AF37" stroke-width="0.6" opacity="0.7"/><line x1="3" y1="6" x2="8" y2="6" stroke="#D4AF37" stroke-width="0.6" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#D4AF37" stroke-width="0.6" opacity="0.4"/></svg><a href="/notes/en-logbook-02-yc128">EN — Logbook 02-YC128</a></td>
        <td style="text-align:right;padding-right:14px;white-space:nowrap;"><span style="font-family:'Share Tech Mono',monospace;font-size:9px;letter-spacing:1.5px;padding:2px 6px;border:1px solid #D4AF37;color:#D4AF37;white-space:nowrap;">RESTRICTED</span> <span class="eve-meta" style="display:inline-block;margin-left:10px;">02 / YC128</span></td>
      </tr>
      <!-- FR -->
      <tr class="lang-hdr lang-sep"><td colspan="3"><span style="display:inline-block;width:8px;height:8px;background:#8B6914;clip-path:polygon(50% 0%,100% 50%,50% 100%,0% 50%);margin-right:8px;vertical-align:middle;"></span>SYS.LANG // FRANÇAIS</td></tr>
      <tr class="folder-hdr"><td colspan="3"><span style="font-size:8px;color:#555;margin-right:6px;">▼</span><svg width="12" height="12" viewBox="0 0 13 13" style="vertical-align:middle;margin-right:6px;"><path d="M1 3.5 L1 12 L12 12 L12 3.5 L6 3.5 L5 1.5 L1 1.5 Z" fill="#1a1a1e" stroke="#444" stroke-width="0.8"/></svg>Archives MIO</td></tr>
      <tr class="file-row">
        <td style="width:30px;padding-left:30px;"><span style="font-size:7px;color:#2a2a2a;">▶</span></td>
        <td><svg width="13" height="13" viewBox="0 0 14 14" style="vertical-align:middle;margin-right:8px;"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#0a1520" stroke="#7DF9FF" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#7DF9FF" stroke-width="0.6" opacity="0.6"/><line x1="3" y1="6" x2="8" y2="6" stroke="#7DF9FF" stroke-width="0.6" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#7DF9FF" stroke-width="0.6" opacity="0.4"/></svg><a href="/notes/fr-archives-of-house-tash-murkon">FR — ARCHIVES OF HOUSE TASH-MURKON</a></td>
        <td style="text-align:right;padding-right:14px;white-space:nowrap;"><span style="font-family:'Share Tech Mono',monospace;font-size:9px;letter-spacing:1.5px;padding:2px 6px;border:1px solid #ff4d4d;color:#ff4d4d;white-space:nowrap;">CLASSIFIÉ</span> <span class="eve-meta" style="display:inline-block;margin-left:10px;">2.4 TB</span></td>
      </tr>
      <tr class="file-row">
        <td style="width:30px;padding-left:30px;"><span style="font-size:7px;color:#2a2a2a;">▶</span></td>
        <td><svg width="13" height="13" viewBox="0 0 14 14" style="vertical-align:middle;margin-right:8px;"><rect x="1" y="1" width="9" height="12" rx="0.5" fill="#12100a" stroke="#D4AF37" stroke-width="0.8"/><line x1="3" y1="4" x2="8" y2="4" stroke="#D4AF37" stroke-width="0.6" opacity="0.7"/><line x1="3" y1="6" x2="8" y2="6" stroke="#D4AF37" stroke-width="0.6" opacity="0.4"/><line x1="3" y1="8" x2="6" y2="8" stroke="#D4AF37" stroke-width="0.6" opacity="0.4"/></svg><a href="/notes/fr-journal-de-bord-02-yc128">FR — Journal de bord 02-YC128</a></td>
        <td style="text-align:right;padding-right:14px;white-space:nowrap;"><span style="font-family:'Share Tech Mono',monospace;font-size:9px;letter-spacing:1.5px;padding:2px 6px;border:1px solid #D4AF37;color:#D4AF37;white-space:nowrap;">RESTREINT</span> <span class="eve-meta" style="display:inline-block;margin-left:10px;">02 / YC128</span></td>
      </tr>
    </table>
  </div>

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
        <img src="https://images.evetech.net/characters/2124123129/portrait?size=32" width="22" height="22" style="border:1px solid #333;" onerror="this.style.display='none'">
        <a href="https://zkillboard.com/character/2124123129/" target="_blank" style="font-family:var(--font-data);font-size:9px;color:#444;text-decoration:none;letter-spacing:1px;">VIEW ALL →</a>
      </div>
    </div>
    <table width="100%" border="0" cellpadding="0" cellspacing="0" style="border-collapse:collapse;">
      <tr style="background:rgba(0,0,0,0.5);">
        <td style="text-align:center;padding:10px;border-right:1px solid #111;"><div id="kb-kills" style="font-family:var(--font-data);font-size:15px;color:var(--eve-gold);">—</div><div style="font-family:var(--font-ui);font-size:9px;color:#333;margin-top:2px;letter-spacing:2px;">KILLS</div></td>
        <td style="text-align:center;padding:10px;border-right:1px solid #111;"><div id="kb-losses" style="font-family:var(--font-data);font-size:15px;color:var(--eve-red);">—</div><div style="font-family:var(--font-ui);font-size:9px;color:#333;margin-top:2px;letter-spacing:2px;">PERTES</div></td>
        <td style="text-align:center;padding:10px;border-right:1px solid #111;"><div id="kb-danger" style="font-family:var(--font-data);font-size:15px;color:var(--eve-cyan);">—</div><div style="font-family:var(--font-ui);font-size:9px;color:#333;margin-top:2px;letter-spacing:2px;">DANGER</div></td>
        <td style="text-align:center;padding:10px;"><div id="kb-isk" style="font-family:var(--font-data);font-size:15px;color:var(--eve-gold);">—</div><div style="font-family:var(--font-ui);font-size:9px;color:#333;margin-top:2px;letter-spacing:2px;">ISK DÉTRUIT</div></td>
      </tr>
    </table>
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
  var CID=2124123129;
  function isk(v){if(v>=1e9)return(v/1e9).toFixed(1)+' B';if(v>=1e6)return(v/1e6).toFixed(1)+' M';if(v>=1e3)return(v/1e3).toFixed(1)+' K';return v.toFixed(0);}
  function ago(d){var s=Math.floor((Date.now()-new Date(d))/1000);if(s<60)return s+'s';if(s<3600)return Math.floor(s/60)+'m';if(s<86400)return Math.floor(s/3600)+'h';return Math.floor(s/86400)+'d';}
  function sc(s){if(s>=0.5)return'#4dff91';if(s>=0.1)return'#ff9900';return'#ff4d4d';}
  fetch('https://zkillboard.com/api/stats/characterID/'+CID+'/').then(function(r){return r.json();}).then(function(s){
    document.getElementById('kb-kills').textContent=s.shipsDestroyed||0;
    document.getElementById('kb-losses').textContent=s.shipsLost||0;
    var dr=s.dangerRatio||0;
    document.getElementById('kb-danger').textContent=dr+'%';
    document.getElementById('kb-danger').style.color=dr>50?'#ff4d4d':'#7DF9FF';
    document.getElementById('kb-isk').textContent=isk(s.iskDestroyed||0);
  }).catch(function(){});
  fetch('https://zkillboard.com/api/kills/characterID/'+CID+'/').then(function(r){return r.json();}).then(function(kills){
    var list=document.getElementById('kb-list');
    if(!Array.isArray(kills)||kills.length===0){list.innerHTML='<div style="text-align:center;padding:30px;font-family:monospace;font-size:10px;color:#1e1e1e;letter-spacing:2px;">// AUCUN ENGAGEMENT ENREGISTRÉ</div>';return;}
    list.innerHTML='';
    kills.slice(0,8).forEach(function(k,i){
      var row=document.createElement('div');
      row.className='eve-kill-row';
      row.style.animation='fadeSlideIn 0.3s ease '+(i*0.06)+'s both';
      row.innerHTML='<div class="eve-kill-ship"><img src="https://images.evetech.net/types/670/render?size=64" width="36" height="36"></div><div style="flex:1;min-width:0;font-family:var(--font-data);font-size:10px;color:#333;letter-spacing:1px;">Loading...</div><div style="font-family:var(--font-data);font-size:9px;color:#D4AF37;padding:1px 5px;border:1px solid #2a2a00;background:rgba(212,175,55,0.05);flex-shrink:0;">KILL</div>';
      row.onclick=function(){window.open('https://zkillboard.com/kill/'+k.killmail_id+'/','_blank');};
      list.appendChild(row);
      fetch('https://esi.evetech.net/latest/killmails/'+k.killmail_id+'/'+k.zkb.hash+'/').then(function(r){return r.json();}).then(function(km){
        Promise.all([
          fetch('https://esi.evetech.net/latest/universe/types/'+km.victim.ship_type_id+'/?language=en').then(function(r){return r.json();}),
          fetch('https://esi.evetech.net/latest/universe/systems/'+km.solar_system_id+'/').then(function(r){return r.json();}),
          km.victim.character_id?fetch('https://esi.evetech.net/latest/characters/'+km.victim.character_id+'/').then(function(r){return r.json();}):Promise.resolve({name:'Unknown'})
        ]).then(function(res){
          var ship=res[0],sys=res[1],vic=res[2];
          var isKill=km.attackers&&km.attackers.some(function(a){return a.character_id===CID;});
          var sec=sys.security_status||0;
          row.querySelector('.eve-kill-ship img').src='https://images.evetech.net/types/'+km.victim.ship_type_id+'/render?size=64';
          row.querySelector('div[style*="flex:1"]').innerHTML='<div style="margin-bottom:3px;"><span style="font-family:Rajdhani,sans-serif;font-size:13px;font-weight:600;color:#e0e0e0;">'+(vic.name||'Unknown')+'</span> <span style="font-family:Electrolize,monospace;font-size:10px;color:#444;">—</span> <span style="font-family:Rajdhani,sans-serif;font-size:12px;color:#666;">'+(ship.name||'?')+'</span></div><div style="font-family:\'Share Tech Mono\',monospace;font-size:10px;"><span style="color:'+sc(sec)+';">'+sys.name+' ('+sec.toFixed(1)+')</span> <span style="color:#D4AF37;margin-left:8px;">'+isk(k.zkb.totalValue||0)+' ISK</span> <span style="color:#2a2a2a;margin-left:8px;">'+ago(km.killmail_time)+'</span></div>';
          var badge=row.lastElementChild;
          badge.textContent=isKill?'KILL':'LOSS';
          badge.style.color=isKill?'#D4AF37':'#ff4d4d';
          badge.style.borderColor=isKill?'#2a2a00':'#2a0000';
          row.style.borderLeftColor=isKill?'#D4AF37':'#ff4d4d';
        }).catch(function(){});
      }).catch(function(){});
    });
  }).catch(function(){
    document.getElementById('kb-list').innerHTML='<div style="text-align:center;padding:30px;font-family:monospace;font-size:10px;color:#2a2a2a;letter-spacing:2px;">✗ CONNEXION ÉCHOUÉE</div>';
  });
})();
</script>