❤️STORY WORLD ❤️
<html lang="hi">
<head>
<meta charset="UTF-8">
<title>Gourav Yadav Story World</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
:root{--bg:#fff;--text:#111;--card:#ffe6f0;--btn:#ff4d6d;}
body.dark{--bg:#111;--text:#fff;--card:#1a1a1a;--btn:#ff4d6d;}
body{margin:0;font-family:Arial;background:var(--bg);color:var(--text);}
.header{text-align:center;padding:18px;font-size:24px;font-weight:bold;color:#ff4d6d;}
.theme-btn{position:fixed;top:10px;right:10px;padding:8px 14px;border:none;border-radius:20px;background:var(--btn);color:#fff;cursor:pointer;z-index:10;}
.categories{display:flex;flex-wrap:wrap;justify-content:center;gap:8px;margin:12px;}
.categories button{padding:7px 14px;border:none;border-radius:18px;background:#ccc;font-weight:bold;cursor:pointer;}
.categories button.active{background:var(--btn);color:#fff;}
.story-container{max-width:420px;height:75vh;margin:auto;background:var(--card);border-radius:22px;padding:18px;box-shadow:0 0 25px rgba(255,77,109,.5);display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;position:relative;overflow:hidden;}
.story-line{opacity:0;margin:7px 0;font-size:18px;animation:fade .8s forwards;}
@keyframes fade{to{opacity:1}}
.progress{width:90%;height:5px;background:#ccc;border-radius:5px;overflow:hidden;margin-bottom:10px;}
.progress-bar{height:100%;width:0;background:var(--btn);animation:load 10s linear forwards;}
@keyframes load{to{width:100%}}
.dots{display:flex;gap:6px;margin-top:10px}
.dot{width:9px;height:9px;background:#bbb;border-radius:50%}
.dot.active{background:var(--btn)}
.actions{display:flex;gap:12px;margin-top:14px;}
.actions button{padding:7px 15px;border:none;border-radius:20px;background:var(--btn);color:#fff;font-weight:bold;cursor:pointer;}
.footer{text-align:center;padding:15px;color:#ff4d6d}

/* Admin Panel Custom */
#adminPanel{display:none;position:fixed;inset:0;z-index:999;align-items:center;justify-content:center;backdrop-filter:blur(8px);}
#adminPanel > div{background:linear-gradient(135deg,#ff4d6d,#ff85b3);color:#fff;width:90%;max-width:400px;padding:25px;border-radius:25px;box-shadow:0 0 20px rgba(0,0,0,0.5);transform:scale(0);opacity:0;transition:0.3s;}
#adminPanel.show > div{transform:scale(1);opacity:1;}
#adminPanel h3{text-align:center;color:#fff;margin-bottom:15px;font-size:22px;}
#adminPanel input,#adminPanel textarea,#adminPanel select{width:100%;margin:10px 0;padding:12px;border-radius:12px;border:none;}
#adminPanel textarea{resize:none;}
#adminPanel button{width:100%;padding:12px;border:none;border-radius:25px;margin-top:8px;cursor:pointer;font-weight:bold;}
#adminPanel button.addBtn{background:#fff;color:#ff4d6d;}
#adminPanel button.closeBtn{background:#333;color:#fff;}
#loginBox input{background:rgba(255,255,255,0.3);color:#fff;}
#loginBox button{background:#fff;color:#ff4d6d;}
</style>
</head>
<body class="dark">

<div class="header">Gourav Yadav Story World ❤️</div>
<button class="theme-btn" onclick="toggleTheme()">🌙 Theme</button>
<button class="theme-btn" style="left:10px;right:auto" onclick="openAdmin()">📝 Admin</button>

<div class="categories">
  <button class="active" onclick="changeCategory('love',this)">❤️ Love</button>
  <button onclick="changeCategory('sad',this)">💔 Sad</button>
  <button onclick="changeCategory('horror',this)">👻 Horror</button>
  <button onclick="changeCategory('motivation',this)">💪 Motivation</button>
  <button onclick="changeCategory('friendship',this)">🤝 Friendship</button>
  <button onclick="changeCategory('attitude',this)">😎 Attitude</button>
  <button onclick="changeCategory('life',this)">🌙 Life</button>
</div>

<div class="story-container" id="storyBox">
  <div class="progress"><div class="progress-bar" id="bar"></div></div>
  <div id="storyText"></div>
  <div class="dots" id="dots"></div>
  <div class="actions">
    <button onclick="likeStory()">❤️ Like</button>
    <button onclick="copyStory()">📋 Copy</button>
    <button onclick="toggleVoice()" id="voiceBtn">▶️ Play Voice</button>
  </div>
</div>

<div class="footer">© 2026 Gourav Yadav</div>

<!-- Admin Panel -->
<div id="adminPanel">
<div>
<h3>Admin Panel Login</h3>
<div id="loginBox">
<input id="adminUser" type="text" placeholder="storldworld02">
<input id="adminPass" type="password" placeholder="gourav123">
<button onclick="adminLogin()">Login</button>
</div>
<div id="storyBoxAdmin" style="display:none">
<select id="adminCategory">
  <option value="love">Love</option>
  <option value="sad">Sad</option>
  <option value="horror">Horror</option>
  <option value="motivation">Motivation</option>
  <option value="friendship">Friendship</option>
  <option value="attitude">Attitude</option>
  <option value="life">Life</option>
</select>
<textarea id=""adminStory" rows="8" placeholder="हर लाइन नई line में लिखें"></textarea>
<button class="addBtn" onclick="saveStory()">➕ Add Story</button>
<button class="closeBtn" onclick="closeAdmin()">❌ Close</button>
</div>
</div>
</div>

<script>
let stories = {love:[],sad:[],horror:[],motivation:[],friendship:[],attitude:[],life:[]};
let saved = localStorage.getItem("storiesData");
if(saved){Object.assign(stories, JSON.parse(saved));}

let current="love",i=0;
const storyText=document.getElementById("storyText");
const dots=document.getElementById("dots");
const bar=document.getElementById("bar");
const voiceBtn=document.getElementById("voiceBtn");
let synth=window.speechSynthesis,voiceOn=false,utter;

function loadStory(){
 storyText.innerHTML="";
 bar.style.animation="none";bar.offsetHeight;bar.style.animation="load 10s linear forwards";
 if(stories[current][i]){
   stories[current][i].forEach((l,idx)=>{
     let d=document.createElement("div");
     d.className="story-line";
     d.style.animationDelay=`${idx*0.5}s`;
     d.innerText=l;
     storyText.appendChild(d);
   });
 }
 dots.innerHTML="";
 stories[current].forEach((_,x)=>{
   let dot=document.createElement("div");
   dot.className="dot"+(x===i?" active":"");
   dots.appendChild(dot);
 });
 speakStory();
}
function changeCategory(cat,btn){current=cat;i=0;document.querySelectorAll(".categories button").forEach(x=>x.classList.remove("active"));btn.classList.add("active");loadStory();}
function likeStory(){alert("❤️ Story Liked")}
function copyStory(){if(stories[current][i]){navigator.clipboard.writeText(stories[current][i].join("\n"));alert("📋 Story Copied");}}
function toggleVoice(){voiceOn=!voiceOn;voiceBtn.innerText=voiceOn?"⏸ Pause Voice":"▶️ Play Voice";if(!voiceOn)synth.cancel();else speakStory();}
function speakStory(){if(!voiceOn)return;if(synth.speaking)synth.cancel();if(stories[current][i]){utter=new SpeechSynthesisUtterance(stories[current][i].join(" । "));utter.lang="hi-IN";utter.rate=0.9;synth.speak(utter);}}
let sx=0;
const storyBox=document.getElementById("storyBox");
storyBox.addEventListener("touchstart",e=>sx=e.touches[0].clientX);
storyBox.addEventListener("touchend",e=>{let d=sx-e.changedTouches[0].clientX;if(Math.abs(d)>30){i=d>0?(i+1)%stories[current].length:(i-1+stories[current].length)%stories[current].length;loadStory();}});
storyBox.addEventListener("mousedown",e=>sx=e.clientX);
storyBox.addEventListener("mouseup",e=>{let d=sx-e.clientX;if(Math.abs(d)>30){i=d>0?(i+1)%stories[current].length:(i-1+stories[current].length)%stories[current].length;loadStory();}});
function toggleTheme(){document.body.classList.toggle("dark")}
loadStory();

// Admin
function openAdmin(){document.getElementById("adminPanel").style.display="flex";document.getElementById("adminPanel").classList.add("show");}
function closeAdmin(){document.getElementById("adminPanel").style.display="none";document.getElementById("adminPanel").classList.remove("show");}
function adminLogin(){
  let user=document.getElementById("adminUser").value.trim();
  let pass=document.getElementById("adminPass").value.trim();
  if(user==="storyworld02" && pass==="gourav123"){
    document.getElementById("loginBox").style.display="none";
    document.getElementById("storyBoxAdmin").style.display="block";
  } else { alert("❌ Wrong Username or Password "); }
}
function saveStory(){
  let cat=document.getElementById("adminCategory").value;
  let text=document.getElementById("adminStory").value.trim();
  if(!text) return alert("Story लिखो");
  let lines=text.split("\n").filter(l=>l.trim()!=="");
  if(!stories[cat]) stories[cat]=[];
  stories[cat].push(lines);
  localStorage.setItem("storiesData",JSON.stringify(stories));
  alert("✅ Story Added Successfully");
  document.getElementById("adminStory").value="";
  loadStory();
}
</script>
</body>
</html>

