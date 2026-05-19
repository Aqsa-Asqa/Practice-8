<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1.0,user-scalable=no"/>
<title>Aqsa Noreen 🎂</title>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Nunito:wght@400;700;900&display=swap" rel="stylesheet"/>
<style>
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Nunito',sans-serif;background:#020d05;color:#e8fff2;min-height:100vh;overflow-x:hidden}
canvas#bgc{position:fixed;inset:0;z-index:0;pointer-events:none}
#wrap{position:relative;z-index:1;max-width:520px;margin:0 auto;padding:20px 14px 60px;min-height:100vh;display:flex;flex-direction:column;justify-content:center}
.page{display:none;flex-direction:column;gap:18px;animation:fadeIn .6s ease forwards}
.page.active{display:flex}
@keyframes fadeIn{from{opacity:0;transform:translateY(22px)}to{opacity:1;transform:none}}
.card{background:rgba(0,20,10,.82);border:1px solid rgba(0,255,136,.22);border-radius:20px;padding:26px 20px;backdrop-filter:blur(14px);box-shadow:0 0 30px rgba(0,255,136,.1),0 4px 20px rgba(0,0,0,.5)}
.center{text-align:center}
h1{font-family:'Pacifico',cursive;font-size:clamp(22px,6vw,34px);text-align:center;background:linear-gradient(135deg,#00ff88,#b9ffd6,#00e676);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;margin:10px 0}
.sub{color:#b9ffd6;font-size:14px;line-height:1.85;text-align:center}
.cake{font-size:72px;display:inline-block;animation:bounce 1.2s ease-in-out infinite alternate,vibe .18s linear infinite;filter:drop-shadow(0 0 18px #00ff88)}
@keyframes bounce{from{transform:translateY(0)}to{transform:translateY(-14px)}}
@keyframes vibe{0%,100%{transform:translate(0,0)}25%{transform:translate(-2px,1px)}75%{transform:translate(2px,-1px)}}
.big-emoji{font-size:56px;text-align:center;display:block;margin-bottom:8px;animation:popIn .5s ease;filter:drop-shadow(0 0 12px #00ff88)}
@keyframes popIn{from{transform:scale(0)}to{transform:scale(1)}}
.hearts{text-align:center;font-size:26px;letter-spacing:4px;animation:vibe .14s linear infinite;filter:drop-shadow(0 0 6px #00ff88);margin:8px 0}
.celebrate{text-align:center;font-size:30px;letter-spacing:2px;margin:6px 0}
.msg{font-size:15px;line-height:1.9;color:#b9ffd6}
.msg strong{color:#00ff88;text-shadow:0 0 8px #39ff14}
.sign{font-family:'Pacifico',cursive;font-size:20px;text-align:center;color:#00ff88;text-shadow:0 0 12px #39ff14;margin-top:18px}
.dot-label{color:#00ff88;font-size:11px;letter-spacing:2px;text-transform:uppercase;font-weight:700;text-align:center;margin-bottom:4px}

/* NEXT BUTTON */
.next-btn{display:block;margin:0 auto;background:linear-gradient(135deg,#00c853,#00ff88);border:none;border-radius:50px;color:#002b10;font-family:'Pacifico',cursive;font-size:17px;padding:15px 40px;cursor:pointer;box-shadow:0 0 24px #39ff14,0 4px 16px rgba(0,0,0,.4);transition:transform .15s,box-shadow .2s;animation:vibe .15s linear infinite}
.next-btn:hover{transform:scale(1.07);box-shadow:0 0 44px #39ff14}

/* CONFETTI BTN */
.celebbtn{display:block;margin:0 auto;background:linear-gradient(135deg,#00c853,#00ff88);border:none;border-radius:50px;color:#002b10;font-family:'Pacifico',cursive;font-size:16px;padding:14px 34px;cursor:pointer;box-shadow:0 0 22px #39ff14;animation:vibe .16s linear infinite}
.celebbtn:hover{transform:scale(1.07)}

/* PAGE DOTS */
.dots{display:flex;justify-content:center;gap:8px;margin-top:6px}
.dot{width:8px;height:8px;border-radius:50%;background:rgba(0,255,136,.3);transition:.3s}
.dot.on{background:#00ff88;box-shadow:0 0 8px #00ff88;transform:scale(1.3)}

/* PARTICLES + RINGS */
.particle{position:fixed;border-radius:50%;background:#00ff88;pointer-events:none;z-index:0;animation:floatUp linear infinite}
@keyframes floatUp{0%{opacity:.5;transform:translateY(0) scale(1)}100%{opacity:0;transform:translateY(-110vh) scale(0)}}
.ring{position:fixed;border-radius:50%;border:1.5px solid #00e676;opacity:0;animation:ringp 4s ease-out infinite;pointer-events:none;z-index:0}
@keyframes ringp{0%{transform:translate(-50%,-50%) scale(0);opacity:.6}100%{transform:translate(-50%,-50%) scale(4);opacity:0}}

/* CONFETTI */
.confp{position:fixed;top:-20px;border-radius:2px;pointer-events:none;z-index:9999;animation:fall linear forwards}
@keyframes fall{0%{transform:translateY(0) rotate(0deg);opacity:1}100%{transform:translateY(110vh) rotate(720deg);opacity:0}}
</style>
</head>
<body>
<canvas id="bgc"></canvas>

<div id="wrap">

  <!-- PAGE 1: WELCOME -->
  <div class="page active" id="p1">
    <div class="card center">
      <span class="cake">🎂</span>
      <p class="dot-label" style="margin-top:12px">Ek Khaas Message Hai</p>
      <h1>Aqsa Noreen</h1>
      <p class="sub">Ek khaas Bandii keliee..!!!<br><br>
        Arey ruko ruko! 🙅‍♂️<br>
        Ye link randomly nahi khola...<br>
        kisi ne <strong style="color:#00ff88">specially</strong> banaa ky bheja hai 👀
      </p>
    </div>
    <button class="next-btn" onclick="goTo(2)">Aagay Chalein →</button>
    <div class="dots" id="dots"></div>
  </div>

  <!-- PAGE 2: YOU ARE SPECIAL -->
  <div class="page" id="p2">
    <div class="card center">
      <span class="big-emoji">💌</span>
      <h1>Tum Khaas Ho!</h1>
      <p class="sub" style="margin-top:10px">
        From fighting with you...<br>
        to teasing you endlessly...<br>
        to calling you <strong style="color:#00ff88">Chirri / Asqa wgera wgera</strong> every other minute...<br><br>
        You've become someone really special in my life 💚
      </p>
    </div>
    <button class="next-btn" onclick="goTo(3)">Aagay Chalein →</button>
    <div class="dots" id="dots2"></div>
  </div>

  <!-- PAGE 3: DUA / PRAYER -->
  <div class="page" id="p3">
    <div class="card center">
      <span class="big-emoji">🤲</span>
      <h1>Dil Se Dua</h1>
      <p class="sub" style="margin-top:10px">
        I pray that your life is filled with<br>
        <strong style="color:#00ff88">happiness, success, and peace.</strong><br><br>
        May you achieve everything you dream of 🤲✨<br><br>
        And honestly... I hope we keep fighting<br>
        like idiots forever 😄<br><br>
        😌 Because life without irritating you<br>
        would be... kinda boring.
      </p>
    </div>
    <button class="next-btn" onclick="goTo(4)">Aagay Chalein →</button>
    <div class="dots" id="dots3"></div>
  </div>

  <!-- PAGE 4: BIRTHDAY MESSAGE -->
  <div class="page" id="p4">
    <div class="card center">
      <span class="big-emoji">👑</span>
      <h1>Happy Birthday<br>!!..ASQA..!!</h1>
      <div class="hearts">💚💚💚💚💚</div>
      <div class="celebrate">🎉🎊🥳🎈🎁✨</div>
      <p class="sub" style="margin-top:10px">
        Stay the same crazy, annoying,<br>
        amazing person you are 💚<br><br>
        <strong style="color:#00ff88">Forever your… favorite problem 😎</strong>
      </p>
      <div class="hearts" style="margin-top:10px">💚💚💚💚💚💚💚</div>
      <div class="sign" style="margin-top:14px">💚💚 Your Bachaaa 💚💚</div>
    </div>
    <button class="celebbtn" onclick="blast()">🎉 Confetti Chalaao!</button>
    <div class="dots" id="dots4"></div>
  </div>

</div>

<script>
/* ── CANVAS BG ── */
const cv=document.getElementById('bgc'),cx=cv.getContext('2d');
function rsz(){cv.width=innerWidth;cv.height=innerHeight}
rsz();window.addEventListener('resize',rsz);
let t=0;
(function frame(){
  cx.clearRect(0,0,cv.width,cv.height);
  const g=cx.createRadialGradient(cv.width/2,cv.height/2,0,cv.width/2,cv.height/2,Math.max(cv.width,cv.height));
  g.addColorStop(0,'#0a3b1a');g.addColorStop(.6,'#041a0a');g.addColorStop(1,'#020d05');
  cx.fillStyle=g;cx.fillRect(0,0,cv.width,cv.height);
  const sp=34;
  for(let x=0;x<cv.width+sp;x+=sp)for(let y=0;y<cv.height+sp;y+=sp){
    const w=Math.sin((x+y)*.04+t)*.5+.5;
    cx.beginPath();cx.arc(x,y,w*3+.8,0,Math.PI*2);
    cx.fillStyle=`rgba(0,255,136,${w*.2+.03})`;cx.fill();
  }
  for(let i=0;i<5;i++){
    const yb=(cv.height/5)*i;cx.beginPath();cx.moveTo(0,yb);
    for(let x=0;x<=cv.width;x+=4)cx.lineTo(x,yb+Math.sin(x*.009+t+i)*38);
    cx.strokeStyle=`rgba(0,255,136,${.04+i*.012})`;cx.lineWidth=1.2;cx.stroke();
  }
  t+=.022;requestAnimationFrame(frame);
})();

/* ── PARTICLES ── */
for(let i=0;i<28;i++){
  const p=document.createElement('div');p.className='particle';
  const s=Math.random()*5+2;
  p.style.cssText=`width:${s}px;height:${s}px;left:${Math.random()*100}vw;bottom:${Math.random()*20}vh;animation-duration:${Math.random()*10+6}s;animation-delay:${Math.random()*8}s`;
  document.body.appendChild(p);
}

/* ── RINGS ── */
for(let i=0;i<4;i++){
  const r=document.createElement('div');r.className='ring';
  r.style.cssText=`width:${300+i*80}px;height:${300+i*80}px;left:50%;top:50%;animation-delay:${i}s`;
  document.body.appendChild(r);
}

/* ── PAGE NAVIGATION ── */
const TOTAL=4;
let cur=1;

function renderDots(){
  ['dots','dots2','dots3','dots4'].forEach((id,pi)=>{
    const el=document.getElementById(id);
    if(!el)return;
    el.innerHTML='';
    for(let i=1;i<=TOTAL;i++){
      const d=document.createElement('div');
      d.className='dot'+(i===cur?' on':'');
      el.appendChild(d);
    }
  });
}

function goTo(n){
  document.getElementById('p'+cur).classList.remove('active');
  cur=n;
  const next=document.getElementById('p'+cur);
  next.classList.add('active');
  next.style.animation='none';
  next.offsetHeight;
  next.style.animation='';
  renderDots();
  window.scrollTo({top:0,behavior:'smooth'});
  if(n===4) setTimeout(blast,400);
}

renderDots();

/* ── CONFETTI ── */
const cols=['#00ff88','#39ff14','#00e676','#b9ffd6','#fff176','#80ff80','#00bfa5'];
function blast(){
  for(let i=0;i<90;i++){
    setTimeout(()=>{
      const c=document.createElement('div');c.className='confp';
      const s=Math.random()*10+5;
      c.style.cssText=`left:${Math.random()*100}vw;background:${cols[Math.floor(Math.random()*cols.length)]};width:${s}px;height:${s}px;border-radius:${Math.random()>.5?'50%':'2px'};animation-duration:${Math.random()*2+1.4}s`;
      document.body.appendChild(c);setTimeout(()=>c.remove(),3500);
    },i*16);
  }
}
</script>
</body>
</html>
