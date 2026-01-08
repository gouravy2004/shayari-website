SHAYARI FOR GOURAVYADAV
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Long Shayari Website</title>

<style>
body{
    margin:0;
    font-family:Arial, sans-serif;
    background:#f2f4f8;
}

/* Header */
header{
    background:linear-gradient(135deg,#ff512f,#dd2476);
    color:#fff;
    text-align:center;
    padding:25px;
}

/* Filter Buttons */
.filters{
    text-align:center;
    margin:20px;
}
.filters button{
    border:none;
    padding:10px 18px;
    margin:5px;
    border-radius:25px;
    cursor:pointer;
    background:#fff;
    box-shadow:0 5px 15px rgba(0,0,0,0.15);
    font-weight:600;
    transition:0.3s;
}
.filters button:hover,
.filters button.active{
    background:#dd2476;
    color:#fff;
}

/* Grid */
.container{
    padding:20px;
    display:grid;
    grid-template-columns:repeat(6,1fr);
    gap:15px;
}

/* Responsive */
@media(max-width:1200px){
    .container{ grid-template-columns:repeat(3,1fr); }
}
@media(max-width:768px){
    .container{ grid-template-columns:repeat(2,1fr); }
}
@media(max-width:480px){
    .container{ grid-template-columns:1fr; }
}

/* Card */
.card{
    background:#fff;
    border-radius:14px;
    padding:15px;
    box-shadow:0 8px 20px rgba(0,0,0,0.1);
    transition:0.3s;
}
.card:hover{
    transform:translateY(-6px);
}

.card h3{
    margin-top:0;
    color:#dd2476;
    font-size:16px;
}

.shayari{
    font-size:14px;
    line-height:1.6;
    white-space:pre-line;
}
</style>
</head>

<body>

<header>
    <h1>🔥 Best Long Shayari 🔥</h1>
    <p>Category Filter System</p>
</header>

<!-- FILTER BUTTONS -->
<div class="filters">
    <button class="active" onclick="filterShayari('all', this)">All</button>
    <button onclick="filterShayari('love', this)">❤️ Love</button>
    <button onclick="filterShayari('sad', this)">😢 Sad</button>
    <button onclick="filterShayari('attitude', this)">😎 Attitude</button>
    <button onclick="filterShayari('life', this)">🌿 Life</button>
</div>

<!-- SHAYARI GRID -->
<div class="container">

<div class="card love">
<h3>❤️ Love</h3>
<div class="shayari">
तेरी मोहब्बत में खुद को खो दिया,
हर ख्वाब तेरे नाम कर दिया।
तू साथ हो तो डर नहीं लगता,
तेरे बिना सब अधूरा लगता।
तेरी हँसी ही मेरी पहचान,
तू ही मेरा सुकून, तू ही मेरी जान।
</div>
</div>

<div class="card sad">
<h3>😢 Sad</h3>
<div class="shayari">
हमने चाहा जिसे टूटकर,
उसी ने हमें तोड़ दिया।
खामोशी में रोते रहे,
और दर्द ने रिश्ता जोड़ लिया।
अब अकेलापन ही अपना है,
क्योंकि भरोसा सबने छोड़ दिया।
</div>
</div>

<div class="card attitude">
<h3>😎 Attitude</h3>
<div class="shayari">
हम अपनी शर्तों पर जीते हैं,
किसी के इशारों पर नहीं।
जो समझे हमें वही अपना,
बाकी दुनिया की परवाह नहीं।
हमारी खामोशी ही काफी है,
हम शोर मचाया नहीं करते।
</div>
</div>

<div class="card life">
<h3>🌿 Life</h3>
<div class="shayari">
ज़िंदगी ने बहुत कुछ सिखाया,
हर मोड़ पर खुद को आजमाया।
गिरकर उठना सीखा है मैंने,
मुश्किलों से रास्ता बनाया।
जो हार मान ले वो रुक जाए,
जो लड़ जाए वही आगे जाए।
</div>
</div>

<div class="card love">
<h3>❤️ Love</h3>
<div class="shayari">
तेरे नाम से शुरू होती है सुबह,
तेरे ख्यालों में ढलती है शाम।
तू साथ हो तो हर ग़म हल्का,
तेरे बिना सब लगे बेनाम।
तू ही मेरी हर दुआ,
तू ही मेरी पूरी कहानी।
</div>
</div>

<div class="card sad">
<h3>😢 Sad</h3>
<div class="shayari">
कभी अपने थे जो अजनबी बन गए,
हँसी के पीछे आँसू छुप गए।
वक़्त ने सब बदल दिया,
और हम खामोशी में ढल गए।
अब सवाल भी नहीं करते,
बस हालात से समझौता कर गए।
</div>
</div>

</div>

<!-- JAVASCRIPT -->
<script>
function filterShayari(category, btn){
    let cards = document.querySelectorAll('.card');
    let buttons = document.querySelectorAll('.filters button');

    buttons.forEach(b => b.classList.remove('active'));
    btn.classList.add('active');

    cards.forEach(card=>{
        if(category === 'all'){
            card.style.display = "block";
        }else{
            card.style.display = card.classList.contains(category) ? "block" : "none";
        }
    });
}
</script>

</body>
</html>
<button id="themeToggle">🌙 Dark Mode</button>


      






<footer>
© 2026 | Designed with ❤️ by Gourav Yadav
</footer>
