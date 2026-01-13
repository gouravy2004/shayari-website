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
#adminPanel{display:none;position:fixed;inset:0;background:rgba(0,0,0,.8);z-index:999;align-items:center;justify-content:center;}
#adminPanel > div{background:#fff;color:#111;width:90%;max-width:400px;padding:20px;border-radius:20px;}
#adminPanel h3{text-align:center;color:#ff4d6d;margin-bottom:10px;}
#adminPanel input,#adminPanel textarea,#adminPanel select{width:100%;margin:8px 0;padding:10px;border-radius:10px;border:1px solid #ccc;}
#adminPanel button{width:100%;padding:10px;border:none;border-radius:20px;margin-top:5px;cursor:pointer;}
#adminPanel button.addBtn{background:#ff4d6d;color:#fff;}
#adminPanel button.closeBtn{background:#333;color:#fff;}
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

<div class="footer">© 2026 designed Gourav Yadav</div>

<!-- ADMIN PANEL -->
<div id="adminPanel">
<div>
<h3>Admin Panel</h3>
<div id="loginBox">
<input id="adminPass" type="password" placeholder="Enter Password">
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
<textarea id="adminStory" rows="8" placeholder="हर लाइन नई line में लिखें"></textarea>
<button class="addBtn" onclick="saveStory()">➕ Add Story</button>
<button class="closeBtn" onclick="closeAdmin()">❌ Close</button>
</div>
</div>
</div>

<script>
let stories={
love:[
["उसकी मुस्कान ने दिल को छू लिया","बिना कहे बहुत कुछ कह दिया","हर सुबह उसकी याद आई","हर रात उसका ख्वाब आया","धीरे-धीरे समझ आया","प्यार आवाज़ नहीं","एक एहसास होता है","जो ज़िंदगी बदल देता है","हमेशा उसके ख्यालों में खो जाता हूँ","उसकी हँसी मेरे दिन को रोशन कर देती है","उसके बिना सब अधूरा लगता है","प्यार हर पल बढ़ता जाता है"]
],
sad:[
["भीड़ में भी अकेलापन लगा","हँसी के पीछे दर्द छुपा","रातें सवाल करती रहीं","नींद जवाब नहीं दे पाई","कुछ यादें चुभती रहीं","और हम चुपचाप सहते रहे","दिल टूटने का एहसास","कभी शब्दों में नहीं आता","आँखों से कह दिया","पर कोई नहीं समझा","यादें कभी नहीं मिटती","दर्द हमेशा साथ रहता है"]
],
horror:[
["कमरा अंधेरे में डूबा था","घड़ी बारह बजा चुकी थी","किसी ने मेरा नाम लिया","पीछे मुड़ा तो कोई नहीं","आईने में देखा","वहाँ कोई मुस्कुरा रहा था","दिल तेज़ी से धड़क रहा था","हवा चल रही थी","दरवाज़ा खुद बंद हुआ","कोई साया गुजरता दिखा","भूत की आवाज़ गूंज रही थी","और मैं कांपता रहा"]
],
motivation:[
["थक जाना हार नहीं","रुक जाना हार है","हर मुश्किल सबक है","हर दर्द ताकत बनता है","खुद पर भरोसा रखो","तुम बहुत आगे जाओगे","कभी पीछे मत देखो","सपनों को पकड़ो","मेहनत रंग लाएगी","हर असफलता एक सीख है","दृढ़ता सफलता लाएगी","अपने लक्ष्य पर कायम रहो"]
],
friendship:[
["दोस्ती नाम नहीं एक एहसास है","जो हर मुश्किल में साथ खड़ा हो","सच्चा दोस्त वही है","जो बिना कहे समझ जाए","साथ हँसना और साथ रोना","यादें हमेशा साथ रहती हैं","वक्त बदलता है पर दोस्ती नहीं","एक सच्चा दोस्त अनमोल है","जीवन में खुशियाँ बाँटता है","साथ होने से ताकत बढ़ती है","वफ़ादारी की मिसाल","दोस्ती अमर होती है"]
],
attitude:[
["हम चुप रहते हैं","क्योंकि शब्द कम हैं","जो समझे वही अपना है","दूसरों की नज़रों से मत डर","खुद की राह खुद बनाओ","शक्ति भीतर है","दिखावा छोड़ो","सफलता अपने आप आएगी","धैर्य रखो","हमेशा आगे बढ़ो","सकारात्मक सोच रखो","दुनिया पीछे रह जाएगी"]
],
life:[
["ज़िंदगी सीखों का सफ़र है","हर दिन कुछ सिखा जाता है","गलतियाँ अनुभव देती हैं","सफलता मेहनत मांगती है","खुश रहना एक कला है","सपने हमेशा देखो","उम्मीद मत खोना","दूसरों की तुलना मत करना","सकारात्मक सोच रखो","हर पल जियो","परिवार और दोस्त ज़रूरी हैं","हर दिन नई कहानी है"]
]
};

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
 stories[current][i].forEach((l,idx)=>{
  let d=document.createElement("div");d.className="story-line";
  d.style.animationDelay=`${idx*0.5}s`;d.innerText=l;
  storyText.appendChild(d);
 });
 dots.innerHTML="";
 stories[current].forEach((_,x)=>{let dot=document.createElement("div");dot.className="dot"+(x===i?" active":"");dots.appendChild(dot);});
 speakStory();
}
function changeCategory(cat,btn){current=cat;i=0;document.querySelectorAll(".categories button").forEach(x=>x.classList.remove("active"));btn.classList.add("active");loadStory();}
function likeStory(){alert("❤️ Story Liked")}
function copyStory(){navigator.clipboard.writeText(stories[current][i].join("\n"));alert("📋 Story Copied");}
function toggleVoice(){voiceOn=!voiceOn;voiceBtn.innerText=voiceOn?"⏸ Pause Voice":"▶️ Play Voice";if(!voiceOn)synth.cancel();else speakStory();}
function speakStory(){if(!voiceOn)return;if(synth.speaking)synth.cancel();utter=new SpeechSynthesisUtterance(stories[current][i].join(" । "));utter.lang="hi-IN";utter.rate=0.9;synth.speak(utter);}
let sx=0;const storyBox=document.getElementById("storyBox");
storyBox.addEventListener("touchstart",e=>sx=e.touches[0].clientX);
storyBox.addEventListener("touchend",e=>{let d=sx-e.changedTouches[0].clientX;if(Math.abs(d)>30){i=d>0?(i+1)%stories[current].length:(i-1+stories[current].length)%stories[current].length;loadStory();}});
storyBox.addEventListener("mousedown",e=>sx=e.clientX);
storyBox.addEventListener("mouseup",e=>{let d=sx-e.clientX;if(Math.abs(d)>30){i=d>0?(i+1)%stories[current].length:(i-1+stories[current].length)%stories[current].length;loadStory();}});
function toggleTheme(){document.body.classList.toggle("dark")}

// ADMIN PANEL
function openAdmin(){document.getElementById("adminPanel").style.display="flex";}
function closeAdmin(){document.getElementById("adminPanel").style.display="none";}
function adminLogin(){let pass=document.getElementById("adminPass").value;if(pass==="admin123"){document.getElementById("loginBox").style.display="none";document.getElementById("storyBoxAdmin").style.display="block";}else{alert("storygy or gourav123");}}
function saveStory(){let cat=document.getElementById("adminCategory").value;let text=document.getElementById("adminStory").value.trim();if(!text)return alert("Story लिखो");let lines=text.split("\n").filter(l=>l.trim()!=="");if(!stories[cat])stories[cat]=[];stories[cat].push(lines);localStorage.setItem("storiesData",JSON.stringify(stories));alert("✅ Story Added Successfully");document.getElementById("adminStory").value="";loadStory();}

loadStory();
</script>
</body>
</html>

