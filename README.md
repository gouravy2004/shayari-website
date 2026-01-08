SHAYARI FOR GOURAVYADAV
<html lang="hi">
<head>
<meta charset="UTF-8">
<title>Gourav Shayari World</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
/* Like Button */
.like-btn{
  margin-top:5px;
  background:#ff69b4; /* Pink */
  color:#fff;
  border:none;
  padding:5px 12px;
  border-radius:20px;
  cursor:pointer;
  font-weight:bold;
  transition:0.3s;
}
.like-btn:hover{
  transform: scale(1.1);
}
.like-btn.liked{
  background:#ff1493; /* Dark Pink */
  color:#fff;
}

/* Theme variables */
:root {
  --bg-gradient-dark: linear-gradient(135deg,#330033,#660066,#990099); /* Dark Pink gradient */
  --bg-gradient-light: linear-gradient(135deg,#ffffff,#ffe6f0,#ffcce6); /* Light Pink gradient */
  --text-color-dark: #ffffff;
  --text-color-light: #000000;
  --column-bg-dark: rgba(255,255,255,0.1);
  --column-bg-light: rgba(255,20,147,0.05);
  --shayari-bg-dark: rgba(255,255,255,0.15);
  --shayari-bg-light: rgba(255,192,203,0.2);
}

/* Global styles */
body{
  margin:0;
  font-family:Segoe UI, sans-serif;
  background: var(--bg-gradient-dark);
  color: var(--text-color-dark);
  transition: 0.5s;
}
h1{
  text-align:center;
  padding:20px;
  color:#ff69b4; /* Pink */
}

.container{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:20px;
  padding:20px;
}

.column{
  background: var(--column-bg-dark);
  padding:15px;
  border-radius:15px;
  transition:0.5s;
}

.column h2{
  text-align:center;
  color:#ff69b4; /* Pink */
  border-bottom:1px solid rgba(255,255,255,0.2);
  padding-bottom:8px;
}

.shayari{
  background: var(--shayari-bg-dark);
  padding:12px;
  margin:12px 0;
  border-radius:12px;
  line-height:1.8;
  font-size:14px;
  transition:0.5s;
}

/* Copy Button */
.copy-btn{
  margin-top:8px;
  background:#ff69b4; /* Pink */
  border:none;
  padding:6px 12px;
  border-radius:20px;
  cursor:pointer;
  color:#fff;
}
.copy-btn:hover{
  background:#ff1493; /* Dark Pink */
}

/* Theme Toggle Button */
#themeToggle{
  padding:8px 20px;
  border-radius:20px;
  border:none;
  cursor:pointer;
  background:#ff69b4;
  color:#fff;
  font-weight:bold;
  box-shadow:0 0 10px #ff69b4;
  transition:0.3s;
}

/* Dark / Light theme toggle */
.light-theme{
  background: var(--bg-gradient-light) !important;
  color: var(--text-color-light) !important;
}
.light-theme .column{
  background: var(--column-bg-light) !important;
}
.light-theme .shayari{
  background: var(--shayari-bg-light) !important;
}
.light-theme .copy-btn{
  background:#ff69b4 !important;
  color:#fff !important;
}
.light-theme .like-btn{
  background:#ff69b4 !important;
  color:#fff !important;
}
</style>
</head>                                                                       
                                                                                                                                                      <body>
<h1>Shayari World</h1>
<div style="text-align:center; margin:15px;">
  <button id="themeToggle" onclick="toggleTheme()">🌙 Dark / Light Toggle</button>
</div>

<script>
function toggleTheme(){
  document.body.classList.toggle('light-theme');
}

// Like button functionality
const likeButtons = document.querySelectorAll('.like-btn');
likeButtons.forEach(btn => {
  btn.addEventListener('click', () => {
    const countSpan = btn.querySelector('.count');
    let count = countSpan ? parseInt(countSpan.textContent) : 0;
    if(countSpan) countSpan.textContent = count + 1;
    btn.style.background = '#ff1493'; // Dark Pink when liked
    btn.style.color = '#fff';
  });
});
</script>
</body>
</html>                                                                               
<body>/


<h1>✨ Gourav Shayari World ✨</h1>

<div class="container">

<!-- LOVE -->
<div class="column">
<h2>❤️ Love</h2>

<div class="shayari" id="l1">तुम्हारी एक मुस्कान<br>मेरे हर ग़म को भुला देती है,<br>तुम्हारी हर बात<br>दिल को सुकून दे जाती है,<br>तुम साथ हो तो<br>हर रास्ता आसान लगता है,<br>तुम्हें चाहना<br>मेरी सबसे खूबसूरत आदत है।</div>
<button class="copy-btn" onclick="copyText('l1')">Copy</button>

<div class="shayari" id="l2">मोहब्बत सिर्फ पास होने का नाम नहीं,<br>यह तो दिल से निभाने का नाम है,<br>तुम दूर रहकर भी मेरे हो,<br>यही प्यार की सबसे बड़ी पहचान है।</div>
<button class="copy-btn" onclick="copyText('l2')">Copy</button>

<div class="shayari" id="l3">तेरे बिना अधूरी सी लगती है दुनिया,<br>तेरे साथ हर खुशी पूरी लगती है,<br>तू मिल जाए बस एक बार,<br>यही दुआ रोज़ दिल से निकलती है।</div>
<button class="copy-btn" onclick="copyText('l3')">Copy</button>

<div class="shayari" id="l4">तुम्हें देख कर ही सुकून मिल जाता है,<br>दिल की हर बेचैनी थम जाती है,<br>यही तो मोहब्बत है,<br>जो बिना कहे सब समझ जाती है।</div>
<button class="copy-btn" onclick="copyText('l4')">Copy</button>

<div class="shayari" id="l5">प्यार वो नहीं जो दुनिया को दिखाया जाए,<br>प्यार वो है जो दिल में निभाया जाए,<br>तू मिले या न मिले,<br>तुझे हर हाल में चाहा जाए।</div>
<button class="copy-btn" onclick="copyText('l5')">Copy</button>

<div class="shayari" id="l6">तुम मेरे ख्वाबों की हकीकत हो,<br>मेरी हर दुआ की जरूरत हो,<br>तुम साथ रहो बस हमेशा,<br>यही मेरी सबसे बड़ी ख्वाहिश हो।</div>
<button class="copy-btn" onclick="copyText('l6')">Copy</button>

<div class="shayari" id="l7">दिल ने जब भी सुकून माँगा,<br>तेरा नाम सामने आया,<br>शायद यही इश्क़ है,<br>जो हर बार तुझ तक लाया।</div>
<button class="copy-btn" onclick="copyText('l7')">Copy</button>

<div class="shayari" id="l8">तेरे साथ बिताया हर पल,<br>मेरे लिए अनमोल है,<br>तू पास हो या दूर,<br>तू हमेशा दिल के करीब है।</div>
<button class="copy-btn" onclick="copyText('l8')">Copy</button>
</div>

<!-- ROMANTIC -->
<div class="column">
<h2>💕 Romantic</h2>

<div class="shayari" id="r1">तेरी बाहों में आकर,<br>हर डर खो जाता है,<br>तेरे होंठों की मुस्कान से,<br>दिल फिर से जीना सीख जाता है।</div>
<button class="copy-btn" onclick="copyText('r1')">Copy</button>

<div class="shayari" id="r2">तेरी हर सांस मेरी जरूरत बन गई,<br>तेरी हर नजर मेरी चाहत बन गई,<br>अब कुछ और नहीं चाहिए,<br>तू ही मेरी पूरी दुनिया बन गई।</div>
<button class="copy-btn" onclick="copyText('r2')">Copy</button>

<div class="shayari" id="r3">तेरे हाथों को थाम कर,<br>हर रास्ता आसान लगे,<br>तेरी आँखों में खो जाऊँ,<br>हर शाम खास लगे।</div>
<button class="copy-btn" onclick="copyText('r3')">Copy</button>

<div class="shayari" id="r4">तेरे बिना अधूरी सी है हर खुशी,<br>तेरे साथ हर पल हसीन है,<br>इश्क़ सिर्फ तुझसे है,<br>और रहेगा उम्र भर यकीन है।</div>
<button class="copy-btn" onclick="copyText('r4')">Copy</button>

<div class="shayari" id="r5">तेरी एक झलक से,<br>दिल बेकाबू हो जाता है,<br>पता नहीं ये इश्क़ है या जादू,<br>जो हर बार तुझ तक ले जाता है।</div>
<button class="copy-btn" onclick="copyText('r5')">Copy</button>

<div class="shayari" id="r6">तू पास हो तो,<br>हर मौसम सुहाना लगता है,<br>तेरे बिना तो,<br>हर लम्हा वीराना लगता है।</div>
<button class="copy-btn" onclick="copyText('r6')">Copy</button>

<div class="shayari" id="r7">तेरी हंसी मेरी कमजोरी है,<br>तेरी बातें मेरी मजबूरी हैं,<br>तू साथ रहे बस हमेशा,<br>यही मेरी जिंदगी की कहानी है।</div>
<button class="copy-btn" onclick="copyText('r7')">Copy</button>

<div class="shayari" id="r8">तेरे प्यार में इतना खो गए,<br>खुद को ही भूल बैठे,<br>अब तो बस तेरा नाम,<br>हर सांस के साथ लेते हैं।</div>
<button class="copy-btn" onclick="copyText('r8')">Copy</button>
</div>

<!-- LIFE / SAD / DEEP भी इसी structure में पूरे 8–8 shayari के साथ बन सकते हैं -->

</div>
</body>

<!-- LIFE -->
<div class="column">
<h2>🌿 Life</h2>

<div class="shayari" id="li1">
ज़िंदगी हर रोज़ नया इम्तिहान लेती है,<br>
कभी हँसाती है, कभी रुला देती है,<br>
जो हालात से लड़ना सीख ले,<br>
उसी को असली जीत मिलती है,<br>
हार मान लेना आसान होता है,<br>
पर खड़ा रहना ही जिंदगी है।
</div>
<button class="copy-btn" onclick="copyText('li1')">Copy</button>

<div class="shayari" id="li2">
ज़िंदगी किताब जैसी होती है,<br>
हर पन्ने पर नया सबक होता है,<br>
कुछ पन्ने खुशी के होते हैं,<br>
कुछ दर्द से भरे होते हैं,<br>
लेकिन पूरी किताब ही,<br>
इंसान को मजबूत बनाती है।
</div>
<button class="copy-btn" onclick="copyText('li2')">Copy</button>

<div class="shayari" id="li3">
वक़्त बदलता है, हालात बदलते हैं,<br>
आज जो अपने हैं, कल दूर हो जाते हैं,<br>
इसी का नाम जिंदगी है,<br>
जो हर दिन कुछ नया सिखा जाती है।
</div>
<button class="copy-btn" onclick="copyText('li3')">Copy</button>

<div class="shayari" id="li4">
ज़िंदगी आसान नहीं होती,<br>
पर जीने के तरीके होते हैं,<br>
जो मुस्कुरा कर सह ले,<br>
वही जिंदगी के असली खिलाड़ी होते हैं।
</div>
<button class="copy-btn" onclick="copyText('li4')">Copy</button>

<div class="shayari" id="li5">
हर दिन खुद से लड़ना पड़ता है,<br>
हर रात खुद को समझाना पड़ता है,<br>
तभी जाकर कहीं,<br>
ज़िंदगी आगे बढ़ पाती है।
</div>
<button class="copy-btn" onclick="copyText('li5')">Copy</button>

<div class="shayari" id="li6">
ज़िंदगी ने बहुत कुछ छीना है,<br>
पर बहुत कुछ सिखाया भी है,<br>
जो मिला उसी में खुश रहना,<br>
यही जिंदगी का हुनर सिखाया है।
</div>
<button class="copy-btn" onclick="copyText('li6')">Copy</button>

<div class="shayari" id="li7">
आज मुश्किल है, कल आसान होगा,<br>
हर अंधेरी रात के बाद सवेरा होगा,<br>
बस भरोसा रख खुद पर,<br>
तेरा भी वक्त आएगा।
</div>
<button class="copy-btn" onclick="copyText('li7')">Copy</button>

<div class="shayari" id="li8">
ज़िंदगी को समझने में ही,<br>
आधी उम्र निकल जाती है,<br>
बाकी उम्र बस,<br>
इसे जीने में निकल जाती है।
</div>
<button class="copy-btn" onclick="copyText('li8')">Copy</button>
</div>
<!-- SAD -->
<div class="column">
<h2>💔 Sad</h2>

<div class="shayari" id="s1">
खामोशी सबसे बड़ा दर्द है,<br>
जो बिना आवाज़ के सहा जाता है,<br>
जो मुस्कुराता हुआ दिखे,<br>
वही अंदर से सबसे ज्यादा टूटा होता है।
</div>
<button class="copy-btn" onclick="copyText('s1')">Copy</button>

<div class="shayari" id="s2">
जिसे अपना समझा था,<br>
वही सबसे ज्यादा दर्द दे गया,<br>
हम निभाते रहे रिश्ते,<br>
और वो हमें अकेला कर गया।
</div>
<button class="copy-btn" onclick="copyText('s2')">Copy</button>

<div class="shayari" id="s3">
आंसू तब निकलते हैं,<br>
जब शब्द खत्म हो जाते हैं,<br>
और दर्द तब बढ़ता है,<br>
जब अपने ही पराए बन जाते हैं।
</div>
<button class="copy-btn" onclick="copyText('s3')">Copy</button>

<div class="shayari" id="s4">
हमने चाहा बहुत शिद्दत से,<br>
पर किस्मत को कुछ और मंज़ूर था,<br>
दिल टूट गया हमारा,<br>
और वो बेखबर रहा।
</div>
<button class="copy-btn" onclick="copyText('s4')">Copy</button>

<div class="shayari" id="s5">
अकेले रहना सीख लिया है,<br>
अब किसी से उम्मीद नहीं रखते,<br>
दर्द बहुत दिया लोगों ने,<br>
अब किसी पर भरोसा नहीं करते।
</div>
<button class="copy-btn" onclick="copyText('s5')">Copy</button>

<div class="shayari" id="s6">
जिसे सबसे ज्यादा चाहा,<br>
उसी ने सबसे ज्यादा रुलाया,<br>
इश्क़ का यही सच है,<br>
जो मिला वही पराया।
</div>
<button class="copy-btn" onclick="copyText('s6')">Copy</button>

<div class="shayari" id="s7">
हम चुप रहे तो सब ठीक समझ बैठे,<br>
हम रोए नहीं तो मजबूत समझ बैठे,<br>
किसी ने ये नहीं पूछा,<br>
दिल पर क्या बीत रही है।
</div>
<button class="copy-btn" onclick="copyText('s7')">Copy</button>

<div class="shayari" id="s8">
दर्द लिखना मजबूरी बन गया,<br>
आंसू कागज़ पर उतर आए,<br>
जो कह न सके किसी से,<br>
वो शायरी बनकर बाहर आए।
</div>
<button class="copy-btn" onclick="copyText('s8')">Copy</button>
</div>
<!-- DEEP -->
<div class="column">
<h2>🖤 Deep</h2>

<div class="shayari" id="d1">
हर इंसान अच्छा नहीं होता,<br>
हर चेहरा सच्चा नहीं होता,<br>
इस दुनिया में भरोसा,<br>
सोच समझ कर करना पड़ता है।
</div>
<button class="copy-btn" onclick="copyText('d1')">Copy</button>

<div class="shayari" id="d2">
अकेलापन डराता नहीं,<br>
यह सिखाता है,<br>
कौन अपना है,<br>
और कौन सिर्फ मतलब का।
</div>
<button class="copy-btn" onclick="copyText('d2')">Copy</button>

<div class="shayari" id="d3">
खामोश रहना भी एक हुनर है,<br>
जो हर किसी के पास नहीं होता,<br>
कभी-कभी चुप रहना ही,<br>
सबसे बड़ा जवाब होता है।
</div>
<button class="copy-btn" onclick="copyText('d3')">Copy</button>

<div class="shayari" id="d4">
लोग बदलते नहीं,<br>
बस उनके असली चेहरे सामने आ जाते हैं,<br>
और हम समझ जाते हैं,<br>
कि भरोसा गलत जगह किया था।
</div>
<button class="copy-btn" onclick="copyText('d4')">Copy</button>

<div class="shayari" id="d5">
हर रिश्ता निभाया नहीं जाता,<br>
हर वादा पूरा नहीं होता,<br>
कुछ लोग जिंदगी में,<br>
सिर्फ सबक बनकर आते हैं।
</div>
<button class="copy-btn" onclick="copyText('d5')">Copy</button>

<div class="shayari" id="d6">
जितना कम बोलो,<br>
उतना ज्यादा समझ पाओगे,<br>
दुनिया शब्दों से नहीं,<br>
इरादों से पहचानी जाती है।
</div>
<button class="copy-btn" onclick="copyText('d6')">Copy</button>

<div class="shayari" id="d7">
खुद से लड़ना सबसे मुश्किल होता है,<br>
पर जो ये जीत ले,<br>
वही जिंदगी की हर जंग जीत लेता है।
</div>
<button class="copy-btn" onclick="copyText('d7')">Copy</button>

<div class="shayari" id="d8">
भीड़ में रहकर भी,<br>
अकेला महसूस करना,<br>
यही आज की दुनिया का,<br>
सबसे गहरा सच है।
</div>
<button class="copy-btn"


  <section id="contact" class="contact-box">
  <h2>📩 Contact Me</h2>

  <form action="mailto:gouravy330@gmail.com" method="post" enctype="text/plain">
    <input type="text" name="Name" gouravyadav="Your Name" required>

    <textarea name="Message" rows="5" placeholder="Your Message" required></textarea>

    <button type="submit">Send Message</button>
  </form>
</section>

<style>
.contact-box{
  max-width:500px;
  margin:40px auto;
  padding:25px;
  background:rgba(255,255,255,0.08);
  border-radius:20px;
  box-shadow:0 0 25px rgba(0,0,0,0.4);
  text-align:center;
}
.contact-box h2{
  color:#00fff0;
  margin-bottom:15px;
  text-shadow:0 0 6px #00fff0;
}
.contact-box input,
.contact-box textarea{
  width:100%;
  padding:12px;
  margin:10px 0;
  border:none;
  border-radius:12px;
  outline:none;
  font-size:1rem;
}
.contact-box button{
  margin-top:10px;
  padding:12px 30px;
  border:none;
  border-radius:25px;
  background:#00fff0;
  color:#000;
  font-weight:600;
  cursor:pointer;
  box-shadow:0 0 15px #00fff0;
  transition:0.3s;
}
.contact-box button:hover{
  box-shadow:0 0 30px #00fff0;
  transform: scale(1.05);
}
</style>
<div class="social-icons">
  <a href="https://instagram.com/yourusername" target="_blank" title="Instagram">
    <img src="https://cdn-icons-png.flaticon.com/512/2111/2111463.png" alt="Instagram">
  </a>

  <a href="mailto:yourgmail@gmail.com" title="Gmail">
    <img src="https://cdn-icons-png.flaticon.com/512/732/732200.png" alt="Gmail">
  </a>
</div>

<style>
@keyframes neonColor {
  0% { box-shadow: 0 0 10px #ff00ff, 0 0 20px #ff00ff; }
  25% { box-shadow: 0 0 10px #00fff0, 0 0 20px #00fff0; }
  50% { box-shadow: 0 0 10px #ffea00, 0 0 20px #ffea00; }
  75% { box-shadow: 0 0 10px #ff4d4d, 0 0 20px #ff4d4d; }
  100% { box-shadow: 0 0 10px #ff00ff, 0 0 20px #ff00ff; }
}

.social-icons{
  display:flex;
  justify-content:center;
  gap:18px;
  margin-top:12px;
}

.social-icons a{
  width:50px;
  height:50px;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
  background:rgba(255,255,255,0.05);
  animation: neonColor 4s infinite alternate;
  transition: transform 0.3s;
}

.social-icons a:hover{
  transform: scale(1.2) rotate(-5deg);
}

.social-icons img{
  width:24px;
  filter: brightness(1.2);
}
 <script>


<footer>
© 2026 | Designed with ❤️ by Gourav Yadav
</footer>
