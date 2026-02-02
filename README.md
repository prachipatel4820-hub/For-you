<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Only For You ❤️</title>
  <style>
    *{box-sizing:border-box;margin:0;padding:0;font-family:'Segoe UI',sans-serif}
    body{
      background:linear-gradient(135deg,#ff9a9e,#fad0c4);
      min-height:100vh;
      overflow:hidden;
      color:#fff;
    }
    .card{
      display:none;
      position:absolute;
      inset:0;
      padding:30px 20px;
      text-align:center;
      animation:fadeIn 0.8s ease;
    }
    .card.active{display:flex;flex-direction:column;justify-content:center;align-items:center}
    h1,h2{margin-bottom:15px}
    p{font-size:18px;line-height:1.7;margin-bottom:20px}
    .next{
      margin-top:25px;
      font-size:18px;
      cursor:pointer;
      color:#fff;
      text-decoration:underline;
    }
    @keyframes fadeIn{from{opacity:0;transform:scale(.97)}to{opacity:1;transform:scale(1)}}

    /* Letters grid */
    .letters-grid{
      display:grid;
      grid-template-columns:repeat(2,1fr);
      gap:12px;
      width:100%;
      max-width:420px;
      margin:10px auto;
    }
    .letter{
      background:rgba(255,255,255,0.2);
      padding:14px;
      border-radius:14px;
      filter:blur(6px);
      cursor:pointer;
      transition:all 0.5s ease;
      font-size:15px;
      color:#fff;
    }
    .letter img{
      display:none;
      width:100%;
      border-radius:16px;
      margin-top:18px;
      opacity:0;
      transform:translateY(10px);
      transition:all 0.6s ease;
    }
    .letter.open img{
      display:block;
      opacity:1;
      transform:translateY(0);
    }
    .hint{
      font-size:14px;
      color:#888;
      margin-top:10px;
    }
    .letter.open img{display:block}
    }
    .letter:hover{transform:scale(1.03)}
    .letter.open{
      position:fixed;
      inset:15% 8%;
      background:#fff;
      color:#d6336c;
      filter:blur(0);
      z-index:1001;
      font-size:18px;
      line-height:1.7;
      padding:25px;
      border-radius:20px;
      overflow:auto;
    }

    .overlay{
      display:none;
      position:fixed;
      inset:0;
      background:rgba(0,0,0,0.5);
      z-index:1000;
    }
    .overlay.show{display:block}

    /* Hug */
    .hug-btn{padding:15px 25px;background:#ff4b6e;border-radius:30px;cursor:pointer;margin-top:15px}
    body.hugged{animation:hug 0.6s ease}
    @keyframes hug{0%{transform:scale(1)}50%{transform:scale(0.97)}100%{transform:scale(1)}}

    /* Puzzle */
    .puzzle{display:grid;grid-template-columns:repeat(5,1fr);gap:4px;width:90%;max-width:360px;margin:15px auto}
    .piece{width:100%;padding-top:60%;background-image:url('photo.jpg');background-size:500% 300%;border-radius:6px}

    /* Hearts */
    .heart{position:fixed;color:#ff4b6e;font-size:18px;animation:float 2s ease forwards;pointer-events:none}
    @keyframes float{to{transform:translateY(-80px);opacity:0}}

    input{padding:10px;border:none;border-radius:6px}
  </style>
</head>
<body>

<audio id="song1" src="A Thousand Years.mp3" autoplay loop></audio>
<audio id="song2" src="Perfect.mp3"></audio>

<div class="card active">
  <h1>Hey Love ❤️</h1>
  <p>Even if I’m far away… my heart is holding yours.</p>
  <div class="next">Come closer 🤍</div>
</div>

<div class="card">
  <h2>My Letters For You 💌</h2>
  <p>All letters are hidden… touch one gently 🤍</p>
  <div class="letters-grid">
    <div class="letter" onclick="openLetter(this)"><b><strong>Letter 1</strong> · 🌹 Rose Day</b><br><br>ગુલાબ ની જેમ આખી જિંદગી તારા જીવન માં સુગંધ ભેળવી દેવા ❤️<div class="hint">This memory is only ours 🤍</div></b><br><br>ગુલાબ ની જેમ આખી જિંદગી તારા જીવન માં સુગંધ ભેળવી દેવા ❤️<img src="IMG_20260202_184410_258.jpg" alt="Rose Day"></b><br><br>ગુલાબ ની જેમ આખી જિંદગી તારા જીવન માં સુગંધ ભેળવી દેવા ❤️</div>
    <div class="letter" onclick="openLetter(this)"><b><strong>Letter 2</strong> · 💞 Propose Day</b><br><br>તું મને કઈ પણ પૂછશે હું તો હા જ પાડીશ ❤️<div class="hint">This memory is only ours 🤍</div></b><br><br>તું મને કઈ પણ પૂછશે હું તો હા જ પાડીશ ❤️<img src="IMG_20260202_184334_288.jpg" alt="Propose Day"></b><br><br>તું મને કઈ પણ પૂછશે હું તો હા જ પાડીશ ❤️</div>
    <div class="letter" onclick="openLetter(this)"><b><strong>Letter 3</strong> · 🍫 Chocolate Day</b><br><br>ચોકલેટ ની જેમ મીઠાશ તારા જીવન માં લાવવા ❤️<div class="hint">This memory is only ours 🤍</div></b><br><br>ચોકલેટ ની જેમ મીઠાશ તારા જીવન માં લાવવા ❤️<img src="IMG_20260202_184317_748.jpg" alt="Chocolate Day"></b><br><br>ચોકલેટ ની જેમ મીઠાશ તારા જીવન માં લાવવા ❤️</div>
    <div class="letter" onclick="openLetter(this)"><b><strong>Letter 4</strong> · 🐻 Teddy Day</b><br><br>Teddy Bear ની જેમ હંમેશા તને સુકુન આપવા ❤️<div class="hint">This memory is only ours 🤍</div></b><br><br>Teddy Bear ની જેમ હંમેશા તને સુકુન આપવા ❤️<img src="IMG_20260202_184410_258.jpg" alt="Teddy Day"></b><br><br>Teddy Bear ની જેમ હંમેશા તને સુકુન આપવા ❤️</div>
    <div class="letter" onclick="openLetter(this)"><b><strong>Letter 5</strong> · 🤝 Promise Day</b><br><br>હું તને Promise આપું છું હંમેશા તારો સાથ આપવાનો ❤️<div class="hint">This memory is only ours 🤍</div></b><br><br>હું તને Promise આપું છું હંમેશા તારો સાથ આપવાનો ❤️<img src="IMG_20260202_184334_288.jpg" alt="Promise Day"></b><br><br>હું તને Promise આપું છું હંમેશા તારો સાથ આપવાનો ❤️</div>
    <div class="letter" onclick="openLetter(this)"><b><strong>Letter 6</strong> · 🫂 Hug Day</b><br><br>આ રહ્યો મારું મોટું Hug ❤️<div class="hint">This memory is only ours 🤍</div></b><br><br>આ રહ્યો મારું મોટું Hug ❤️<img src="IMG_20260202_184317_748.jpg" alt="Hug Day"></b><br><br>આ રહ્યો મારું મોટું Hug ❤️</div>
    <div class="letter" onclick="openLetter(this)"><b><strong>Letter 7</strong> · 💋 Kiss Day</b><br><br>Virtual kisses just for you 😘<div class="hint">This memory is only ours 🤍</div></b><br><br>Virtual kisses just for you 😘<img src="IMG_20260202_184410_258.jpg" alt="Kiss Day"></b><br><br>Virtual kisses just for you 😘</div>
  </div>
  <div class="next">When you’re ready… let’s continue 🤍</div>
</div>

<div class="overlay" id="overlay" onclick="closeLetter()"></div>

<div class="card">
  <h2>Virtual Hug 🧸</h2>
  <div class="hug-btn" onclick="hug()">I need a hug</div>
  <div class="next">Hold it tight 🤍</div>
</div>

<div class="card">
  <h2>Only You 🔐</h2>
  <p>What do you call me?</p>
  <input type="password" id="pwd" placeholder="Type here" />
  <div class="next" onclick="checkPwd()">Unlock ❤️</div>
</div>

<div class="card">
  <h1>Will you be my Valentine? ❤️</h1>
  <p>એક હોઈ હા<br>એક હોઈ એકદમ હા<br>એક હોઈ અરે હા ભાઈ હા<br>અને આ એના થી પણ ઉપર હું હંમેશા તારો જ છું ❤️</p>
</div>

<script>
const cards=document.querySelectorAll('.card');
let i=0;
document.querySelectorAll('.next').forEach(btn=>{
  btn.addEventListener('click',()=>{
    if(!btn.onclick){
      cards[i].classList.remove('active');
      i++;
      if(cards[i]) cards[i].classList.add('active');
      if(i===cards.length-1){song1.pause();song2.play();}
    }
  });
});

function hug(){document.body.classList.add('hugged');setTimeout(()=>document.body.classList.remove('hugged'),600)}

function checkPwd(){
  if(pwd.value==='Pihu'){
    cards[i].classList.remove('active');i++;cards[i].classList.add('active');song1.pause();song2.play();
  } else alert('Hint: the name you lovingly call me ❤️');
}

function openLetter(el){
  document.getElementById('overlay').classList.add('show');
  el.classList.add('open');
}

function closeLetter(){
  document.getElementById('overlay').classList.remove('show');
  document.querySelectorAll('.letter.open').forEach(l=>l.classList.remove('open'));
}

setInterval(()=>{
  for(let k=0;k<4;k++){
    const h=document.createElement('div');
    h.className='heart';
    h.innerText='❤️';
    h.style.left=Math.random()*100+'%';
    h.style.top='80%';
    document.body.appendChild(h);
    setTimeout(()=>h.remove(),2200);
  }
},1100);
  h.className='heart';
  h.innerText='❤️';
  h.style.left=Math.random()*100+'%';
  h.style.top='80%';
  document.body.appendChild(h);
  setTimeout(()=>h.remove(),2000);
},1800);
</script>
</body>
</html>
