---
{"dg-publish":true,"permalink":"/neocom-zorath-77/","tags":["gardenEntry"],"created":"2026-02-28T21:09:16.622+01:00"}
---

<style>@import url('https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Electrolize&family=Share+Tech+Mono&family=Cinzel:wght@400;600;700&display=swap');#nc{all:initial;display:block;max-width:1400px;margin:0 auto;font-family:'Rajdhani',sans-serif;background:#060709;color:#888A98;box-sizing:border-box}#nc *,#nc *::before,#nc *::after{box-sizing:border-box;margin:0;padding:0}#nc p,#nc ul,#nc ol,#nc li,#nc h1,#nc h2,#nc h3,#nc h4,#nc h5,#nc h6{all:unset;display:block}#nc a{text-decoration:none}#nc img{display:inline-block;border:none}</style>

<div id="nc"></div>

<script>
(function(){
var R=document.getElementById('nc');
if(!R)return;
var G='#C8A84B',G2='#6B5520',C='#4FC3F7',RD='#CF3B3B',R2='#FF4444',BG='#060709',BG2='rgba(10,12,18,0.98)',B1='#1A1D26',B2='#262930',T1='#D0D0D8',T2='#888A98',T3='#404455',T4='#252730';
var CSS='@keyframes blink{0%,100%{opacity:1;box-shadow:0 0 6px #4FC3F7}50%{opacity:.25;box-shadow:none}}@keyframes kd{0%,100%{opacity:1;box-shadow:0 0 5px #FF4444}50%{opacity:.2;box-shadow:none}}@keyframes sc{0%{top:0%;opacity:0}5%{opacity:1}95%{opacity:1}100%{top:100%;opacity:0}}@keyframes tscroll{0%{transform:translateY(0)}100%{transform:translateY(-50%)}}@keyframes sfill{0%{width:0}100%{width:100%}}@keyframes fadeout{0%,75%{opacity:1}100%{opacity:0}}@keyframes fadein{0%,75%{opacity:0}100%{opacity:1}}@keyframes pulse{0%,100%{background:rgba(18,0,0,.5);border-left-color:#CF3B3B;box-shadow:none}50%{background:rgba(36,0,0,.7);border-left-color:#FF4444;box-shadow:inset 0 0 18px rgba(207,59,59,.12)}}@keyframes wvanim{0%{height:15%}100%{height:95%}}@keyframes slidein{from{opacity:0;transform:translateX(-4px)}to{opacity:1;transform:translateX(0)}}';
var s=document.createElement('style');s.textContent=CSS;document.head.appendChild(s);
var MIO='https://image.eveonline.com/Corporation/1000082_128.png';
var PORT='https://images.evetech.net/characters/2124123129/portrait?size=512';
var CID=2124123129;
function el(tag,css,inner){var e=document.createElement(tag);if(css)e.style.cssText=css;if(inner!==undefined)e.innerHTML=inner;return e;}
function tx(tag,css,text){var e=el(tag,css);e.textContent=text;return e;}
function img(src,alt,css){var i=el('img',css);i.src=src;i.alt=alt||'';return i;}

/* TOPBAR */
var tb=el('div','display:flex;align-items:center;justify-content:space-between;padding:8px 20px;background:linear-gradient(180deg,#0E1018,#08090E);border:1px solid #1A1D26;border-bottom:2px solid #6B5520;gap:16px;flex-wrap:wrap;position:relative;z-index:10');
var tbl=el('div','display:flex;align-items:center;gap:9px;font-family:Cinzel,serif;font-size:10px;letter-spacing:3.5px;color:#C8A84B;text-shadow:0 0 14px rgba(200,168,75,.35);text-transform:uppercase');
tbl.appendChild(img(MIO,'MIO','width:18px;height:18px;filter:drop-shadow(0 0 6px rgba(200,168,75,.7))'));
tbl.appendChild(document.createTextNode('MIO // Secure Info Terminal // Node 77-A'));
var nav=el('nav','display:flex;align-items:center;gap:2px');
['Character','Archives','Combat','Feeds'].forEach(function(n,i){
  var a=tx('a','padding:4px 13px;font-family:Electrolize,monospace;font-size:8px;letter-spacing:2px;text-transform:uppercase;border:1px solid '+(i===0?'#6B5520':'transparent')+';background:'+(i===0?'rgba(200,168,75,.1)':'transparent')+';color:'+(i===0?'#C8A84B':'#404455')+';cursor:pointer;transition:all .2s',n);
  a.href='#';nav.appendChild(a);
});
var clk=tx('div','font-family:"Share Tech Mono",monospace;font-size:9px;color:#404455;letter-spacing:2px;white-space:nowrap','YC128 // --:--:-- UTC');
clk.id='nc-clk';
tb.appendChild(tbl);tb.appendChild(nav);tb.appendChild(clk);R.appendChild(tb);

/* WINDOW */
var win=el('div','position:relative;background:rgba(10,12,18,0.98);border:1px solid #262930;border-top:2px solid #6B5520;box-shadow:0 20px 60px rgba(0,0,0,.95);overflow:hidden');
win.appendChild(el('div','position:absolute;top:0;right:0;border-style:solid;border-width:0 18px 18px 0;border-color:transparent #6B5520 transparent transparent;z-index:30'));
win.appendChild(el('div','position:absolute;inset:0;background:repeating-linear-gradient(0deg,transparent,transparent 2px,rgba(0,0,0,.05) 2px,rgba(0,0,0,.05) 4px);pointer-events:none;z-index:50;opacity:.5'));

/* TITLEBAR */
var br=el('div','display:flex;align-items:center;justify-content:space-between;padding:10px 20px;background:linear-gradient(180deg,#13151E,#09090E);border-bottom:1px solid #1A1D26;position:relative;z-index:10;gap:12px');
var brl=el('div','display:flex;align-items:center;gap:9px');
brl.appendChild(img(MIO,'','width:16px;height:16px;filter:drop-shadow(0 0 4px rgba(200,168,75,.5))'));
brl.appendChild(tx('span','font-family:Electrolize,monospace;font-size:9px;letter-spacing:3px;text-transform:uppercase;color:#A0A0AE;white-space:nowrap;overflow:hidden;text-overflow:ellipsis','MIO // Secure_Info_Terminal // Node 77-A // Access Level: ALPHA-CLEAR'));
var pill=el('div','display:inline-flex;align-items:center;gap:6px;padding:3px 10px;border:1px solid rgba(79,195,247,.18);background:rgba(79,195,247,.03);font-family:"Share Tech Mono",monospace;font-size:8px;letter-spacing:2px;color:#4FC3F7;flex-shrink:0');
pill.appendChild(el('span','width:5px;height:5px;border-radius:50%;background:#4FC3F7;box-shadow:0 0 6px #4FC3F7;animation:blink 1.8s ease-in-out infinite;display:inline-block;flex-shrink:0'));
pill.appendChild(document.createTextNode('\u00a0LINK SECURE'));
br.appendChild(brl);br.appendChild(pill);win.appendChild(br);

/* BODY */
var body=el('div','display:flex;align-items:stretch;position:relative;z-index:1;min-height:400px');

/* TERMINAL */
var term=el('div','width:200px;flex-shrink:0;background:#000;border-right:1px solid #0C0E14;position:relative;overflow:hidden;-webkit-mask-image:linear-gradient(to bottom,transparent 0%,black 6%,black 94%,transparent 100%);mask-image:linear-gradient(to bottom,transparent 0%,black 6%,black 94%,transparent 100%)');
var tswrap=el('div','position:absolute;top:0;left:0;right:0;padding:14px 12px;animation:tscroll 22s linear infinite');
var TL=[['CONNECTING_TO_NODE_77-A...',''],['ESTABLISHING_NEURAL_LINK...',''],['AUTH_REQUEST_SENT...',''],['WAITING_FOR_RESPONSE *','w'],['MIO_AUTH_RECEIVED...','g'],['SECURE_CHANNEL_ALPHA-7',''],['ANALYZING_FIREWALL_3...','d'],['INJECTING_EXPLOIT...',''],['FIREWALL_BYPASSED...','g'],['WARNING:ELEVATION!','w'],['RE-ROUTING_TRACE...',''],['PACKET_SNIFFING...','d'],['EXTRACTING_SIG...',''],['SUCCESS_ID:ZORATH','g'],['TRACE_INBOUND!','w'],['MIO_PURGE_INIT','w'],['BREACH_SECTOR-G',''],['DATA_MINING_ACTIVE','d'],['REBOOT_SEQ_7722',''],['SIG_VERIFY_LOOP...','d'],['NODE_77A_ALIVE','g'],['ENCRYPTION_AES-256',''],['HANDSHAKE_COMPLETE','g'],['LATENCY: 4ms','g'],['UPLINK_NOMINAL',''],['MIO_WATCH: ACTIVE','w'],['BIOMETRIC_CONFIRMED',''],['CORTEX_LINK: 100%','g'\|'CONNECTING_TO_NODE_77-A...',''],['ESTABLISHING_NEURAL_LINK...',''],['AUTH_REQUEST_SENT...',''],['WAITING_FOR_RESPONSE *','w'],['MIO_AUTH_RECEIVED...','g'],['SECURE_CHANNEL_ALPHA-7',''],['ANALYZING_FIREWALL_3...','d'],['INJECTING_EXPLOIT...',''],['FIREWALL_BYPASSED...','g'],['WARNING:ELEVATION!','w'],['RE-ROUTING_TRACE...',''],['PACKET_SNIFFING...','d'],['EXTRACTING_SIG...',''],['SUCCESS_ID:ZORATH','g'],['TRACE_INBOUND!','w'],['MIO_PURGE_INIT','w'],['BREACH_SECTOR-G',''],['DATA_MINING_ACTIVE','d'],['REBOOT_SEQ_7722',''],['SIG_VERIFY_LOOP...','d'],['NODE_77A_ALIVE','g'],['ENCRYPTION_AES-256',''],['HANDSHAKE_COMPLETE','g'],['LATENCY: 4ms','g'],['UPLINK_NOMINAL',''],['MIO_WATCH: ACTIVE','w'],['BIOMETRIC_CONFIRMED',''],['CORTEX_LINK: 100%','g']];
var tclr={'':'rgba(79,195,247,.45)','w':'rgba(207,59,59,.65)','g':'rgba(200,168,75,.65)','d':'rgba(79,195,247,.18)'};
var tsdw={'':'rgba(79,195,247,.25)','w':'rgba(207,59,59,.25)','g':'rgba(200,168,75,.25)','d':'rgba(79,195,247,.1)'};
for(var rep=0;rep<2;rep++){TL.forEach(function(t){var sp=tx('span','display:block;font-family:"Share Tech Mono",monospace;font-size:8.5px;line-height:1.75;letter-spacing:.3px;color:'+tclr[t[1]]+';text-shadow:0 0 4px '+tsdw[t[1]],(t[1]===''||t[1]==='d'?'> ':'')+t[0]);tswrap.appendChild(sp);});}
term.appendChild(tswrap);body.appendChild(term);

/* CONTENT */
var ct=el('div','flex:1;padding:28px 36px;min-width:0;background:radial-gradient(ellipse at 15% 0%,rgba(200,168,75,.02) 0%,transparent 55%)');
function secLbl(text){var d=el('div','display:flex;align-items:center;gap:8px;font-family:Electrolize,monospace;font-size:9px;letter-spacing:4px;text-transform:uppercase;color:#404455;padding-bottom:7px;border-bottom:1px solid #1A1D26;margin-bottom:13px');var g=el('span','display:inline-block;width:6px;height:6px;background:#6B5520;clip-path:polygon(50% 0%,100% 50%,50% 100%,0% 50%);flex-shrink:0');d.appendChild(g);d.appendChild(document.createTextNode('\u00a0'+text));return d;}
function divdr(){var d=el('div','display:flex;align-items:center;gap:10px;margin:18px 0');d.appendChild(el('span','flex:1;height:1px;background:linear-gradient(90deg,transparent,#262930)'));d.appendChild(el('span','width:6px;height:6px;background:#6B5520;clip-path:polygon(50% 0%,100% 50%,50% 100%,0% 50%)'));d.appendChild(el('span','flex:1;height:1px;background:linear-gradient(90deg,#262930,transparent)'));return d;}

/* NEURAL SYNC */
var sy=el('div','position:relative;border:1px solid #141C28;background:rgba(0,6,16,.55);padding:9px 13px 18px;margin-bottom:18px;font-family:"Share Tech Mono",monospace;font-size:8.5px;letter-spacing:1.5px;color:#252730;overflow:hidden');
sy.appendChild(el('div','position:absolute;top:0;left:0;border-style:solid;border-width:9px 9px 0 0;border-color:#0D2A38 transparent transparent transparent'));
var shd=el('div','display:flex;justify-content:space-between;align-items:center;margin-bottom:7px');
shd.appendChild(tx('span','color:#0D2A38','> INITIALIZING NEURAL PATHWAYS...'));
var sst=el('div','position:relative;height:13px;width:240px');
sst.appendChild(tx('span','position:absolute;right:0;top:0;color:#C8A84B;text-shadow:0 0 5px rgba(200,168,75,.4);animation:fadeout 2.4s ease forwards','SCANNING PILOT SIGNATURE [ WAIT ]'));
sst.appendChild(tx('span','position:absolute;right:0;top:0;color:#4FC3F7;text-shadow:0 0 5px rgba(79,195,247,.5);opacity:0;animation:fadein 2.4s ease forwards','SIGNATURE MATCHED [ SYNC 100% ]'));
shd.appendChild(sst);sy.appendChild(shd);
var str=el('div','height:2px;background:#060C18;overflow:hidden');
str.appendChild(el('div','height:100%;width:0;background:linear-gradient(90deg,transparent,#4FC3F7 60%,rgba(79,195,247,.3));box-shadow:0 0 8px #4FC3F7;animation:sfill 2s ease-out forwards'));
sy.appendChild(str);
var wfw=el('div','position:absolute;bottom:5px;right:10px;display:flex;align-items:flex-end;gap:2px;height:11px');
[.6,.8,.5,.9,.7,.55,.75,.65,.85,.45].forEach(function(sp,i){wfw.appendChild(el('span','display:inline-block;width:2px;background:#4FC3F7;box-shadow:0 0 3px #4FC3F7;border-radius:1px;height:15%;animation:wvanim '+sp+'s ease-in-out '+(i*.11)+'s infinite alternate;opacity:'+(0.4+i*.055)));});
sy.appendChild(wfw);ct.appendChild(sy);

/* ALERT */
var al=el('div','display:flex;align-items:center;justify-content:space-between;gap:14px;padding:11px 15px;border-left:3px solid #CF3B3B;background:rgba(18,0,0,.5);margin-bottom:18px;animation:pulse 2.8s ease-in-out infinite');
var ald=el('div','flex:1');
var alh=el('div','display:flex;align-items:center;gap:7px;font-family:Electrolize,monospace;font-size:9px;letter-spacing:3px;color:#FF4444;text-transform:uppercase;margin-bottom:5px');
alh.innerHTML='<svg width="13" height="13" viewBox="0 0 16 16" fill="none"><path d="M8 1.5L14.5 13.5H1.5L8 1.5Z" stroke="#FF4444" stroke-width="1.2" fill="rgba(255,68,68,0.1)"/><line x1="8" y1="6" x2="8" y2="10" stroke="#FF4444" stroke-width="1.5"/><circle cx="8" cy="12" r="0.9" fill="#FF4444"/></svg>';
alh.appendChild(document.createTextNode('\u00a0RESTRICTED ACCESS PROTOCOL'));
ald.appendChild(alh);
ald.appendChild(tx('div','font-family:Rajdhani,sans-serif;font-size:13px;color:#A8A8B0;line-height:1.4','Monitoring active. Any synaptic deviation is logged by the Ministry of Internal Order.'));
al.appendChild(ald);al.appendChild(img(MIO,'MIO','filter:drop-shadow(0 0 12px rgba(207,59,59,.8));flex-shrink:0;width:46px;height:46px'));
ct.appendChild(al);

/* BIO */
ct.appendChild(secLbl('Biometric Data'));
var bio=el('div','display:flex;border:1px solid #262930;border-top:2px solid #6B5520;background:rgba(0,0,0,.5);margin-bottom:18px;overflow:hidden');
var pp=el('div','position:relative;width:210px;height:210px;flex-shrink:0;background:#000;overflow:hidden;border-right:1px solid #181400');
pp.appendChild(img(PORT,'Ithika Zorath','width:100%;height:100%;object-fit:cover;object-position:top center;display:block'));
pp.appendChild(el('div','position:absolute;left:0;width:100%;height:1px;background:linear-gradient(90deg,transparent,rgba(79,195,247,.7) 40%,rgba(255,255,255,.85) 50%,rgba(79,195,247,.7) 60%,transparent);box-shadow:0 0 8px rgba(79,195,247,.5);animation:sc 3.2s cubic-bezier(.4,0,.2,1) infinite;z-index:10'));
pp.appendChild(el('div','position:absolute;bottom:0;left:0;right:0;height:50px;background:linear-gradient(transparent,rgba(0,0,0,.95));z-index:5'));
pp.appendChild(tx('div','position:absolute;bottom:5px;left:8px;font-family:"Share Tech Mono",monospace;font-size:7px;color:rgba(107,85,32,.75);letter-spacing:2px;z-index:15','MIO // CAPSULEER'));
var bi=el('div','padding:14px 20px;flex:1;display:flex;flex-direction:column;justify-content:center');
bi.appendChild(tx('div','font-family:Cinzel,serif;font-size:7.5px;letter-spacing:4px;color:#C8A84B;text-transform:uppercase;border-bottom:1px solid rgba(200,168,75,.1);padding-bottom:7px;margin-bottom:9px;opacity:.75','Identification Records'));
var tbl2=el('table','width:100%;border-collapse:collapse');
[['Designation','font-family:Rajdhani,sans-serif;font-size:22px;font-weight:700;color:#EBEBF0;letter-spacing:.5px','Ithika Zorath'],['Bio-Tech','font-family:"Share Tech Mono",monospace;font-size:12px;color:\|'Designation','font-family:Rajdhani,sans-serif;font-size:22px;font-weight:700;color:#EBEBF0;letter-spacing:.5px','Ithika Zorath'],['Bio-Tech','font-family:"Share Tech Mono",monospace;font-size:12px;color:#4FC3F7','__capsuleer__'],['Origin','font-family:Rajdhani,sans-serif;font-size:14px;color:#808090','Nafomeh III'],['Allegiance','font-family:Cinzel,serif;font-size:14px;color:#C8A84B','House Tash-Murkon'],['Timestamp','font-family:"Share Tech Mono",monospace;font-size:10px;color:#404455;letter-spacing:1px','YC128.02']].forEach(function(r){
  var tr=el('tr','border-bottom:1px solid rgba(200,168,75,.05)');
  tr.appendChild(tx('td','font-family:Electrolize,monospace;font-size:7.5px;letter-spacing:2px;color:#404455;text-transform:uppercase;width:105px;white-space:nowrap;padding:5px 0;border:none;vertical-align:middle',r[0]));
  var vtd=el('td',r[1]+';padding:5px 0;border:none;vertical-align:middle');
  if(r[2]==='__capsuleer__'){vtd.textContent='Capsuleer';var sp=tx('span','color:rgba(79,195,247,.3);margin-left:5px','[ ACTIVE ]');vtd.appendChild(sp);}else{vtd.textContent=r[2];}
  tr.appendChild(vtd);tbl2.appendChild(tr);
});
bi.appendChild(tbl2);bio.appendChild(pp);bio.appendChild(bi);ct.appendChild(bio);

/* INDEX */
ct.appendChild(secLbl('Index Manager'));
var ix=el('div','border:1px solid #262930;background:rgba(0,0,0,.62);margin-bottom:18px;overflow:hidden');
function ixHdr(lbl,sep){var h=el('div','display:flex;align-items:center;gap:8px;padding:5px 13px;background:linear-gradient(90deg,rgba(200,168,75,.07),rgba(200,168,75,.015) 70%,transparent);border-bottom:1px solid rgba(200,168,75,.12);font-family:Electrolize,monospace;font-size:8.5px;letter-spacing:3px;color:#C8A84B'+(sep?';border-top:1px solid rgba(200,168,75,.08)':''));var g=el('span','width:6px;height:6px;background:#6B5520;clip-path:polygon(50% 0%,100% 50%,50% 100%,0% 50%);display:inline-block;flex-shrink:0');h.appendChild(g);h.appendChild(document.createTextNode('\u00a0'+lbl));return h;}
function ixFld(lbl){var f=el('div','display:flex;align-items:center;gap:7px;padding:5px 13px 5px 18px;border-bottom:1px solid rgba(255,255,255,.035);background:rgba(255,255,255,.004);font-family:Electrolize,monospace;font-size:9px;letter-spacing:2px;color:#404455;text-transform:uppercase');f.innerHTML='<svg width="11" height="11" viewBox="0 0 14 14"><path d="M1 3.5L1 12L13 12L13 3.5L7 3.5L6 1.5L1 1.5Z" fill="#141418" stroke="#2A2D38" stroke-width="0.8"/></svg>';f.appendChild(document.createTextNode('\u00a0'+lbl));return f;}
function ixRow(href,lbl,badge,btype,meta,ic){
  var a=el('a','display:flex;align-items:center;gap:8px;padding:10px 16px 10px 32px;border-bottom:1px solid rgba(255,255,255,.022);border-left:3px solid transparent;cursor:pointer;transition:background .15s,border-left-color .15s;color:inherit');
  a.href=href;
  var svg=document.createElementNS('http://www.w3.org/2000/svg','svg');svg.setAttribute('width','12');svg.setAttribute('height','12');svg.setAttribute('viewBox','0 0 14 14');
  var rc=document.createElementNS('http://www.w3.org/2000/svg','rect');rc.setAttribute('x','1');rc.setAttribute('y','1');rc.setAttribute('width','9');rc.setAttribute('height','12');rc.setAttribute('rx','0.5');rc.setAttribute('fill',ic==='c'?'#061420':'#100E04');rc.setAttribute('stroke',ic==='c'?'#4FC3F7':'#C8A84B');rc.setAttribute('stroke-width','0.8');svg.appendChild(rc);
  ['4','6','8'].forEach(function(y,i){var ln=document.createElementNS('http://www.w3.org/2000/svg','line');ln.setAttribute('x1','3');ln.setAttribute('y1',y);ln.setAttribute('x2',i===2?'6':'8');ln.setAttribute('y2',y);ln.setAttribute('stroke',ic==='c'?'#4FC3F7':'#C8A84B');ln.setAttribute('stroke-width',i===0?'0.6':'0.5');ln.setAttribute('opacity',i===0?'0.7':'0.4');svg.appendChild(ln);});
  var nm=tx('span','flex:1;font-family:Rajdhani,sans-serif;font-size:14px;color:#B8B8C4',lbl);
  var bg=tx('span','font-family:"Share Tech Mono",monospace;font-size:7.5px;letter-spacing:1.5px;padding:2px 6px;white-space:nowrap;border:1px solid '+(btype==='r'?'#CF3B3B':'#6B5520')+';color:'+(btype==='r'?'#CF3B3B':'#C8A84B'),badge);
  var mt=tx('span','font-family:"Share Tech Mono",monospace;font-size:8.5px;color:#404455;letter-spacing:1px;text-align:right;white-space:nowrap;min-width:65px',meta);
  a.appendChild(svg);a.appendChild(nm);a.appendChild(bg);a.appendChild(mt);
  a.addEventListener('mouseenter',function(){a.style.background='rgba(79,195,247,.022)';a.style.borderLeftColor='rgba(79,195,247,.28)';nm.style.color='#4FC3F7';});
  a.addEventListener('mouseleave',function(){a.style.background='';a.style.borderLeftColor='transparent';nm.style.color='#B8B8C4';});
  return a;
}
ix.appendChild(ixHdr('SYS.LANG // ENGLISH',false));ix.appendChild(ixFld('MIO Archives'));
ix.appendChild(ixRow('/notes/en-archives-of-house-tash-murkon','EN \u2014 ARCHIVES OF HOUSE TASH-MURKON','CLASSIFIED','r','2.4 TB','c'));
ix.appendChild(ixRow('/notes/en-logbook-02-yc128','EN \u2014 Logbook 02-YC128','RESTRICTED','g','02 / YC128','g'));
ix.appendChild(ixHdr('SYS.LANG // FRAN\u00c7AIS',true));ix.appendChild(ixFld('Archives MIO'));
ix.appendChild(ixRow('/notes/fr-archives-of-house-tash-murkon','FR \u2014 ARCHIVES OF HOUSE TASH-MURKON','CLASSIFI\u00c9','r','2.4 TB','c'));
ix.appendChild(ixRow('/notes/fr-journal-de-bord-02-yc128','FR \u2014 Journal de bord 02-YC128','RESTREINT','g','02 / YC128','g'));
ct.appendChild(ix);ct.appendChild(divdr());

/* KILLBOARD */
ct.appendChild(secLbl('Combat Registry // Live Feed'));
var kb=el('div','border:1px solid #262930;background:rgba(0,0,0,.58);margin-bottom:18px;overflow:hidden');
var kbh=el('div','display:flex;align-items:center;justify-content:space-between;padding:7px 13px;background:linear-gradient(90deg,rgba(207,59,59,.07),transparent);border-bottom:1px solid rgba(207,59,59,.12);gap:10px');
var kbhl=el('div','display:flex;align-items:center;gap:7px');
kbhl.appendChild(el('span','width:5px;height:5px;border-radius:50%;background:#FF4444;box-shadow:0 0 5px #FF4444;animation:kd 1.5s ease-in-out infinite;display:inline-block'));
kbhl.appendChild(tx('span','font-family:Electrolize,monospace;font-size:8.5px;letter-spacing:2px;color:#FF4444;text-transform:uppercase','BLOOD_TITHE_METRICS // ITHIKA ZORATH'));
var kbhr=el('div','display:flex;align-items:center;gap:9px');
kbhr.appendChild(img('https://images.evetech.net/characters/2124123129/portrait?size=32','','border:1px solid #1A1A1A;width:20px;height:20px'));
var kbha=tx('a','font-family:"Share Tech Mono",monospace;font-size:8px;color:#404455;letter-spacing:1px','VIEW ALL \u2192');kbha.href='https://zkillboard.com/character/2124123129/';kbha.target='_blank';kbhr.appendChild(kbha);
kbh.appendChild(kbhl);kbh.appendChild(kbhr);kb.appendChild(kbh);
var ksr=el('div','display:flex;background:rgba(0,0,0,.38);border-bottom:1px solid #1A1D26');
[['nc-kills','Kills','#C8A84B'],['nc-losses','Losses','\|'nc-kills','Kills','#C8A84B'],['nc-losses','Losses','#FF4444'],['nc-danger','Danger','#4FC3F7'],['nc-isk','ISK Destroyed','#C8A84B']].forEach(function(st,i){
  var kst=el('div','flex:1;text-align:center;padding:11px 8px;border-right:1px solid #1A1D26'+(i===3?';border-right:none':''));
  var v=tx('span','display:block;font-family:"Share Tech Mono",monospace;font-size:17px;margin-bottom:2px;color:'+st[2],'\u2014');v.id=st[0];
  kst.appendChild(v);kst.appendChild(tx('span','display:block;font-family:Electrolize,monospace;font-size:7.5px;letter-spacing:2px;color:#404455;text-transform:uppercase',st[1]));
  ksr.appendChild(kst);
});
kb.appendChild(ksr);
var kbl=el('div','max-height:270px;overflow-y:auto');kbl.id='nc-kbl';
kbl.innerHTML='<div style="text-align:center;padding:28px;font-family:\'Share Tech Mono\',monospace;font-size:8.5px;color:#252730;letter-spacing:3px">\u27f3 RETRIEVING DATA...</div>';
kb.appendChild(kbl);ct.appendChild(kb);ct.appendChild(divdr());

/* FEEDS */
ct.appendChild(secLbl('External Live Feeds'));
var fds=el('div','display:grid;grid-template-columns:1fr 1fr;gap:12px');
function feedBtn(href,sub,title,tc,bc,hbc,hbg){
  var a=el('a','display:block;padding:16px 18px;border:1px solid '+bc+';background:rgba(5,6,10,.9);position:relative;overflow:hidden;transition:all .25s;clip-path:polygon(0 0,calc(100% - 9px) 0,100% 9px,100% 100%,9px 100%,0 calc(100% - 9px))');
  a.href=href;a.target='_blank';
  a.appendChild(tx('span','display:block;font-family:Electrolize,monospace;font-size:8px;letter-spacing:3px;text-transform:uppercase;margin-bottom:5px;opacity:.65;color:'+tc,sub));
  a.appendChild(tx('span','display:block;font-family:Cinzel,serif;font-size:11px;letter-spacing:2px;font-weight:600;color:#CCCCDA',title));
  a.addEventListener('mouseenter',function(){a.style.borderColor=hbc;a.style.background=hbg;});
  a.addEventListener('mouseleave',function(){a.style.borderColor=bc;a.style.background='rgba(5,6,10,.9)';});
  return a;
}
fds.appendChild(feedBtn('https://zkillboard.com/character/2124123129/','Combat Registry','[ Blood Tithe Metrics ]','#FF4444','#3A1515','rgba(207,59,59,.45)','rgba(207,59,59,.035)'));
fds.appendChild(feedBtn('https://abysstracker.com/u/ithika-zorath','Deadspace Anomalies','[ Abyssal Telemetry ]','#4FC3F7','#0A1E28','rgba(79,195,247,.38)','rgba(79,195,247,.035)'));
ct.appendChild(fds);

/* FOOTER */
var ft=el('div','display:flex;align-items:center;justify-content:space-between;padding:7px 15px;border:1px solid #1A1D26;border-top:1px solid #262930;background:rgba(0,0,0,.55);margin-top:18px');
ft.appendChild(tx('span','font-family:"Share Tech Mono",monospace;font-size:7.5px;letter-spacing:2px;color:#252730','MIO // SECURE TERMINAL // NODE 77-A // ACCESS ALPHA-CLEAR'));
ft.appendChild(tx('span','font-family:"Share Tech Mono",monospace;font-size:7.5px;letter-spacing:2px;color:#252730','YC128.02 \u2014 ITHIKA ZORATH'));
ct.appendChild(ft);

body.appendChild(ct);win.appendChild(body);R.appendChild(win);

/* RESPONSIVE */
function rsp(){if(window.innerWidth<=700){body.style.flexDirection='column';term.style.width='100%';term.style.height='70px';term.style.borderRight='none';term.style.borderBottom='1px solid #1A1D26';ct.style.padding='14px';pp.style.width='100%';pp.style.height='140px';fds.style.gridTemplateColumns='1fr';}else{body.style.flexDirection='';term.style.width='200px';term.style.height='';term.style.borderRight='1px solid #0C0E14';term.style.borderBottom='none';ct.style.padding='28px 36px';pp.style.width='210px';pp.style.height='210px';fds.style.gridTemplateColumns='1fr 1fr';}}
window.addEventListener('resize',rsp);rsp();

/* CLOCK */
var ck=document.getElementById('nc-clk');
function ec(){var n=new Date();return'YC128 // '+String(n.getUTCHours()).padStart(2,'0')+':'+String(n.getUTCMinutes()).padStart(2,'0')+':'+String(n.getUTCSeconds()).padStart(2,'0')+' UTC';}
if(ck){ck.textContent=ec();setInterval(function(){ck.textContent=ec();},1000);}

/* KILLBOARD API */
function fmtI(v){if(v>=1e9)return(v/1e9).toFixed(1)+' B';if(v>=1e6)return(v/1e6).toFixed(1)+' M';if(v>=1e3)return(v/1e3).toFixed(1)+' K';return String(Math.round(v));}
function tago(d){var s=Math.floor((Date.now()-new Date(d))/1000);if(s<60)return s+'s ago';if(s<3600)return Math.floor(s/60)+'m ago';if(s<86400)return Math.floor(s/3600)+'h ago';return Math.floor(s/86400)+'d ago';}
function sclr(s){return s>=0.5?'#4FC870':s>=0.1?'#E8A020':'#FF4444';}
fetch('https://zkillboard.com/api/stats/characterID/'+CID+'/').then(function(r){return r.json();}).then(function(s){
  var ek=document.getElementById('nc-kills'),el2=document.getElementById('nc-losses'),ed=document.getElementById('nc-danger'),ei=document.getElementById('nc-isk');
  if(ek)ek.textContent=s.shipsDestroyed||0;
  if(el2)el2.textContent=s.shipsLost||0;
  if(ed){var dr=s.dangerRatio||0;ed.textContent=dr+'%';ed.style.color=dr>50?'#FF4444':'#4FC3F7';}
  if(ei)ei.textContent=fmtI(s.iskDestroyed||0);
}).catch(function(){});
fetch('https://zkillboard.com/api/kills/characterID/'+CID+'/').then(function(r){return r.json();}).then(function(kills){
  if(!Array.isArray(kills)||!kills.length){kbl.innerHTML='<div style="text-align:center;padding:28px;font-family:\'Share Tech Mono\',monospace;font-size:8.5px;color:#252730;letter-spacing:3px">// NO ENGAGEMENTS RECORDED</div>';return;}
  kbl.innerHTML='';
  kills.slice(0,8).forEach(function(k,i){
    var row=el('div','display:flex;align-items:center;gap:9px;padding:7px 13px;border-bottom:1px solid rgba(255,255,255,.025);border-left:3px solid #1A1D26;cursor:pointer;transition:background .15s;animation:slidein .3s ease '+(i*.07)+'s both');
    var thumb=el('div','width:36px;height:36px;flex-shrink:0;border:1px solid #181818;background:#000;overflow:hidden');
    var thi=img('https://images.evetech.net/types/670/render?size=64','','width:100%;height:100%;display:block;object-fit:cover');
    thumb.appendChild(thi);
    var info=el('div','flex:1;min-width:0');
    var kvn=tx('div','font-family:Rajdhani,sans-serif;font-size:14px;font-weight:600;color:#484858;white-space:nowrap;overflow:hidden;text-overflow:ellipsis','Loading...');
    var ksb=el('div','font-family:"Share Tech Mono",monospace;font-size:8.5px;margin-top:2px;display:flex;gap:9px;flex-wrap:wrap');
    info.appendChild(kvn);info.appendChild(ksb);
    var badge=tx('span','font-family:"Share Tech Mono",monospace;font-size:7.5px;letter-spacing:1.5px;padding:2px 6px;flex-shrink:0;color:#C8A84B;border:1px solid rgba(200,168,75,.28);background:rgba(200,168,75,.03)','KILL');
    row.appendChild(thumb);row.appendChild(info);row.appendChild(badge);
    row.addEventListener('click',function(){window.open('https://zkillboard.com/kill/'+k.killmail_id+'/','_blank');});
    row.addEventListener('mouseenter',function(){row.style.background='rgba(200,168,75,.025)';});
    row.addEventListener('mouseleave',function(){row.style.background='';});
    kbl.appendChild(row);
    fetch('https://esi.evetech.net/latest/killmails/'+k.killmail_id+'/'+k.zkb.hash+'/').then(function(r){return r.json();}).then(function(km){
      return Promise.all([
        fetch('https://esi.evetech.net/latest/universe/types/'+km.victim.ship_type_id+'/?language=en').then(function(r){return r.json();}),
        fetch('https://esi.evetech.net/latest/universe/systems/'+km.solar_system_id+'/').then(function(r){return r.json();}),
        km.victim.character_id?fetch('https://esi.evetech.net/latest/characters/'+km.victim.character_id+'/').then(function(r){return r.json();}):Promise.resolve({name:'Unknown'})
      ]).then(function(res){
        var ship=res[0],sys=res[1],vic=res[2];
        var isKill=km.attackers&&km.attackers.some(function(a){return a.character_id===CID;});
        var sec=sys.security_status||0;
        thi.src='https://images.evetech.net/types/'+km.victim.ship_type_id+'/render?size=64';
        kvn.style.color='#D8D8E0';kvn.textContent=vic.name||'Unknown';
        var shipSp=tx('span','font-size:11px;color:#404450',' \u2014 '+(ship.name||'?'));kvn.appendChild(shipSp);
        ksb.appendChild(tx('span','color:'+sclr(sec),sys.name+' ('+sec.toFixed(1)+')'));
        ksb.appendChild(tx('span','color:#C8A84B',' '+fmtI(k.zkb.totalValue||0)+' ISK'));
        ksb.appendChild(tx('span','color:#404455',' '+tago(km.killmail_time)));
        if(isKill){badge.textContent='KILL';badge.style.color='#C8A84B';badge.style.borderColor='rgba(200,168,75,.28)';row.style.borderLeftColor='rgba(200,168,75,.45)';}
        else{badge.textContent='LOSS';badge.style.color='#FF4444';badge.style.borderColor='rgba(207,59,59,.28)';badge.style.background='rgba(207,59,59,.03)';row.style.borderLeftColor='rgba(207,59,59,.45)';}
      });
    }).catch(function(){kvn.textContent='[ESI UNAVAILABLE]';kvn.style.color='#404455';});
  });
}).catch(function(){kbl.innerHTML='<div style="text-align:center;padding:28px;font-family:\'Share Tech Mono\',monospace;font-size:8.5px;color:#252730;letter-spacing:3px">\u2717 CONNECTION FAILED</div>';});
})();
</script>