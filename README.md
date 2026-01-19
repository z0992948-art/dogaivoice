<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<title>AI Dog Website</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body{ font-family: Arial; background:#f2f2f2; text-align:center; padding-top:80px;}
.box{background:white; width:90%; max-width:400px; margin:auto; padding:25px; border-radius:10px; box-shadow:0 0 10px rgba(0,0,0,0.1);}
input{width:100%; padding:12px; font-size:18px;}
button{width:100%; padding:12px; margin-top:15px; font-size:18px; cursor:pointer;}
img{margin-top:20px; width:100%; border-radius:10px; display:none;}
.watermark{position: fixed; top:50%; left:50%; transform: translate(-50%,-50%) rotate(-30deg); font-size:50px; color: rgba(0,0,0,0.08); pointer-events:none; user-select:none; z-index:9999; white-space:nowrap;}
</style>
</head>
<body>

<div class="box">
  <h2>আপনার নাম লিখুন</h2>
  <input type="text" id="name" placeholder="আপনার নাম">
  <button onclick="showDog()">Submit</button>
  <p id="msg"></p>
  <img id="dog" src="https://images.dog.ceo/breeds/labrador/n02099712_5644.jpg">
</div>

<div class="watermark">Zihad Hasan</div>

<script>
function showDog(){
  const name = document.getElementById("name").value;
  const dog = document.getElementById("dog");
  const msg = document.getElementById("msg");
  if(name.trim()===""){ alert("দয়া করে নাম লিখুন"); return; }
  msg.innerHTML = "হ্যালো " + name + " 🐶";
  dog.style.display = "block";
}
</script>

</body>
</html>
