❤️STORY WORLD ❤️
<html lang="hi">
<head>
<meta charset="UTF-8">
<title>Gourav Yadav Story World</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
:root{
 --bg:#fff; --text:#111; --card:#ffe6f0; --btn:#ff4d6d;
}
body.dark{
 --bg:#111; --text:#fff; --card:#1a1a1a; --btn:#ff4d6d;
}
body{
 margin:0;font-family:Arial;
 background:var(--bg);color:var(--text);
}
.header{
 text-align:center;padding:18px;
 font-size:24px;font-weight:bold;color:#ff4d6d;
}
.theme-btn{
 position:fixed;top:10px;right:10px;
 padding:8px 14px;border:none;border-radius:20px;
 background:var(--btn);color:#fff;cursor:pointer;
}
.categories{
 display:flex;flex-wrap:wrap;justify-content:center;
 gap:8px;margin:12px;
}
.categories button{
 padding:7px 14px;border:none;border-radius:18px;
 background:#ccc;font-weight:bold;cursor:pointer;
}
.categories button.active{background:var(--btn);color:#fff}

.story-container{
 max-width:420px;height:75vh;margin:auto;
 background:var(--card);border-radius:22px;
 padding:18px;box-shadow:0 0 25px rgba(255,77,109,.5);
 display:flex;flex-direction:column;
 justify-content:center;align-items:center;
 text-align:center;position:relative;overflow:hidden;
}

.story-line{
 opacity:0;margin:7px 0;font-size:18px;
 animation:fade .8s forwards;
}
@keyframes fade{to{opacity:1}}

.progress{
 width:90%;height:5px;background:#ccc;
 border-radius:5px;overflow:hidden;margin-bottom:10px;
}
.progress-bar{
 height:100%;width:0;background:var(--btn);
 animation:load 8s linear forwards;
}
@keyframes load{to{width:100%}}

.dots{display:flex;gap:6px;margin-top:10px}
.dot{width:9px;height:9px;background:#bbb;border-radius:50%}
.dot.active{background:var(--btn)}

.actions{
 display:flex;gap:12px;margin-top:14px;
}
.actions button{
 padding:7px 15px;border:none;border-radius:20px;
 background:var(--btn);color:#fff;font-weight:bold;
 cursor:pointer;
}
.footer{text-align:center;padding:15px;color:#ff4d6d}
</style>
</head>

<body class="dark">

<div class="header">Gourav Yadav Story World ❤️</div>
<button class="theme-btn" onclick="toggleTheme()">🌙 Theme</button>

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
 </div>
</div>

<div class="footer">© 2026 Gourav Yadav</div>

<script>
const stories={
love:[
["उसकी मुस्कान","मेरी सबसे बड़ी दौलत है","हर दिन उससे","और प्यार हो जाता है",
"उसकी आवाज़","मेरे दिल को सुकून देती है","प्यार बस","उसे देखने से हो जाता है"],
["प्यार","शब्दों का मोहताज नहीं","यह तो","एक एहसास है",
"जो बिना कहे","दिल तक पहुँच जाता है"]
],
sad:[
["हम हँसते बहुत हैं","पर अंदर","सब बिखरा होता है",
"कुछ दर्द","कभी कहे नहीं जाते"],
["अधूरी कहानी","और अधूरी चाहत",
"बस याद बनकर","दिल में रह जाती है"]
],
horror:[
["रात के सन्नाटे में","किसी ने नाम लिया",
"पीछे देखा","कोई नहीं था",
"आईने में","कोई मुस्कुरा रहा था"],
["अंधेरे कमरे में","कदमों की आवाज़",
"पर मैं","अकेला था"]
],
motivation:[
["हार मत मानो","शुरुआत हमेशा कठिन होती है",
"एक दिन","यही मेहनत पहचान बनेगी"],
["जो आज दर्द देता है",
"वही कल","ताकत बनेगा"]
],
friendship:[
["दोस्ती","नाम नहीं एक एहसास है",
"जो हर मुश्किल में","साथ खड़ा हो"],
["सच्चा दोस्त","वही है",
"जो बिना कहे","समझ जाए"]
],
attitude:[
["हम चुप रहते हैं","क्योंकि शब्द कम हैं",
"जो समझे","वही अपना है"],
["मेरी खामोशी","मेरी पहचान है"]
],
life:[
["ज़िंदगी","सीखों का सफ़र है",
"हर दिन","कुछ सिखा जाता है"],
["जो मिला","उसी में खुश रहना",
"यही","ज़िंदगी है"]
]
};

let current="love",i=0;
const storyText=document.getElementById("storyText");
const dots=document.getElementById("dots");
const bar=document.getElementById("bar");

function loadStory(){
 storyText.innerHTML="";
 bar.style.animation="none";bar.offsetHeight;
 bar.style.animation="load 8s linear forwards";

 stories[current][i].forEach((l,idx)=>{
  let d=document.createElement("div");
  d.className="story-line";
  d.style.animationDelay=`${idx*0.5}s`;
  d.innerText=l;
  storyText.appendChild(d);
 });

 dots.innerHTML="";
 stories[current].forEach((_,x)=>{
  let dot=document.createElement("div");
  dot.className="dot"+(x===i?" active":"");
  dots.appendChild(dot);
 });
}

function changeCategory(c,b){
 current=c;i=0;
 document.querySelectorAll(".categories button").forEach(x=>x.classList.remove("active"));
 b.classList.add("active");
 loadStory();
}

function likeStory(){alert("❤️ Story Liked")}
function copyStory(){
 navigator.clipboard.writeText(stories[current][i].join("\n"));
 alert("📋 Story Copied");
}
function toggleTheme(){document.body.classList.toggle("dark")}

let sx=0;
storyBox.addEventListener("touchstart",e=>sx=e.touches[0].clientX);
storyBox.addEventListener("touchend",e=>{
 let d=sx-e.changedTouches[0].clientX;
 if(Math.abs(d)>30){
  i=d>0?(i+1)%stories[current].length:(i-1+stories[current].length)%stories[current].length;
  loadStory();
 }
});

loadStory();
</script>
</body>
</html>

