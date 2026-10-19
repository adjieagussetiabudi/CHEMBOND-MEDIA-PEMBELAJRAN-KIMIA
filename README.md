# CHEMBOND-MEDIA-PEMBELAJRAN-KIMIA
Media pembelajaran untuk materi ikatan kovalen koordinasi 
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#12213f">
<title>CHEM-BOND — Ikatan Kovalen Koordinasi</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700&family=Sora:wght@500;600;700;800&display=swap" rel="stylesheet">
<style>
:root{
  --navy:#12213f; --navy-2:#0c172d; --blue:#1d4a8a; --sky:#4aa8ff; --cyan:#3cc7e6;
  --gold:#f4c24d; --mint:#4fd8a0; --rose:#ff7d8c;
  --ink:#16233a; --muted:#5a6a82; --paper:#f3f6fb; --line:#d8e1ee; --white:#fff;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth;-webkit-text-size-adjust:100%}
body{margin:0;font-family:"Plus Jakarta Sans",system-ui,-apple-system,"Segoe UI",Roboto,sans-serif;color:var(--ink);background:#fff;line-height:1.65;font-size:16px}
h1,h2,h3,h4{font-family:"Sora","Plus Jakarta Sans",system-ui,sans-serif;line-height:1.22;margin:0;letter-spacing:-.01em}
p{margin:0}
button{font:inherit;cursor:pointer}
:focus-visible{outline:3px solid var(--gold);outline-offset:3px}
sub,sup{line-height:0}

/* ---------- kerangka slide ---------- */
.slide{position:relative;padding:clamp(36px,6vw,72px) clamp(16px,4vw,32px)}
.wrap{max-width:1040px;margin:0 auto;display:flex;flex-direction:column;gap:18px}
.bg-white{background:#fff}
.bg-paper{background:var(--paper)}

.tag{display:inline-block;align-self:flex-start;font-weight:700;font-size:.9rem;color:var(--blue);background:#e4eefc;border:1px solid #c9dcf6;padding:5px 14px;border-radius:999px}
.sec-title{font-size:clamp(1.7rem,4.2vw,2.5rem);font-weight:700;color:var(--navy)}
.sec-desc{color:var(--muted);max-width:68ch}

.card{background:#fff;border:1px solid var(--line);border-radius:18px;padding:22px 24px}
.card h3{font-size:1.1rem;color:var(--navy);margin-bottom:10px}
.card p,.card li{color:#33445d;font-size:.96rem}
.card ul,.card ol{margin:0;padding-left:1.15rem;display:grid;gap:6px}
.grid3{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
.grid4{display:grid;grid-template-columns:repeat(4,1fr);gap:14px}
.grid2{display:grid;grid-template-columns:repeat(2,1fr);gap:16px}
@media (max-width:860px){.grid3{grid-template-columns:1fr}.grid4{grid-template-columns:repeat(2,1fr)}.grid2{grid-template-columns:1fr}}

.btn{display:inline-flex;align-items:center;justify-content:center;gap:8px;padding:13px 22px;border-radius:12px;border:2px solid transparent;font-weight:700;font-size:.98rem;transition:transform .15s,background .15s,border-color .15s;text-decoration:none}
.btn:active{transform:scale(.97)}
.btn-primary{background:var(--blue);color:#fff}
.btn-primary:hover{background:#245aa6}
.btn-gold{background:var(--gold);color:#2b2205}
.btn-gold:hover{background:#ffd163}
.btn-ghost{background:transparent;color:var(--blue);border-color:#b8cde9}
.btn-ghost:hover{background:#eaf2fd}
.btn[disabled]{opacity:.45;cursor:not-allowed;transform:none}
.btn.speaking{background:var(--rose);color:#3a0710;border-color:var(--rose)}

/* ---------- slide 1 : beranda ---------- */
.hero{color:#fff;text-align:center;
  background:
    radial-gradient(900px 520px at 88% -8%,rgba(74,168,255,.30),transparent 60%),
    radial-gradient(700px 480px at -8% 108%,rgba(60,199,230,.20),transparent 60%),
    linear-gradient(165deg,#0a1530 0%,#12213f 45%,#1c3c70 100%)}
.hero .wrap{gap:22px;align-items:center}
.logo{width:84px;height:84px;border-radius:24px;display:grid;place-items:center;background:rgba(255,255,255,.08);border:1px solid rgba(255,255,255,.2)}
.nav{display:flex;flex-wrap:wrap;justify-content:center;gap:8px}
.nav a{color:#dbe9ff;text-decoration:none;font-size:.86rem;font-weight:600;padding:8px 14px;border-radius:999px;background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.18);transition:background .15s}
.nav a:hover{background:rgba(255,255,255,.18)}
.nav b{color:var(--gold);margin-right:6px;font-weight:700}
.brandrow{display:grid;grid-template-columns:1fr 1fr;align-items:center;gap:0;width:100%;max-width:640px}
.brand{font-family:"Sora",sans-serif;font-weight:800;font-size:clamp(1.8rem,5vw,2.8rem);letter-spacing:.04em;text-align:right;padding-right:22px;border-right:2px solid rgba(255,255,255,.3)}
.brand-sub{text-align:left;padding-left:22px;color:#bcd4f5;font-weight:500;font-size:clamp(.95rem,2.4vw,1.15rem);line-height:1.35}
.progress{width:100%;max-width:640px}
.progress .row{display:flex;justify-content:space-between;font-size:.86rem;color:#bcd4f5;margin-bottom:6px}
.progress .row b{color:var(--gold)}
.track{height:10px;border-radius:999px;background:rgba(255,255,255,.14);overflow:hidden}
.fill{height:100%;width:0;background:linear-gradient(90deg,var(--cyan),var(--gold));border-radius:999px;transition:width .25s}
.hero-label{font-size:.92rem;font-weight:600;color:var(--gold);padding:6px 16px;border:1px solid rgba(244,194,77,.5);border-radius:999px}
.hero h1{font-size:clamp(2.4rem,7vw,4.4rem);font-weight:800;line-height:1.08;max-width:14ch}
.hero .desc{max-width:60ch;color:#cfe0f8;font-size:1.05rem}
.badges{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;width:100%;max-width:820px}
.badge{padding:10px 12px;border-radius:12px;background:rgba(255,255,255,.08);border:1px solid rgba(255,255,255,.18);font-size:.88rem;font-weight:600;color:#e6f0ff}
.hero-btns{display:grid;grid-template-columns:1fr 1fr;gap:12px;width:100%;max-width:520px}
.hero .btn-ghost{color:#fff;border-color:rgba(255,255,255,.4)}
.hero .btn-ghost:hover{background:rgba(255,255,255,.12)}
.hero-illus{width:100%;max-width:640px;border-radius:24px;background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.14);padding:8px}
.hero-illus svg{width:100%;height:auto;display:block}
.orbit{transform-box:fill-box;transform-origin:center;animation:spin 26s linear infinite}
@keyframes spin{to{transform:rotate(360deg)}}
@media (max-width:640px){.badges{grid-template-columns:repeat(2,1fr)}.brandrow{grid-template-columns:1fr}.brand{text-align:center;border-right:0;padding:0 0 6px}.brand-sub{text-align:center;padding:0}.hero-btns{grid-template-columns:1fr}}

/* ---------- slide 2 : peta ---------- */
.accent-title{display:flex;align-items:center;gap:14px}
.accent-title i{display:block;width:6px;height:44px;border-radius:4px;background:linear-gradient(var(--blue),var(--cyan))}
.accent-title span{font-family:"Sora",sans-serif;font-weight:700;color:var(--blue);font-size:1.05rem}
.q-box{background:linear-gradient(135deg,#fff7e0,#fff);border:1px solid #f0dfa8;border-radius:18px;padding:24px}
.q-box h3{font-size:1.15rem;margin-bottom:8px;color:#5b4300}
.q-box .q{font-family:"Sora",sans-serif;font-weight:600;font-size:1.2rem;color:var(--navy);margin-bottom:8px}
textarea{width:100%;min-height:120px;resize:vertical;border:2px solid var(--line);border-radius:14px;padding:14px 16px;font:inherit;color:var(--ink);background:#fff}
textarea:focus{border-color:var(--sky);outline:none}
.ans-box label{display:block;font-weight:700;color:var(--navy);margin-bottom:8px}

/* ---------- slide 3 & 4 ---------- */
.pemantik{position:relative;padding-top:50px}
.pemantik .no{position:absolute;top:14px;left:20px;font-family:"Sora",sans-serif;font-weight:800;font-size:1.5rem;color:var(--sky)}
.head-note{font-family:"Sora",sans-serif;font-weight:700;color:var(--navy);font-size:1.15rem}
.def h3{font-size:1.3rem}
.lewis{display:flex;flex-wrap:wrap;align-items:center;justify-content:center;gap:14px;margin-top:14px;padding:18px;border-radius:14px;background:#eef4fd;font-family:"Sora",sans-serif;font-size:clamp(1.3rem,3.6vw,1.9rem);font-weight:700;color:var(--blue);letter-spacing:.03em}
.lewis small{font-family:"Plus Jakarta Sans",sans-serif;font-size:.85rem;font-weight:500;color:var(--muted);letter-spacing:0;flex-basis:100%;text-align:center}
.note{border-left:6px solid var(--gold);background:#fff9e8;border-radius:0 14px 14px 0;padding:16px 20px}
.note b{font-family:"Sora",sans-serif;color:#6d5000}
.note.key{border-left-color:var(--sky);background:#eaf4ff}
.note.key b{color:var(--blue)}
.config{display:inline-block;font-family:"Sora",sans-serif;font-weight:700;font-size:clamp(1.3rem,3.6vw,1.9rem);color:var(--navy);background:#fff;border:2px dashed #b8cde9;border-radius:14px;padding:12px 22px}
.orbs{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
.orb{background:#fff;border:1px solid var(--line);border-radius:16px;padding:16px;text-align:center}
.orb .nm{font-family:"Sora",sans-serif;font-weight:700;color:var(--navy);margin-bottom:10px}
.boxes{display:flex;justify-content:center;gap:6px}
.obox{width:46px;height:46px;border:2px solid #7e97bd;border-radius:8px;display:grid;place-items:center;font-size:1.25rem;font-weight:800;color:var(--blue);background:#f8fbff;letter-spacing:-2px}
.obox.val{border-color:var(--gold);background:#fff9e8}
@media (max-width:640px){.orbs{grid-template-columns:1fr}}

/* ---------- slide 5 ---------- */
.av-panel{border-radius:24px;padding:clamp(24px,5vw,44px);color:#fff;min-height:200px;display:flex;flex-direction:column;justify-content:center;gap:14px;
  background:radial-gradient(500px 260px at 90% 0%,rgba(60,199,230,.3),transparent 60%),linear-gradient(150deg,#0e1b36,#1c3c70)}
.av-panel h2{font-size:clamp(1.6rem,4vw,2.3rem);font-weight:700}
.eq{display:flex;align-items:flex-end;gap:5px;height:44px}
.eq i{display:block;width:7px;border-radius:4px;background:var(--cyan);height:10px}
.eq.on i{animation:eq 0.9s ease-in-out infinite}
.eq.on i:nth-child(2n){animation-delay:.18s;background:var(--gold)}
.eq.on i:nth-child(3n){animation-delay:.34s}
@keyframes eq{0%,100%{height:8px}50%{height:42px}}
.av-desc{min-height:150px;display:flex;align-items:center;font-size:1.08rem;color:#33445d}
.av-act{min-height:210px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:12px;text-align:center}
.av-act .ico{font-size:2.4rem}
.av-act p{color:var(--muted);font-size:.94rem;max-width:30ch}

/* ---------- slide 6 : simulasi ---------- */
.sim{color:#e6f0ff;background:radial-gradient(800px 400px at 100% 0%,rgba(60,199,230,.14),transparent 60%),linear-gradient(180deg,#0c172d,#12284a)}
.sim .tag{background:rgba(255,255,255,.1);border-color:rgba(255,255,255,.2);color:#bfe0ff}
.sim .sec-title{color:#fff}
.sim .sec-desc{color:#b7cdea}
.stage-ind{display:flex;align-items:center;gap:12px;flex-wrap:wrap}
.stage-pill{font-family:"Sora",sans-serif;font-weight:700;color:#2b2205;background:var(--gold);padding:6px 16px;border-radius:999px}
.dots{display:flex;gap:6px}
.dots i{width:28px;height:6px;border-radius:4px;background:rgba(255,255,255,.2);transition:background .2s}
.dots i.on{background:var(--cyan)}
.sim-area{background:#0a1429;border:1px solid rgba(255,255,255,.14);border-radius:20px;padding:14px 14px 16px}
.sim-area .hd{display:flex;justify-content:space-between;gap:10px;flex-wrap:wrap;padding:2px 8px 8px;font-size:.9rem}
.sim-area .hd b{font-family:"Sora",sans-serif;color:var(--cyan)}
.sim-area .hd span{color:#a9c1e2}
.sim-area svg{width:100%;height:auto;display:block}
.sim-area .cap{padding:10px 10px 2px;text-align:center;color:#dcebff;min-height:3.4em}
.sim-btns{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
.sim .btn-ghost{color:#e6f0ff;border-color:rgba(255,255,255,.35)}
.sim .btn-ghost:hover{background:rgba(255,255,255,.1)}
@media (max-width:640px){.sim-btns{grid-template-columns:1fr}}
.flow{background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.14);border-radius:18px;padding:20px 22px}
.flow .st{font-size:.85rem;color:var(--cyan);font-weight:700}
.flow h3{font-size:1.25rem;color:#fff;margin:2px 0 14px}
.flow ol{list-style:none;margin:0;padding:0;display:flex;flex-wrap:wrap;gap:8px 6px;align-items:center}
.flow li{display:flex;align-items:center;gap:6px;font-size:.88rem}
.flow li span{padding:6px 12px;border-radius:999px;border:1px solid rgba(255,255,255,.22);color:#a9c1e2;background:transparent}
.flow li.done span{color:#bff0dc;border-color:rgba(79,216,160,.5)}
.flow li.now span{background:var(--gold);color:#2b2205;border-color:var(--gold);font-weight:700}
.flow li:not(:last-child)::after{content:"→";color:#6f89ad}
.challenge{background:linear-gradient(135deg,rgba(244,194,77,.18),rgba(244,194,77,.06));border:1px solid rgba(244,194,77,.45);border-radius:18px;padding:20px 22px}
.challenge h3{color:var(--gold);font-size:1.1rem;margin-bottom:6px}
.challenge p{color:#f1e6c6}
.sim .btn-gold{align-self:flex-start}
.pulse{animation:pulse 1.6s ease-in-out infinite}
@keyframes pulse{50%{opacity:.55}}
.drop{animation:drop .9s cubic-bezier(.2,.8,.2,1) both}
@keyframes drop{from{transform:translateY(-58px);opacity:.2}to{transform:none;opacity:1}}
.fadein{animation:fade .6s ease both}
@keyframes fade{from{opacity:0}to{opacity:1}}

/* ---------- slide 7 & 8 ---------- */
.video-box{position:relative;border-radius:20px;overflow:hidden;background:#0a1429;border:1px solid #223457;aspect-ratio:854/414;width:100%;max-width:900px;margin:0 auto}
.video-box video{width:100%;height:100%;display:block;background:#000}
.video-missing{position:absolute;inset:0;display:none;flex-direction:column;align-items:center;justify-content:center;gap:8px;text-align:center;padding:24px;color:#cfe0f8;background:linear-gradient(150deg,#0e1b36,#1c3c70)}
.video-missing.show{display:flex}
.video-missing code{background:rgba(255,255,255,.12);padding:2px 8px;border-radius:6px;color:var(--gold)}
.narr{display:flex;flex-wrap:wrap;align-items:center;justify-content:space-between;gap:12px;background:#eaf4ff;border:1px solid #c9dcf6;border-radius:16px;padding:14px 18px}
.narr .info{display:flex;flex-direction:column;font-size:.92rem;color:#33445d}
.narr .info b{color:var(--blue)}
.switch{display:inline-flex;align-items:center;gap:10px;padding:9px 16px;border-radius:999px;border:2px solid var(--blue);background:var(--blue);color:#fff;font-weight:700}
.switch.off{background:#fff;color:var(--muted);border-color:#b8cde9}
.particle{text-align:center;padding:18px 12px}
.particle .f{font-family:"Sora",sans-serif;font-weight:800;font-size:1.6rem;color:var(--blue)}
.particle .n{font-size:.88rem;color:var(--muted)}
.life-banner{position:relative;overflow:hidden;border-radius:24px;min-height:200px;padding:clamp(28px,5vw,48px);display:flex;align-items:center;color:#fff;
  background:radial-gradient(420px 220px at 100% 100%,rgba(79,216,160,.35),transparent 60%),linear-gradient(140deg,#12385a,#1b6a7e)}
.life-banner h2{font-size:clamp(1.6rem,4vw,2.4rem);font-weight:700;position:relative;z-index:1}
.life-banner svg{position:absolute;right:-30px;top:50%;transform:translateY(-50%);opacity:.22;width:340px;height:340px}
.life-card{min-height:300px;padding:26px}
.life-card .ico{font-size:2rem;margin-bottom:8px}
.life-card h3{font-size:1.2rem;color:var(--navy);margin-bottom:10px}

/* ---------- slide 9 & 10 ---------- */
.q-item{padding:18px 0;border-top:1px solid var(--line)}
.q-item:first-child{border-top:0;padding-top:4px}
.q-text{font-weight:700;color:var(--navy);margin-bottom:10px}
.opts{display:grid;gap:8px}
.opt{display:flex;gap:12px;align-items:flex-start;text-align:left;width:100%;padding:12px 14px;border-radius:12px;border:2px solid var(--line);background:#fff;color:var(--ink);transition:border-color .15s,background .15s}
.opt:hover:not([disabled]){border-color:var(--sky);background:#f2f8ff}
.opt .lt{flex:none;width:26px;height:26px;border-radius:50%;display:grid;place-items:center;font-weight:700;font-size:.82rem;background:#e4eefc;color:var(--blue)}
.opt.ok{border-color:var(--mint);background:#e9fbf3}
.opt.ok .lt{background:var(--mint);color:#06361f}
.opt.bad{border-color:var(--rose);background:#fff0f2}
.opt.bad .lt{background:var(--rose);color:#4a0a14}
.opt[disabled]{cursor:default}
.reason{border-radius:16px;padding:18px 20px;background:#eef4fd;border:1px dashed #b8cde9;color:#33445d}
.reason b{color:var(--navy)}
.reason.ok{background:#e9fbf3;border:1px solid #b3ecd3}
.reason.bad{background:#fff3e6;border:1px solid #f6d3a8}
.quiz-bar{display:flex;justify-content:space-between;flex-wrap:wrap;gap:10px;font-weight:700;color:var(--navy)}
.quiz-bar .sc{color:var(--blue)}
.result{text-align:center;padding:18px 8px}
.result .big{font-family:"Sora",sans-serif;font-size:3.4rem;font-weight:800;color:var(--blue)}
.result p{color:var(--muted);margin-top:6px}

/* ---------- slide 11 ---------- */
.rc{padding:20px}
.rc .n{font-family:"Sora",sans-serif;font-weight:800;color:var(--sky);font-size:1.2rem;margin-bottom:4px}
.rc h3{font-size:1.05rem;margin-bottom:6px}
.rc p{font-size:.92rem}
.mis{background:#fff7f0;border:1px solid #f6d3a8;border-radius:18px;padding:22px 24px}
.mis h3{color:#8a4300;margin-bottom:12px;font-size:1.15rem}
.mis ul{margin:0;padding:0;list-style:none;display:grid;gap:12px}
.mis li{display:grid;gap:2px;font-size:.95rem}
.mis li s{color:#a0562b;text-decoration-thickness:2px}
.mis li span{color:#1d6b46}
.save-row{display:flex;flex-wrap:wrap;align-items:center;justify-content:center;gap:14px;border:1px solid var(--line);border-radius:18px;padding:18px;background:#fff}
.save-row .msg{color:#1d6b46;font-weight:600;min-height:1.4em}
.foot{margin-top:6px;border-radius:20px;background:linear-gradient(150deg,#0a1530,#1c3c70);color:#dbe9ff;display:flex;flex-wrap:wrap;gap:12px;align-items:center;justify-content:space-between;padding:20px 24px}
.foot b{font-family:"Sora",sans-serif;color:#fff}
.foot .btn{padding:10px 16px}

/* ---------- modal orbital ---------- */
.modal{position:fixed;inset:0;z-index:50;display:none;align-items:center;justify-content:center;padding:16px;background:rgba(6,12,26,.72)}
.modal.open{display:flex}
.modal-card{background:#fff;border-radius:22px;width:min(640px,100%);max-height:92vh;overflow:auto;padding:24px;animation:pop .22s ease-out}
@keyframes pop{from{transform:scale(.96);opacity:0}to{transform:none;opacity:1}}
.modal-card .top{display:flex;justify-content:space-between;align-items:center;gap:10px;margin-bottom:12px}
.modal-card h3{font-size:1.25rem;color:var(--navy)}
.x{width:40px;height:40px;border-radius:50%;border:1px solid var(--line);background:#fff;font-size:1.1rem}
.mod-orbs{display:flex;flex-wrap:wrap;gap:12px;justify-content:center;padding:16px 8px;background:#f3f7fd;border-radius:16px}
.mod-orbs .g{text-align:center}
.mod-orbs .g .nm{font-family:"Sora",sans-serif;font-weight:700;color:var(--navy);margin-bottom:6px}
.mod-info{margin:14px 0;padding:14px 16px;border-radius:14px;background:#eef4fd;min-height:4.6em;color:#33445d}
.mod-ctl{display:flex;gap:10px;flex-wrap:wrap;align-items:center}
.mod-ctl .cnt{margin-left:auto;font-weight:700;color:var(--blue)}



/* hero muat dalam satu layar */
.hero .wrap{gap:clamp(8px,1.7vh,20px)}
.hero .logo{width:clamp(52px,8vh,76px);height:clamp(52px,8vh,76px);border-radius:20px}
.hero .logo svg{width:70%;height:70%}
.hero h1{font-size:clamp(2rem,min(7vw,8.5vh),4.2rem);max-width:none}
.hero .brand{font-size:clamp(1.6rem,min(5vw,5.5vh),2.6rem)}
.hero .nav{gap:6px}
.hero .nav a{padding:7px 12px;font-size:.82rem}
.hero .desc{font-size:clamp(.92rem,2vh,1.05rem)}
.hero .badge{padding:8px 10px}
.hero .btn{padding:11px 20px}
.hero-illus svg{max-height:clamp(120px,22vh,260px)}


@media (min-width:700px) and (max-height:1100px){
  #slide-1{padding-top:18px}
  .hero .wrap{gap:8px}
  .hero .logo{width:48px;height:48px;border-radius:14px}
  .hero .nav{gap:5px;flex-wrap:wrap}
  .hero .nav a{padding:6px 9px;font-size:.76rem;white-space:nowrap}
  .hero .nav b{margin-right:4px}
  .hero .brand{font-size:1.7rem;padding-right:18px}
  .hero .brand-sub{font-size:.95rem;padding-left:18px}
  .hero .progress .row{margin-bottom:3px;font-size:.78rem}
  .hero .track{height:8px}
  .hero-label{font-size:.82rem;padding:4px 14px}
  .hero h1{font-size:clamp(1.9rem,7.4vh,3.2rem)}
  .hero .desc{font-size:.9rem;max-width:84ch;line-height:1.5}
  .hero .badge{padding:6px 10px;font-size:.8rem}
  .hero .btn{padding:9px 18px;font-size:.92rem}
  .hero
