SHAYARI FOR GOURAVYADAV
<!-- SHAYARI SECTION -->
<div class="shayari-section">
<div class="categories">
  <button onclick="showCategory('love')">❤️ Love</button>
  <button onclick="showCategory('sad')">💔 Sad</button>
  <button onclick="showCategory('attitude')">😎 Attitude</button>
  <button onclick="showCategory('motivation')">🔥 Motivation</button>
</div>

<div class="shayari-section" id="shayariBox"></div>

 <style>
body{
  background:#0b0f1a;
  color:white;
  font-family: Arial, sans-serif;
}
.categories{
  text-align:center;
  margin:25px 0;
}
.categories button{
  margin:6px;
  padding:10px 20px;
  border:none;
  border-radius:25px;
  cursor:pointer;
  background:#ff4ecd;
  color:black;
  font-weight:bold;
}
.shayari-section{
  padding:20px;
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:25px;
}
.shayari-card{
  background:#0f1629;
  padding:22px;
  border-radius:18px;
  box-shadow:0 0 18px #ff4ecd;
}
.shayari-card p{
  line-height:1.9;
  font-size:15px;
  text-align:center;
}
.copy-btn{
  margin-top:15px;
  padding:8px 18px;
  border:none;
  border-radius:20px;
  background:#ff4ecd;
  cursor:pointer;
  font-weight:bold;
}
</style>
 <script>
const longShayari = {

love:[
`तुम मिले तो ऐसा लगा जैसे ज़िंदगी मुस्कुरा उठी,<br><br>
हर अधूरी ख्वाहिश को मानो नई वजह मिल गई।<br><br>
तुम्हारे साथ हर लम्हा खास लगता है,<br>
जैसे वक़्त भी हमें देखकर ठहर गया हो।`,

`इश्क़ सिर्फ़ पास होने का नाम नहीं होता,<br><br>
इश्क़ वो एहसास है जो दूर रहकर भी साथ रहता है।<br><br>
तुम मेरी ज़िंदगी की वो आदत हो,<br>
जिसे छोड़ना मेरे बस में नहीं।`
],

sad:[
`अकेले रहने का भी एक अलग सुकून होता है,<br><br>
ना किसी से उम्मीद, ना किसी से शिकायत।<br><br>
जो अपने थे वही सबसे ज़्यादा दर्द दे गए,<br>
और हम मुस्कुराते रह गए।`,

`हमने छोड़ना सीख लिया है अब,<br><br>
क्योंकि हर कोई साथ निभाने लायक नहीं होता।<br><br>
खामोशी भी अब अपना दर्द बयां करती है,<br>
जहां अल्फ़ाज़ थक जाते हैं।`
],

attitude:[
`हम खामोश ज़रूर रहते हैं,<br><br>
पर इसका मतलब ये नहीं कि हमें जवाब देना नहीं आता।<br><br>
वक़्त आने पर शब्द नहीं,<br>
हमारे काम बोलते हैं।`,

`हमारी पहचान हमारे उसूलों से है,<br><br>
ना कि लोगों की राय से।<br><br>
जो समझे वही अपना है,<br>
बाकी सब भीड़ है।`
],

motivation:[
`रास्ते मुश्किल ज़रूर होंगे,<br><br>
पर मंज़िलें उन्हीं को मिलती हैं जो चलते रहते हैं।<br><br>
आज की मेहनत ही कल की पहचान बनेगी,<br>
इसलिए कभी हार मत मानो।`,

`जो गिरकर भी उठना जानता है,<br><br>
वही इंसान असली विजेता होता है।<br><br>
आज दर्द सह लो चुपचाप,<br>
कल यही दर्द आपकी ताक़त बनेगा।`
]

};

function showCategory(type){
  const box = document.getElementById("shayariBox");
  box.innerHTML = "";
  longShayari[type].forEach(text=>{
    box.innerHTML += `
      <div class="shayari-card">
        <p>${text}</p>
        <button class="copy-btn" onclick="copyText(this)">Copy</button>
      </div>
    `;
  });
}

function copyText(btn){
  const text = btn.previousElementSibling.innerText;
  navigator.clipboard.writeText(text);
  btn.innerText = "Copied!";
  setTimeout(()=>btn.innerText="Copy",1500);
}

// default load
showCategory('love');
</script><section id="contact" style="max-width:900px;margin:40px auto 0;padding:25px;text-align:center;background:rgba(255,255,255,0.08);border-radius:20px;box-shadow:0 0 25px rgba(0,0,0,0.4);">
<h2 style="color:#00fff0;margin-bottom:10px;text-shadow:0 0 5px #00fff0;">📧 Contact Me</h2>
<p style="margin-bottom:10px;">अगर आप मुझसे सीधे संपर्क करना चाहते हैं तो नीचे क्लिक करें</p>
<a href="mailto:gouravy33o@gmail.com" style="display:inline-block;margin-top:10px;padding:10px 20px;border-radius:25px;background:#00fff0;color:#000;font-weight:600;text-decoration:none;box-shadow:0 0 15px #00fff0;">Send Email</a>
</section>
<footer>
© 2026 | Designed with ❤️ by Gourav Yadav
</footer>
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
<footer class="personal-footer">
  © 2026 | Designed with ❤️ by <span>Gourav Yadav</span>
</footer>

<style>
.personal-footer{
  text-align:center;
  padding:16px;
  margin-top:40px;
  background:rgba(0,0,0,0.45);
  font-size:0.95rem;
  color:#ddd;
  box-shadow:0 0 20px rgba(0,255,255,0.25);
}
.personal-footer span{
  color:#00fff0;
  font-weight:600;
  text-shadow:0 0 6px #00fff0;
}
</style>
<h3 class="neon-name">Gourav Yadav</h3>

<style>
.neon-name{
  color:#00fff0;
  font-weight:700;
  letter-spacing:1px;
  text-align:center;
  text-shadow:
    0 0 5px #00fff0,
    0 0 10px #00fff0,
    0 0 20px #00e6d6,
    0 0 40px #00b3a4;
}
</style>
<footer>
  Designed with ❤️ by <span class="neon-name">Gourav Yadav</span>
</footer>


