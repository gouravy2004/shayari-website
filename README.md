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
</script>
<footer>
© 2026 | Designed with ❤️ by Gourav Yadav
</footer>



