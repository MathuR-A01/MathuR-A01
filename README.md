<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0"/>
<title>Aayush Mathur · Full Stack Developer & Tester · MathuR-A01</title>
<meta name="description" content="Full Stack Web Developer & Software Tester with 3+ years experience. Laravel, React.js, PHP, MySQL, n8n AI Automation."/>
<meta property="og:title" content="Aayush Mathur · Full Stack Developer & Tester"/>
<meta property="og:description" content="Laravel · React.js · PHP · n8n · AI Automation · Manual Testing"/>
<meta property="og:url" content="https://mathuR-A01.vercel.app"/>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800;900&family=JetBrains+Mono:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
:root{
  --bg:#06080f;--s1:#0b0e1a;--s2:#0f1322;--s3:#141929;
  --bd:#1e2540;--bd2:#2a3460;
  --pu:#a855f7;--pu2:#c084fc;--pu3:#7c3aed;
  --tl:#2dd4bf;--tl2:#5eead4;--tl3:#0d9488;
  --pk:#f472b6;--am:#fbbf24;--or:#fb923c;
  --wh:#eef2ff;--tx:#c4cde8;--mu:#5a6882;--mu2:#3d4f6a;
  --mono:'JetBrains Mono',monospace;
  --body:'Outfit',sans-serif;
}
*{box-sizing:border-box;margin:0;padding:0;scroll-behavior:smooth}
html{overflow-x:hidden}
body{background:var(--bg);color:var(--tx);font-family:var(--body);min-height:100vh;overflow-x:hidden}

/* ── CANVAS BG ── */
#bgCanvas{position:fixed;inset:0;width:100%;height:100%;pointer-events:none;z-index:0;opacity:0.45}

/* ── SCROLLBAR ── */
::-webkit-scrollbar{width:4px}
::-webkit-scrollbar-track{background:var(--bg)}
::-webkit-scrollbar-thumb{background:var(--pu3);border-radius:2px}

/* ── NAV ── */
nav{
  position:fixed;top:0;left:0;right:0;z-index:100;
  background:rgba(6,8,15,0.85);
  backdrop-filter:blur(12px);
  border-bottom:1px solid var(--bd);
  padding:0 2rem;height:56px;
  display:flex;align-items:center;justify-content:space-between;
}
.nav-brand{font-family:var(--mono);font-size:13px;color:var(--tl);letter-spacing:2px}
.nav-brand span{color:var(--pu)}
.nav-links{display:flex;gap:24px}
.nav-links a{font-family:var(--mono);font-size:10px;letter-spacing:1.5px;text-transform:uppercase;color:var(--mu);text-decoration:none;transition:color .2s}
.nav-links a:hover{color:var(--tl)}
.nav-dot{width:6px;height:6px;border-radius:50%;background:var(--tl);animation:ndot 1.8s ease-in-out infinite}
@keyframes ndot{0%,100%{opacity:1}50%{opacity:.2}}

/* ── LAYOUT ── */
.page{position:relative;z-index:1;padding-top:56px}
.wrap{max-width:900px;margin:0 auto;padding:0 2rem}

/* ── HERO ── */
.hero{
  padding:5rem 2rem 3.5rem;
  position:relative;
  border-bottom:1px solid var(--bd);
  overflow:hidden;
}
.hero-wrap{max-width:900px;margin:0 auto;position:relative}
.hero-geo{position:absolute;top:-100px;right:-100px;width:420px;height:420px;border-radius:50%;border:1px solid rgba(168,85,247,.1);pointer-events:none}
.hero-geo::before{content:'';position:absolute;inset:50px;border-radius:50%;border:1px solid rgba(45,212,191,.07)}
.hero-geo::after{content:'';position:absolute;inset:100px;border-radius:50%;border:1px solid rgba(168,85,247,.05)}
.crn{position:absolute;width:24px;height:24px;pointer-events:none}
.crn.a{top:24px;left:24px;border-top:2px solid var(--pu);border-left:2px solid var(--pu)}
.crn.b{top:24px;right:24px;border-top:2px solid var(--tl);border-right:2px solid var(--tl)}
.crn.c{bottom:0;left:24px;border-bottom:2px solid var(--tl);border-left:2px solid var(--tl)}
.crn.d{bottom:0;right:24px;border-bottom:2px solid var(--pu);border-right:2px solid var(--pu)}

.chip{display:inline-flex;align-items:center;gap:8px;font-family:var(--mono);font-size:10px;letter-spacing:2.5px;color:var(--tl);border:1px solid rgba(45,212,191,.3);border-radius:20px;padding:5px 16px;margin-bottom:1.5rem}
.dot-pulse{width:7px;height:7px;border-radius:50%;background:var(--tl);animation:dp 1.7s ease-in-out infinite}
@keyframes dp{0%,100%{opacity:1;transform:scale(1)}50%{opacity:.2;transform:scale(.5)}}

.hname{font-size:clamp(2.6rem,6vw,4.2rem);font-weight:900;line-height:.9;letter-spacing:-3px;color:var(--wh);margin-bottom:.2rem}
.hname .ghost{color:transparent;-webkit-text-stroke:2px var(--pu)}
.hsub{font-size:clamp(1rem,2.5vw,1.6rem);font-weight:600;color:var(--tl);letter-spacing:-1px;margin-bottom:.8rem}
.hrole{font-family:var(--mono);font-size:12px;letter-spacing:2px;color:var(--pu2);margin-bottom:1.4rem;display:flex;align-items:center;gap:8px;min-height:20px}
.hrole::before{content:'';width:28px;height:1px;background:var(--pu);opacity:.6;flex-shrink:0}
.hexp-badge{display:inline-flex;align-items:center;gap:6px;font-family:var(--mono);font-size:10px;letter-spacing:1px;padding:4px 12px;border-radius:3px;background:rgba(251,191,36,.08);border:1px solid rgba(251,191,36,.3);color:var(--am);margin-bottom:1.4rem}
.divg{width:100%;height:1px;background:linear-gradient(to right,transparent,var(--pu),var(--tl),transparent);opacity:.3;margin-bottom:1.6rem}
.hbio{font-size:15px;font-weight:400;line-height:1.85;color:#a0b0cc;max-width:640px;margin-bottom:.9rem}
.hbio strong{color:var(--pu2);font-weight:600}
.hbio em{color:var(--tl2);font-style:normal}
.hmeta{display:flex;flex-wrap:wrap;gap:16px;font-family:var(--mono);font-size:11px;color:var(--mu);margin-bottom:2rem}
.hmeta a{display:flex;align-items:center;gap:5px;color:var(--tx);text-decoration:none;transition:color .2s}
.hmeta a:hover{color:var(--tl)}
.md{width:4px;height:4px;border-radius:50%;background:var(--tl);flex-shrink:0}
.hero-btns{display:flex;flex-wrap:wrap;gap:10px}
.btn{font-family:var(--mono);font-size:10.5px;letter-spacing:1.5px;text-transform:uppercase;padding:10px 22px;border-radius:3px;border:1px solid;cursor:pointer;transition:all .18s;text-decoration:none;display:inline-flex;align-items:center;gap:7px}
.bp{border-color:var(--pu);color:var(--pu);background:rgba(168,85,247,.07)}
.bp:hover{background:rgba(168,85,247,.22);box-shadow:0 0 24px rgba(168,85,247,.35);transform:translateY(-2px)}
.bt{border-color:var(--tl);color:var(--tl);background:rgba(45,212,191,.07)}
.bt:hover{background:rgba(45,212,191,.22);box-shadow:0 0 22px rgba(45,212,191,.3);transform:translateY(-2px)}
.bw{border-color:var(--bd2);color:var(--mu);background:var(--s2)}
.bw:hover{border-color:var(--wh);color:var(--wh);transform:translateY(-2px)}

/* ── STATS BAR ── */
.stats-bar{background:var(--s1);border-bottom:1px solid var(--bd);padding:1.4rem 2rem}
.stats-inner{max-width:900px;margin:0 auto;display:grid;grid-template-columns:repeat(4,1fr);gap:1rem}
.scard{text-align:center;padding:.8rem;border-radius:4px;border:1px solid var(--bd);background:var(--s2);position:relative;overflow:hidden;transition:transform .2s}
.scard:hover{transform:translateY(-2px)}
.scard::after{content:'';position:absolute;bottom:0;left:0;right:0;height:2px}
.scard.tl::after{background:linear-gradient(to right,transparent,var(--tl),transparent)}
.scard.pu::after{background:linear-gradient(to right,transparent,var(--pu),transparent)}
.scard.pk::after{background:linear-gradient(to right,transparent,var(--pk),transparent)}
.scard.am::after{background:linear-gradient(to right,transparent,var(--am),transparent)}
.snum{font-size:1.9rem;font-weight:900;line-height:1;margin-bottom:3px}
.snum.tl{color:var(--tl)}.snum.pu{color:var(--pu)}.snum.pk{color:var(--pk)}.snum.am{color:var(--am)}
.slbl{font-family:var(--mono);font-size:9px;letter-spacing:1.5px;color:var(--mu);text-transform:uppercase}

/* ── SECTIONS ── */
section{padding:3rem 0}
section+section{border-top:1px solid var(--bd)}

/* ── SECTION HEADER ── */
.sh{display:flex;align-items:center;gap:12px;margin-bottom:1.5rem}
.sh-num{font-family:var(--mono);font-size:9px;color:var(--mu2);letter-spacing:1px}
.sh-lbl{font-family:var(--mono);font-size:9.5px;letter-spacing:3px;text-transform:uppercase;white-space:nowrap}
.sh-lbl.pu{color:var(--pu)}.sh-lbl.tl{color:var(--tl)}.sh-lbl.pk{color:var(--pk)}.sh-lbl.am{color:var(--am)}.sh-lbl.or{color:var(--or)}
.sh-line{flex:1;height:1px}
.sh-line.pu{background:linear-gradient(to right,rgba(168,85,247,.4),transparent)}
.sh-line.tl{background:linear-gradient(to right,rgba(45,212,191,.4),transparent)}
.sh-line.pk{background:linear-gradient(to right,rgba(244,114,182,.4),transparent)}
.sh-line.am{background:linear-gradient(to right,rgba(251,191,36,.4),transparent)}
.sh-line.or{background:linear-gradient(to right,rgba(251,146,60,.4),transparent)}

/* ── TERMINAL ── */
.term{background:#050810;border:1px solid var(--bd);border-radius:6px;overflow:hidden;margin-bottom:1.5rem}
.tbar{background:var(--s2);border-bottom:1px solid var(--bd);padding:8px 14px;display:flex;align-items:center;gap:7px}
.td{width:11px;height:11px;border-radius:50%}
.ttl{font-family:var(--mono);font-size:11px;color:var(--mu);flex:1;text-align:center;letter-spacing:1px}
.tb{padding:1.2rem 1.5rem;font-family:var(--mono);font-size:13px;line-height:2.2}
.tp{color:var(--tl)}.tk{color:var(--pu2)}.tv{color:var(--tl2)}.tc{color:var(--mu)}
.tw{color:var(--wh)}.tam{color:var(--am)}.tpk{color:var(--pk)}.tor{color:var(--or)}
.tcur{display:inline-block;width:8px;height:15px;background:var(--tl);vertical-align:middle;margin-left:3px;animation:tcur 1s step-end infinite}
@keyframes tcur{0%,100%{opacity:1}50%{opacity:0}}

/* ── CARDS ── */
.card{background:var(--s1);border:1px solid var(--bd);border-radius:5px;padding:1.4rem 1.5rem;position:relative;overflow:hidden;transition:border-color .22s,box-shadow .22s}
.card:hover{border-color:var(--bd2)}
.card.hpu:hover{border-color:rgba(168,85,247,.55);box-shadow:0 0 24px rgba(168,85,247,.08)}
.card.htl:hover{border-color:rgba(45,212,191,.55);box-shadow:0 0 24px rgba(45,212,191,.08)}
.card.ham:hover{border-color:rgba(251,191,36,.5);box-shadow:0 0 24px rgba(251,191,36,.07)}
.abar{position:absolute;top:0;left:0;right:0;height:2px;border-radius:5px 5px 0 0}
.abar.pu{background:linear-gradient(to right,var(--pu3),var(--pu),transparent)}
.abar.tl{background:linear-gradient(to right,var(--tl3),var(--tl),transparent)}
.abar.pk{background:linear-gradient(to right,#be185d,var(--pk),transparent)}
.abar.am{background:linear-gradient(to right,#b45309,var(--am),transparent)}
.abar.or{background:linear-gradient(to right,#c2410c,var(--or),transparent)}
.clbl{font-family:var(--mono);font-size:9px;letter-spacing:2.5px;text-transform:uppercase;margin-bottom:.6rem}
.clbl.pu{color:var(--pu)}.clbl.tl{color:var(--tl)}.clbl.pk{color:var(--pk)}.clbl.am{color:var(--am)}.clbl.or{color:var(--or)}
.ctitle{font-size:15px;font-weight:700;color:var(--wh);margin-bottom:.3rem}
.cbody{font-size:13px;font-weight:300;color:#7888aa;line-height:1.65}

/* ── GRIDS ── */
.g2{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:1rem}
.g3{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:.9rem}
.g4{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:.8rem}
@media(max-width:640px){.g2,.g3,.g4{grid-template-columns:1fr}.stats-inner{grid-template-columns:repeat(2,1fr)}}

/* ── BADGES ── */
.bgs{display:flex;flex-wrap:wrap;gap:7px;margin-bottom:1rem}
.bg{font-family:var(--mono);font-size:11px;padding:5px 13px;border-radius:3px;border:1px solid;transition:all .18s;cursor:default;user-select:none}
.bg.pu{border-color:rgba(168,85,247,.4);color:var(--pu2);background:rgba(168,85,247,.07)}
.bg.tl{border-color:rgba(45,212,191,.4);color:var(--tl2);background:rgba(45,212,191,.07)}
.bg.pk{border-color:rgba(244,114,182,.4);color:var(--pk);background:rgba(244,114,182,.07)}
.bg.am{border-color:rgba(251,191,36,.4);color:var(--am);background:rgba(251,191,36,.07)}
.bg.or{border-color:rgba(251,146,60,.4);color:var(--or);background:rgba(251,146,60,.07)}
.bg.nu{border-color:var(--bd);color:var(--mu);background:var(--s2)}
.bg:hover{transform:translateY(-2px);filter:brightness(1.4)}
.skill-group-title{font-family:var(--mono);font-size:9.5px;letter-spacing:2px;text-transform:uppercase;color:var(--mu);padding:5px 10px;background:var(--s2);border:1px solid var(--bd);border-radius:3px;margin-bottom:.8rem;display:inline-block}

/* ── PROFICIENCY ── */
.prow{display:flex;align-items:center;gap:10px;margin-bottom:10px}
.pnm{font-family:var(--mono);font-size:11px;color:var(--mu);width:140px;flex-shrink:0}
.ptr{flex:1;height:3px;background:var(--s3);border-radius:2px;overflow:hidden}
.pfl{height:100%;border-radius:2px;width:0;transition:width 1.4s cubic-bezier(.34,1.4,.64,1)}
.ppc{font-family:var(--mono);font-size:10px;color:var(--mu2);width:34px;text-align:right;flex-shrink:0}

/* ── PROJECT CARDS ── */
.pcard{background:var(--s1);border:1px solid var(--bd);border-radius:5px;padding:1.3rem;transition:all .22s;position:relative;overflow:hidden;cursor:pointer}
.pcard::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(to right,transparent,var(--pu),var(--tl),transparent);opacity:0;transition:opacity .22s}
.pcard:hover{border-color:var(--bd2);transform:translateY(-3px);box-shadow:0 8px 32px rgba(0,0,0,.4)}
.pcard:hover::before{opacity:.7}
.ptag{font-family:var(--mono);font-size:9px;letter-spacing:2px;text-transform:uppercase;padding:3px 9px;border-radius:2px;margin-bottom:.8rem;display:inline-block}
.ptag.pu{background:rgba(168,85,247,.12);color:var(--pu2);border:1px solid rgba(168,85,247,.25)}
.ptag.tl{background:rgba(45,212,191,.12);color:var(--tl2);border:1px solid rgba(45,212,191,.25)}
.ptag.pk{background:rgba(244,114,182,.12);color:var(--pk);border:1px solid rgba(244,114,182,.25)}
.ptag.am{background:rgba(251,191,36,.12);color:var(--am);border:1px solid rgba(251,191,36,.25)}
.ptag.or{background:rgba(251,146,60,.12);color:var(--or);border:1px solid rgba(251,146,60,.25)}
.pc-title{font-size:14px;font-weight:700;color:var(--wh);margin-bottom:.3rem}
.pc-desc{font-size:12.5px;font-weight:300;color:#7080a0;line-height:1.6;margin-bottom:.9rem}
.pstk{display:flex;flex-wrap:wrap;gap:5px}
.ps{font-family:var(--mono);font-size:10px;padding:3px 9px;border-radius:2px;background:var(--s3);border:1px solid var(--bd);color:var(--mu)}

/* ── WORK EXP ── */
.wcard{background:var(--s1);border:1px solid var(--bd);border-radius:5px;padding:1.5rem;margin-bottom:1rem;position:relative;overflow:hidden;transition:border-color .22s}
.wcard:hover{border-color:var(--bd2)}
.w-head{display:flex;align-items:flex-start;justify-content:space-between;gap:12px;flex-wrap:wrap;margin-bottom:.5rem}
.w-co{font-size:16px;font-weight:700;color:var(--wh)}
.w-date{font-family:var(--mono);font-size:10px;color:var(--mu);letter-spacing:1px;padding:3px 10px;border:1px solid var(--bd);border-radius:20px;white-space:nowrap}
.w-role{font-family:var(--mono);font-size:11.5px;color:var(--pu2);letter-spacing:1px;margin-bottom:.5rem}
.w-loc{font-family:var(--mono);font-size:10px;color:var(--mu);margin-bottom:1rem;display:flex;align-items:center;gap:6px}
.wpts{list-style:none;display:flex;flex-direction:column;gap:6px}
.wpts li{display:flex;align-items:flex-start;gap:9px;font-size:13px;font-weight:300;color:#8090b0;line-height:1.6}
.wpts li::before{content:'▸';color:var(--tl);flex-shrink:0;margin-top:1px}

/* ── LEARNING ── */
.litem{display:flex;align-items:flex-start;gap:10px;padding:11px 0;border-bottom:1px solid var(--bd)}
.litem:first-child{padding-top:0}
.litem:last-child{border-bottom:none;padding-bottom:0}
.lico{width:32px;height:32px;border-radius:4px;flex-shrink:0;display:flex;align-items:center;justify-content:center;font-size:14px}
.llbl{font-family:var(--mono);font-size:9px;letter-spacing:2px;text-transform:uppercase;margin-bottom:3px}
.lval{font-size:13px;font-weight:300;color:#8898b8;line-height:1.5}

/* ── SPRINT TABLE ── */
.sprint-grid{display:grid;grid-template-columns:1fr 1fr;gap:1rem}
@media(max-width:640px){.sprint-grid{grid-template-columns:1fr}}
.sprint-row{display:flex;align-items:flex-start;gap:10px;padding:10px 0;border-bottom:1px solid var(--bd)}
.sprint-row:first-child{padding-top:0}
.sprint-row:last-child{border-bottom:none;padding-bottom:0}
.sr-ico{width:8px;height:8px;border-radius:50%;flex-shrink:0;margin-top:5px}
.sr-lbl{font-family:var(--mono);font-size:9px;letter-spacing:2px;text-transform:uppercase;margin-bottom:3px}
.sr-val{font-size:13px;font-weight:300;color:#8898b8;line-height:1.5}

/* ── QUOTE ── */
.quote{border-left:2px solid var(--pu);padding:1rem 1.5rem;background:rgba(168,85,247,.05);border-radius:0 4px 4px 0;font-size:14px;font-style:italic;color:#a0b0cc;margin:1.5rem 0;line-height:1.7}

/* ── FOOTER ── */
footer{background:var(--s1);border-top:1px solid var(--bd);padding:3rem 2rem 2rem;text-align:center;position:relative;z-index:1}
.foot-tag{font-family:var(--mono);font-size:9.5px;letter-spacing:3px;text-transform:uppercase;color:var(--mu);margin-bottom:1.5rem}
.socrow{display:flex;justify-content:center;gap:12px;flex-wrap:wrap;margin-bottom:1.5rem}
.soc{width:48px;height:48px;border-radius:5px;border:1px solid var(--bd);background:var(--s2);display:flex;align-items:center;justify-content:center;cursor:pointer;transition:all .2s;text-decoration:none}
.soc:hover{transform:translateY(-4px)}
.soc.gh:hover{border-color:#e6edf3;box-shadow:0 6px 20px rgba(230,237,243,.12)}
.soc.li:hover{border-color:#0a66c2;box-shadow:0 6px 20px rgba(10,102,194,.35)}
.soc.pt:hover{border-color:var(--pu);box-shadow:0 6px 20px rgba(168,85,247,.35)}
.soc.em:hover{border-color:var(--tl);box-shadow:0 6px 20px rgba(45,212,191,.3)}
.soc svg{width:20px;height:20px}
.foot-links{display:flex;flex-direction:column;gap:10px;align-items:center;margin-bottom:1.8rem}
.foot-link-row{display:flex;align-items:center;gap:12px;font-family:var(--mono);font-size:12px}
.foot-link-row .ficon{width:28px;height:28px;border-radius:3px;border:1px solid var(--bd);background:var(--s2);display:flex;align-items:center;justify-content:center;flex-shrink:0}
.foot-link-row .ficon svg{width:14px;height:14px}
.foot-link-row a{color:var(--tx);text-decoration:none;transition:color .2s}
.foot-link-row a:hover{color:var(--tl)}
.foot-divider{width:100%;max-width:500px;height:1px;background:linear-gradient(to right,transparent,var(--bd),transparent);margin:1.5rem auto}
.foot-copy{font-family:var(--mono);font-size:10px;letter-spacing:1.5px;color:var(--mu2);text-transform:uppercase}
.foot-copy span{color:var(--tl)}
.foot-stack{font-family:var(--mono);font-size:9px;letter-spacing:1px;color:var(--mu2);margin-top:.5rem}

/* ── REVEAL ANIMATIONS ── */
.reveal{opacity:0;transform:translateY(24px);transition:opacity .65s ease,transform .65s ease}
.reveal.visible{opacity:1;transform:none}

/* ── CURSOR GLOW ── */
.cursor-glow{position:fixed;width:300px;height:300px;border-radius:50%;pointer-events:none;z-index:0;transition:transform .1s ease;background:radial-gradient(circle,rgba(168,85,247,.06) 0%,transparent 70%);transform:translate(-50%,-50%)}
</style>
</head>
<body>

<canvas id="bgCanvas"></canvas>
<div class="cursor-glow" id="cursorGlow"></div>

<!-- NAV -->
<nav>
  <div class="nav-brand"><span>Aayush</span> Mathur <span style="color:var(--mu)">/ MathuR-A01</span></div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <a href="#experience">Experience</a>
    <a href="#connect">Connect</a>
    <div class="nav-dot"></div>
  </div>
</nav>

<div class="page">

<!-- ═══════════════════ HERO ═══════════════════ -->
<div class="hero">
  <div class="hero-geo"></div>
  <div class="crn a"></div><div class="crn b"></div><div class="crn c"></div><div class="crn d"></div>
  <div class="hero-wrap">
    <div class="chip"><div class="dot-pulse"></div>FULL STACK DEVELOPER & TESTER · INDIA 🇮🇳</div>
    <div class="hname">Aayush <span class="ghost">Mathur</span></div>
    <div class="hsub">/ MathuR-A01</div>
    <div class="hrole"><span id="typed"></span><span class="tcur"></span></div>
    <div class="hexp-badge">⚡ 3+ Years Experience · TMU & Knocial India</div>
    <div class="divg"></div>
    <p class="hbio"><strong>Full Stack Web Developer & Software Tester</strong> with 3+ years designing, developing, testing, and maintaining <em>scalable web applications</em> across the full SDLC. Hands-on expertise in <strong>Laravel, React.js, PHP & MySQL</strong> — bridging clean code with rigorous quality engineering.</p>
    <p class="hbio" style="margin-top:.8rem">My focus: <strong>performance optimisation, clean code principles,</strong> and developer experience — from AI-powered systems handling <em>1,000+ queries/month</em> to enterprise-grade CMS platforms and production deployments.</p>
    <div class="hmeta">
      <a href="mailto:mathur.aayush3780@gmail.com"><div class="md"></div>mathur.aayush3780@gmail.com</a>
      <a href="https://aayu-port.vercel.app" target="_blank"><div class="md"></div>aayu-port.vercel.app</a>
      <a href="https://github.com/MathuR-A01" target="_blank"><div class="md"></div>github.com/MathuR-A01</a>
      <a href="tel:+917505800914"><div class="md"></div>+91 7505800914</a>
    </div>
    <div class="hero-btns">
      <a href="https://aayu-port.vercel.app" target="_blank" class="btn bp">View Portfolio ↗</a>
      <a href="https://github.com/MathuR-A01" target="_blank" class="btn bt">GitHub ↗</a>
      <a href="https://linkedin.com/in/aayush-mathur-fullstack-web-developer" target="_blank" class="btn bw">LinkedIn ↗</a>
    </div>
  </div>
</div>

<!-- STATS BAR -->
<div class="stats-bar">
  <div class="stats-inner">
    <div class="scard tl"><div class="snum tl" id="c1">0</div><div class="slbl">Years Exp</div></div>
    <div class="scard pu"><div class="snum pu" id="c2">0</div><div class="slbl">Live Projects</div></div>
    <div class="scard pk"><div class="snum pk" id="c3">0</div><div class="slbl">Queries / Mo (AI)</div></div>
    <div class="scard am"><div class="snum am" id="c4">0</div><div class="slbl">GB Migrated</div></div>
  </div>
</div>

<!-- ═══════════════════ ABOUT ═══════════════════ -->
<section id="about">
  <div class="wrap">
    <div class="sh reveal"><span class="sh-lbl tl">01 — SYSTEM.INIT</span><div class="sh-line tl"></div></div>
    <div class="term reveal">
      <div class="tbar">
        <div class="td" style="background:#ff5f57"></div>
        <div class="td" style="background:#febc2e"></div>
        <div class="td" style="background:#28c840"></div>
        <span class="ttl">aayush@tmu-dev — ~/workspace — bash</span>
      </div>
      <div class="tb">
        <div><span class="tp">aayush@dev</span><span class="tc">:~$</span> <span class="tw">whoami</span></div>
        <div><span class="tc">→ </span><span class="tv">Aayush Mathur</span><span class="tc"> | Full Stack Dev & Software Tester | TMU, Moradabad 🇮🇳</span></div>
        <div><span class="tp">aayush@dev</span><span class="tc">:~$</span> <span class="tw">cat stack.json</span></div>
        <div><span class="tam">{</span></div>
        <div style="padding-left:20px"><span class="tk">"core"</span><span class="tc">:</span> <span class="tv">["Laravel", "React.js", "PHP", "MySQL", "JavaScript ES6+"]</span><span class="tam">,</span></div>
        <div style="padding-left:20px"><span class="tk">"testing"</span><span class="tc">:</span> <span class="tv">["Manual Testing", "API Testing", "Postman", "Defect Tracking"]</span><span class="tam">,</span></div>
        <div style="padding-left:20px"><span class="tk">"ai"</span><span class="tc">:</span> <span class="tv">["n8n Automation", "RAG / LLM Agents", "Gemini", "Prompt Engineering"]</span></div>
        <div><span class="tam">}</span></div>
        <div><span class="tp">aayush@dev</span><span class="tc">:~$</span> <span class="tw">git log --oneline -1</span></div>
        <div><span class="tam">9f2a1c4</span> <span class="tv"> feat: AI counsellor handles 1,000+ university queries/month 🚀</span></div>
        <div><span class="tp">aayush@dev</span><span class="tc">:~$</span> <span class="tcur"></span></div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════ SKILLS ═══════════════════ -->
<section id="skills">
  <div class="wrap">
    <div class="sh reveal"><span class="sh-lbl pu">02 — SKILL GRID</span><div class="sh-line pu"></div></div>
    <div class="card hpu reveal" style="margin-bottom:1.5rem">
      <div class="abar pu"></div>
      <div style="margin-bottom:1.2rem">
        <div class="skill-group-title">🟣 Core Engine — Languages & Backend</div>
        <div class="bgs">
          <span class="bg pu">PHP</span><span class="bg pu">Laravel</span><span class="bg pu">JavaScript ES6+</span>
          <span class="bg pu">MySQL</span><span class="bg nu">HTML5</span><span class="bg nu">CSS3 / SCSS</span><span class="bg nu">Bash</span>
        </div>
      </div>
      <div style="margin-bottom:1.2rem">
        <div class="skill-group-title">🔵 Frameworks & Libraries</div>
        <div class="bgs">
          <span class="bg tl">React.js</span><span class="bg tl">Bootstrap</span><span class="bg tl">Tailwind CSS</span>
          <span class="bg tl">ASP.NET (UI)</span><span class="bg nu">REST APIs</span><span class="bg nu">Responsive Design</span>
        </div>
      </div>
      <div style="margin-bottom:1.2rem">
        <div class="skill-group-title">🟡 Testing & QA Tools</div>
        <div class="bgs">
          <span class="bg am">Manual Testing</span><span class="bg am">API Testing</span><span class="bg am">Postman</span>
          <span class="bg am">Functional Testing</span><span class="bg am">UI Testing</span><span class="bg am">Regression Testing</span>
          <span class="bg am">Defect Tracking</span><span class="bg am">Negative Testing</span><span class="bg nu">Test Case Design</span>
        </div>
      </div>
      <div style="margin-bottom:1.2rem">
        <div class="skill-group-title">🟠 AI Tools & Automation</div>
        <div class="bgs">
          <span class="bg or">n8n Automation</span><span class="bg or">RAG / LLM Agents</span><span class="bg or">Gemini AI</span>
          <span class="bg or">Prompt Engineering</span><span class="bg or">Webhook Integration</span>
          <span class="bg nu">PostgreSQL (AI)</span><span class="bg nu">AI Chatbot Dev</span>
        </div>
      </div>
      <div>
        <div class="skill-group-title">🔴 DevOps, CMS & Operations</div>
        <div class="bgs">
          <span class="bg pk">Git / GitHub</span><span class="bg pk">Vercel</span><span class="bg pk">Linux / Servers</span>
          <span class="bg pk">On-page SEO</span><span class="bg pk">Server Migration</span><span class="bg pk">CMS Management</span>
          <span class="bg nu">RBAC Systems</span><span class="bg nu">Agile / SDLC</span>
        </div>
      </div>
    </div>

    <div class="sh reveal" style="margin-top:2rem"><span class="sh-lbl tl">PROFICIENCY MATRIX</span><div class="sh-line tl"></div></div>
    <div class="card reveal" id="profCard">
      <div class="prow"><span class="pnm">Laravel / PHP</span><div class="ptr"><div class="pfl" data-w="90" style="background:var(--pu)"></div></div><span class="ppc">90%</span></div>
      <div class="prow"><span class="pnm">React.js</span><div class="ptr"><div class="pfl" data-w="85" style="background:var(--tl)"></div></div><span class="ppc">85%</span></div>
      <div class="prow"><span class="pnm">JavaScript ES6+</span><div class="ptr"><div class="pfl" data-w="88" style="background:var(--pu2)"></div></div><span class="ppc">88%</span></div>
      <div class="prow"><span class="pnm">MySQL / DB</span><div class="ptr"><div class="pfl" data-w="85" style="background:var(--tl2)"></div></div><span class="ppc">85%</span></div>
      <div class="prow"><span class="pnm">Manual Testing</span><div class="ptr"><div class="pfl" data-w="87" style="background:var(--am)"></div></div><span class="ppc">87%</span></div>
      <div class="prow"><span class="pnm">API Testing</span><div class="ptr"><div class="pfl" data-w="82" style="background:var(--am)"></div></div><span class="ppc">82%</span></div>
      <div class="prow"><span class="pnm">n8n / AI Agents</span><div class="ptr"><div class="pfl" data-w="75" style="background:var(--or)"></div></div><span class="ppc">75%</span></div>
      <div class="prow" style="margin-bottom:0"><span class="pnm">HTML5 / CSS3</span><div class="ptr"><div class="pfl" data-w="92" style="background:var(--pk)"></div></div><span class="ppc">92%</span></div>
    </div>
  </div>
</section>

<!-- ═══════════════════ PROJECTS ═══════════════════ -->
<section id="projects">
  <div class="wrap">
    <div class="sh reveal"><span class="sh-lbl pk">04 — LIVE PROJECTS</span><div class="sh-line pk"></div></div>
    <div class="g2 reveal" style="gap:1rem">
      <div class="pcard">
        <div class="ptag pu">FULL STACK · REACT.JS</div>
        <div class="pc-title">TMU ONE Admin Dashboard</div>
        <div class="pc-desc">Role-based access control dashboard with announcements, feedback modules & REST API validation via Postman. Manual testing & bug fixing for Flutter mobile app on Android & iOS.</div>
        <div class="pstk"><span class="ps">React.js</span><span class="ps">RBAC</span><span class="ps">REST APIs</span><span class="ps">Postman</span><span class="ps">Flutter</span></div>
      </div>
      <div class="pcard">
        <div class="ptag or">AI-POWERED SYSTEM</div>
        <div class="pc-title">TMU AI Counsellor</div>
        <div class="pc-desc">AI chatbot using n8n automation + RAG/LLM agents + Gemini, handling 1,000+ university queries/month. Secure webhooks and controlled prompts for TMU-specific compliance.</div>
        <div class="pstk"><span class="ps">n8n</span><span class="ps">RAG / LLM</span><span class="ps">Gemini</span><span class="ps">PostgreSQL</span><span class="ps">Webhooks</span></div>
      </div>
      <div class="pcard">
        <div class="ptag am">TESTING & QA</div>
        <div class="pc-title">TMU GYM Dashboard & App</div>
        <div class="pc-desc">End-to-end manual testing — functional, UI, negative & API flows. Defect identification & fixes, stable Android/iOS releases ensuring high-quality production deployments.</div>
        <div class="pstk"><span class="ps">Manual Testing</span><span class="ps">API Testing</span><span class="ps">Android</span><span class="ps">iOS</span></div>
      </div>
      <div class="pcard">
        <div class="ptag tl">LARAVEL · ENTERPRISE</div>
        <div class="pc-title">Academic & Conference Platforms</div>
        <div class="pc-desc">150+ Laravel program pages, 800GB+ server migration, on-page SEO, CMS management, cross-browser compatibility & large-scale data operations ensuring stable, scalable systems.</div>
        <div class="pstk"><span class="ps">Laravel</span><span class="ps">PHP</span><span class="ps">MySQL</span><span class="ps">Bootstrap</span><span class="ps">SEO</span></div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════ EXPERIENCE ═══════════════════ -->
<section id="experience">
  <div class="wrap">
    <div class="sh reveal"><span class="sh-lbl am">05 — WORK EXPERIENCE</span><div class="sh-line am"></div></div>
    <div class="wcard hpu reveal">
      <div class="abar pu"></div>
      <div class="w-head">
        <div class="w-co">Teerthanker Mahaveer University (TMU)</div>
        <div class="w-date">02/2023 — PRESENT</div>
      </div>
      <div class="w-role">Full Stack Developer & Software Tester</div>
      <div class="w-loc"><div class="md"></div>Moradabad, Uttar Pradesh, India</div>
      <ul class="wpts">
        <li>Built & maintained scalable full-stack apps using HTML, CSS, JS, Bootstrap, React.js, Laravel & MySQL</li>
        <li>Developed AI-powered counselling system (n8n + RAG + Gemini) handling 1,000+ queries/month</li>
        <li>Managed TMU ONE Admin Dashboard — RBAC, announcements, feedback modules & centralized CMS</li>
        <li>Performed manual testing: functional, UI, negative & edge-case validation for web and mobile apps</li>
        <li>Validated REST APIs via Postman ensuring reliable frontend-backend data flow</li>
        <li>Executed 800GB+ server migration and managed 150+ academic & conference web platforms</li>
      </ul>
    </div>
    <div class="wcard htl reveal">
      <div class="abar tl"></div>
      <div class="w-head">
        <div class="w-co">Knocial India Limited</div>
        <div class="w-date">05/2022 — 12/2022</div>
      </div>
      <div class="w-role">Associate Software Engineer</div>
      <div class="w-loc"><div class="md"></div>Gurugram, Haryana, India</div>
      <ul class="wpts">
        <li>Designed responsive UIs using HTML, CSS, JavaScript, Bootstrap & ASP.NET</li>
        <li>Built dynamic UI components with client-side validations improving usability & interaction consistency</li>
        <li>Performed UI testing, bug fixing & layout optimisation for high visual quality standards</li>
      </ul>
    </div>

    <!-- CURRENTLY LEARNING -->
    <div class="sh reveal" style="margin-top:2rem"><span class="sh-lbl or">06 — CURRENTLY LEVELLING UP</span><div class="sh-line or"></div></div>
    <div class="g2 reveal">
      <div class="card ham">
        <div class="abar am"></div>
        <div class="clbl am">TESTING TOOLS</div>
        <div class="litem">
          <div class="lico" style="background:rgba(251,191,36,.1);color:var(--am)">◈</div>
          <div><div class="llbl" style="color:var(--am)">LEARNING NOW</div><div class="lval">Selenium WebDriver — automated browser testing</div></div>
        </div>
        <div class="litem">
          <div class="lico" style="background:rgba(251,191,36,.1);color:var(--am)">◆</div>
          <div><div class="llbl" style="color:var(--am)">IN PROGRESS</div><div class="lval">Cypress.io — end-to-end test automation for React apps</div></div>
        </div>
        <div class="litem">
          <div class="lico" style="background:rgba(251,191,36,.1);color:var(--am)">◉</div>
          <div><div class="llbl" style="color:var(--am)">EXPLORING</div><div class="lval">Jest + React Testing Library — component testing</div></div>
        </div>
      </div>
      <div class="card" style="border-color:rgba(251,146,60,.2)">
        <div class="abar or"></div>
        <div class="clbl or">AI TOOLS & AUTOMATION</div>
        <div class="litem">
          <div class="lico" style="background:rgba(251,146,60,.1);color:var(--or)">⬡</div>
          <div><div class="llbl" style="color:var(--or)">DEEPENING</div><div class="lval">Advanced n8n workflows — multi-agent AI pipelines</div></div>
        </div>
        <div class="litem">
          <div class="lico" style="background:rgba(251,146,60,.1);color:var(--or)">◎</div>
          <div><div class="llbl" style="color:var(--or)">STUDYING</div><div class="lval">LangChain & vector embeddings for RAG architectures</div></div>
        </div>
        <div class="litem">
          <div class="lico" style="background:rgba(251,146,60,.1);color:var(--or)">▸</div>
          <div><div class="llbl" style="color:var(--or)">NEXT UP</div><div class="lval">TypeScript migration — phasing JS codebases to TS</div></div>
        </div>
      </div>
    </div>

    <!-- CURRENT SPRINT -->
    <div class="sh reveal" style="margin-top:2rem"><span class="sh-lbl tl">07 — CURRENT SPRINT</span><div class="sh-line tl"></div></div>
    <div class="sprint-grid reveal">
      <div class="card hpu">
        <div class="abar pu"></div>
        <div class="clbl pu">SHIPPING NOW</div>
        <div class="sprint-row"><div class="sr-ico" style="background:var(--pu)"></div><div><div class="sr-lbl" style="color:var(--pu)">BUILDING</div><div class="sr-val">Scalable Laravel + React.js platforms at TMU</div></div></div>
        <div class="sprint-row"><div class="sr-ico" style="background:var(--pu2)"></div><div><div class="sr-lbl" style="color:var(--pu2)">AUTOMATING</div><div class="sr-val">AI workflows & LLM agent pipelines with n8n</div></div></div>
        <div class="sprint-row"><div class="sr-ico" style="background:var(--am)"></div><div><div class="sr-lbl" style="color:var(--am)">TESTING</div><div class="sr-val">Expanding from manual → automated test coverage</div></div></div>
        <div class="sprint-row"><div class="sr-ico" style="background:var(--tl)"></div><div><div class="sr-lbl" style="color:var(--tl)">READING</div><div class="sr-val">Clean Architecture · The Art of Software Testing</div></div></div>
      </div>
      <div class="card htl">
        <div class="abar tl"></div>
        <div class="clbl tl">OPEN TO COLLABORATE</div>
        <div class="sprint-row"><div class="sr-ico" style="background:var(--tl)"></div><div><div class="sr-lbl" style="color:var(--tl)">OPEN TO</div><div class="sr-val">Laravel / React projects, QA automation, AI integrations</div></div></div>
        <div class="sprint-row"><div class="sr-ico" style="background:var(--tl2)"></div><div><div class="sr-lbl" style="color:var(--tl2)">INTERESTED IN</div><div class="sr-val">AI-integrated web apps, test automation frameworks</div></div></div>
        <div class="sprint-row"><div class="sr-ico" style="background:var(--pk)"></div><div><div class="sr-lbl" style="color:var(--pk)">DOMAINS</div><div class="sr-val">EdTech, SaaS, enterprise web, AI-powered tools</div></div></div>
        <div class="sprint-row"><div class="sr-ico" style="background:var(--pu)"></div><div><div class="sr-lbl" style="color:var(--pu)">DM ME</div><div class="sr-val">Need a dev who codes AND tests — I do both!</div></div></div>
      </div>
    </div>
    <div class="quote reveal">"3+ years in, still learning every day — performance optimisation, clean code, and developer experience are non-negotiable first principles."</div>
  </div>
</section>

<!-- ═══════════════════ CONNECT / FOOTER ═══════════════════ -->
<footer id="connect">
  <div class="foot-tag">Connect · Collaborate · Build · Test · Automate</div>
  <div class="socrow">
    <a href="https://github.com/MathuR-A01" target="_blank" class="soc gh">
      <svg viewBox="0 0 24 24" fill="#e6edf3"><path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/></svg>
    </a>
    <a href="https://linkedin.com/in/aayush-mathur-fullstack-web-developer" target="_blank" class="soc li">
      <svg viewBox="0 0 24 24" fill="#0a66c2"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
    </a>
    <a href="https://aayu-port.vercel.app" target="_blank" class="soc pt">
      <svg viewBox="0 0 24 24" fill="none" stroke="#a855f7" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 010 20M12 2a15.3 15.3 0 000 20"/></svg>
    </a>
    <a href="mailto:mathur.aayush3780@gmail.com" class="soc em">
      <svg viewBox="0 0 24 24" fill="none" stroke="#2dd4bf" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
    </a>
  </div>

  <!-- LINK TABLE -->
  <div class="foot-links">
    <div class="foot-link-row">
      <div class="ficon"><svg viewBox="0 0 24 24" fill="#e6edf3"><path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/></svg></div>
      <a href="https://github.com/MathuR-A01" target="_blank">github.com/MathuR-A01</a>
    </div>
    <div class="foot-link-row">
      <div class="ficon"><svg viewBox="0 0 24 24" fill="#0a66c2"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg></div>
      <a href="https://linkedin.com/in/aayush-mathur-fullstack-web-developer" target="_blank">linkedin.com/in/aayush-mathur-fullstack-web-developer</a>
    </div>
    <div class="foot-link-row">
      <div class="ficon"><svg viewBox="0 0 24 24" fill="none" stroke="#a855f7" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 010 20M12 2a15.3 15.3 0 000 20"/></svg></div>
      <a href="https://aayu-port.vercel.app" target="_blank">aayu-port.vercel.app</a>
    </div>
    <div class="foot-link-row">
      <div class="ficon"><svg viewBox="0 0 24 24" fill="none" stroke="#2dd4bf" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg></div>
      <a href="mailto:mathur.aayush3780@gmail.com">mathur.aayush3780@gmail.com</a>
    </div>
  </div>

  <div class="foot-divider"></div>
  <div class="foot-copy">Crafted with ⚡ by <span>Aayush Mathur</span> · <span>MathuR-A01</span> · Amroha, India</div>
  <div class="foot-stack">STACK: LARAVEL · REACT.JS · PHP · MYSQL · n8n · AI AGENTS · MANUAL TESTING</div>
</footer>

</div><!-- /page -->

<script>
/* ── PARTICLE BG ── */
const cv=document.getElementById('bgCanvas'),ctx=cv.getContext('2d');
let W,H,pts=[];
function resize(){W=cv.width=window.innerWidth;H=cv.height=window.innerHeight}
class Pt{
  constructor(){this.reset()}
  reset(){
    this.x=Math.random()*W;this.y=Math.random()*H;
    this.vx=(Math.random()-.5)*.3;this.vy=(Math.random()-.5)*.3;
    this.r=Math.random()*1.2+.3;
    const r=Math.random();
    this.c=r<.4?'168,85,247':r<.75?'45,212,191':'251,191,36';
    this.a=Math.random()*.4+.15;
  }
  update(){this.x+=this.vx;this.y+=this.vy;if(this.x<0||this.x>W||this.y<0||this.y>H)this.reset()}
  draw(){ctx.beginPath();ctx.arc(this.x,this.y,this.r,0,Math.PI*2);ctx.fillStyle=`rgba(${this.c},${this.a})`;ctx.fill()}
}
function init(){resize();pts=[];const n=Math.min(Math.floor(W*H/7000),100);for(let i=0;i<n;i++)pts.push(new Pt())}
function frame(){
  ctx.clearRect(0,0,W,H);
  for(let i=0;i<pts.length;i++){
    pts[i].update();pts[i].draw();
    for(let j=i+1;j<pts.length;j++){
      const dx=pts[i].x-pts[j].x,dy=pts[i].y-pts[j].y,d=Math.sqrt(dx*dx+dy*dy);
      if(d<120){
        ctx.beginPath();ctx.moveTo(pts[i].x,pts[i].y);ctx.lineTo(pts[j].x,pts[j].y);
        ctx.strokeStyle=`rgba(168,85,247,${(1-d/120)*.1})`;ctx.lineWidth=.5;ctx.stroke();
      }
    }
  }
  requestAnimationFrame(frame);
}
init();frame();
window.addEventListener('resize',init);

/* ── CURSOR GLOW ── */
const glow=document.getElementById('cursorGlow');
document.addEventListener('mousemove',e=>{glow.style.left=e.clientX+'px';glow.style.top=e.clientY+'px'});

/* ── TYPING ── */
const titles=['Full Stack Developer & Tester','Laravel · React.js · PHP Engineer','Manual & API Testing Expert','AI Automation with n8n & LLMs','Open Source · Seamless UX 🚀'];
let ti=0,ci=0,del=false;
const el=document.getElementById('typed');
function tick(){
  const w=titles[ti];
  if(!del){el.textContent=w.slice(0,++ci);if(ci===w.length){del=true;setTimeout(tick,2200);return;}}
  else{el.textContent=w.slice(0,--ci);if(ci===0){del=false;ti=(ti+1)%titles.length;setTimeout(tick,300);return;}}
  setTimeout(tick,del?16:65);
}
setTimeout(tick,600);

/* ── COUNTERS ── */
function cnt(id,end,sfx=''){
  const e=document.getElementById(id);if(!e)return;
  let v=0,s=Math.max(1,Math.ceil(end/50));
  const t=setInterval(()=>{v=Math.min(v+s,end);e.textContent=v+sfx;if(v>=end)clearInterval(t);},22);
}
setTimeout(()=>{cnt('c1',3,'+ yrs');cnt('c2',4,'');cnt('c3',1000,'+ /mo');cnt('c4',800,'GB+')},400);

/* ── SCROLL REVEAL ── */
const obs=new IntersectionObserver(entries=>{
  entries.forEach(e=>{if(e.isIntersecting){e.target.classList.add('visible');obs.unobserve(e.target)}});
},{threshold:.12});
document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));

/* ── PROFICIENCY BARS ── */
const profObs=new IntersectionObserver(entries=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      e.target.querySelectorAll('.pfl').forEach(bar=>{
        bar.style.width=bar.dataset.w+'%';
      });
      profObs.unobserve(e.target);
    }
  });
},{threshold:.3});
const profCard=document.getElementById('profCard');
if(profCard)profObs.observe(profCard);
</script>
</body>
</html>
