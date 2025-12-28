<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>new year</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Trebuchet MS';
}

body{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:black;
    overflow:hidden;
    color:red;
}

/* SCREENS */
.screen{
    display:none;
    width:100%;
    text-align:center;
    padding:20px;
}
.screen.active{display:block;}

/* BUTTON */
button,.btn{
    margin-top:20px;
    padding:10px 24px;
    border:none;
    border-radius:20px;
    background:#5C1A1A;
    color:red;
    cursor:pointer;
}

/* FORM */
.form-box{
    background:linear-gradient(135deg,#EF5350,#E53935,#B71C1C);
    padding:20px;
    border-radius:12px;
    width:300px;
    margin:auto;
    color:black;
}
input{
    width:100%;
    padding:8px;
    margin:8px 0;
    border-radius:6px;
    border:1px solid #ccc;
}

/* ENVELOPE OPEN */
.envelope{
    position:relative;
    width:300px;
    height:200px;
    margin:auto;
    background:linear-gradient(135deg,#EF5350,#E53935,#B71C1C);
    overflow:hidden;
}
.flap{
    position:absolute;
    inset:0;
    background:red;
    clip-path:polygon(0 0,100% 0,50% 50%);
    transform-origin:top;
    transition:0.8s ease;
}
.envelope.open .flap{
    transform:rotateX(180deg);
}
.open-btn{
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    background:none;
    border:none;
    font-size:18px;
    cursor:pointer;
    color:white;
    z-index:2;
}

/* REVEAL */
.reveal{
    display:flex;
    gap:20px;
    max-width:900px;
    margin:auto;
    align-items:center;
}
.left{flex:1;text-align:left;}
.item{
    background:#5C1A1A;
    padding:10px;
    margin:8px 0;
    border-radius:10px;
    opacity:0.4;
    cursor:pointer;
}
.item.show{opacity:1;}
.rose-img{width:260px; animation:fade 2s;}
@keyframes fade{
    from{opacity:0;transform:scale(0.8);}
    to{opacity:1;}
}

/* FINAL ENVELOPE */
.envelope-final{
    width:420px;
    height:260px;
    background:#5C1A1A;
    border:2px solid #ddd;
    border-radius:8px;
    margin:auto;
    position:relative;
    padding:20px;
    color:black;
}
.from{
    position:absolute;
    top:20px;
    left:20px;
}
.to{
    position:absolute;
    bottom:60px;
    left:50%;
    transform:translateX(-50%);
    text-align:center;
    font-weight:bold;
}
.stamp{
    position:absolute;
    top:20px;
    right:20px;
    width:60px;
    height:70px;
    border:2px dashed red;
    display:flex;
    align-items:center;
    justify-content:center;
    color:red;
}

/* FALLING GIFTS */
.falling-gift{
    position:absolute;
    top:-30px;
    font-size:24px;
    animation:fall linear infinite;
}
@keyframes fall{
    to{transform:translateY(110vh);opacity:0;}
}
</style>
</head>

<body>
<audio id="bgMusic" autoplay loop>
    <source src="friend.mp3" type="audio/mpeg">
</audio>


<!-- SCREEN 0 : ASK TO NAME ONLY -->
<div class="screen active" id="s0">
    <div class="form-box">
        <h2>✉️ 𝑬𝒏𝒕𝒆𝒓 𝒀𝒐𝒖𝒓 𝑵𝒂𝒎𝒆</h2>
        <input id="toName" placeholder="To">
        <button onclick="saveName()">𝑪𝒐𝒏𝒕𝒊𝒏𝒖𝒆</button>
    </div>
</div>

<!-- SCREEN 1 -->
<div class="screen" id="s1">
    <h1>🎁 𝑨 𝑺𝒖𝒓𝒑𝒓𝒊𝒔𝒆 𝒇𝒐𝒓 𝒀𝒐𝒖 🎁</h1>
    <div class="envelope" id="env">
        <div class="flap"></div>
        <button class="open-btn" onclick="openEnvelope()">👉👈<br><strong>𝒄𝒍𝒊𝒄𝒌 𝒎𝒆!</strong></button>
    </div>
</div>

<!-- SCREEN 2 -->
<div class="screen" id="s2">
    <h1>😊<br>𝑯𝒆𝒚 𝑭𝒓𝒊𝒆𝒏𝒅</h1>
    <h2>𝑵𝒆𝒘 𝒀𝒆𝒂𝒓 𝑮𝒊𝒇𝒕 𝒊𝒔 𝒘𝒂𝒊𝒕𝒊𝒏𝒈 <br> 𝒇𝒐𝒓 𝒚𝒐𝒖<br>𝒔𝒉𝒉𝒉...🤫 𝒔𝒆𝒄𝒓𝒆𝒕!!!</h2>
    <button onclick="go(3)">𝑶𝑷𝑬𝑵</button>
</div>

<!-- SCREEN 3 -->
<div class="screen" id="s3">
    <h1>💗 𝑻𝒂𝒑 𝒕𝒐 𝑹𝒆𝒗𝒆𝒂𝒍 💗</h1>

    <div class="reveal">
        <div class="left">
            <div class="item" onclick="this.classList.add('show')"><center>✨𝒔𝒖𝒓𝒑𝒓𝒊𝒔𝒆✨</center></div>
            <div class="item" onclick="this.classList.add('show')"><center>✨𝑯𝒂𝒑𝒑𝒚 𝑵𝒆𝒘 𝒀𝒆𝒂𝒓✨</center></div>
            <div class="item" onclick="this.classList.add('show')"><center>🥳 𝑪𝒐𝒏𝒈𝒓𝒂𝒕𝒖𝒍𝒂𝒕𝒊𝒐𝒏𝒔!! 𝒀𝒐𝒖 𝒋𝒖𝒔𝒕 𝒓𝒆𝒔𝒖𝒃𝒔𝒄𝒓𝒊𝒃𝒆𝒅 𝒕𝒐 𝒐𝒖𝒓 𝒇𝒓𝒊𝒆𝒏𝒅𝒔𝒉𝒊𝒑 𝒇𝒐𝒓 2026.🥳</center></div>
            <div class="item" onclick="this.classList.add('show')"><center>🫣𝑻𝒉𝒆𝒓'𝒔 𝒏𝒐 𝒘𝒂𝒚 𝒃𝒂𝒄𝒌🙂‍↔️</center></div>
            <div class="item" onclick="this.classList.add('show')"><center>𝑫𝒐𝒏’𝒕 𝒘𝒐𝒓𝒓𝒚,😄𝑰’𝒎 𝒉𝒆𝒓𝒆 𝒕𝒐 𝒊𝒓𝒓𝒊𝒕𝒂𝒕𝒆 𝒚𝒐𝒖 😁😉</center></div>
        </div>
        <img src="nn.gif" class="rose-img">
    </div>

    <button onclick="go(4)">𝑭𝒊𝒏𝒂𝒍𝒍𝒚 🎁</button>
</div>

<!-- SCREEN 4 : ADDRESS -->
<div class="screen" id="s4">
    <h2>📮 𝑨𝒅𝒅𝒓𝒆𝒔𝒔 𝑬𝒏𝒗𝒆𝒍𝒐𝒑𝒆</h2>
    <div class="envelope-final">
        <div class="from">𝑭𝒓𝒐𝒎,<br>𝒀𝒐𝒖𝒓 𝑭𝒓𝒊𝒆𝒏𝒅 💖</div>
        <div class="stamp">𝑺𝑻𝑨𝑴𝑷</div>
        <div class="to" id="toText"></div>
    </div>
</div>

<script>
const music = document.getElementById("bgMusic");

document.addEventListener("click", () => {
    if (music.paused) {
        music.play();
    }
}, { once: true });

let TO="";

function go(n){
    document.querySelectorAll('.screen').forEach(s=>s.classList.remove('active'));
    document.getElementById('s'+n).classList.add('active');

    if(n===4){
        document.getElementById("toText").innerHTML="To,<br>"+TO;
    }
}

function saveName(){
    TO = toName.value.trim();
    if(!TO){
        alert("Please enter your name");
        return;
    }
    go(1);
}

function openEnvelope(){
    document.getElementById("env").classList.add("open");
    setTimeout(()=>go(2),900);
}

/* Falling gifts */
setInterval(()=>{
    let g=document.createElement("div");
    g.className="falling-gift";
    g.innerText="🎁";
    g.style.left=Math.random()*innerWidth+"px";
    g.style.animationDuration=(Math.random()*3+2)+"s";
    document.body.appendChild(g);
    setTimeout(()=>g.remove(),5000);
},300);
</script>

</body>
</html>
