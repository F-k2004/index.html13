<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <itle>🎨 تولیدگر رنگ تصادفی</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #222;
      font-family: sans-serif;
      direction: rtl;
      color: #fff;
    }

    .box {
      background: rgba(255,255,255,0.1);
      padding: 30px;
      border-radius: 15px;
      text-align: center;
      width: 300px;
      backdrop-filter: blur(6px);
      box-shadow: 0 4px 20px rgba(0,0,0,0.4);
    }

    #colorBox {
      width: 100%;
      height: 120px;
      border-radius: 10px;
      margin-bottom: 15px;
      background: #444;
    }

    #colorCode {
      font-size: 20px;
      margin-bottom: 10px;
    }

    button {
      padding: 10px 20px;
      border: none;
      border-radius: 10px;
      background: #fff;
      color: #333;
      cursor: pointer;
      transition: 0.2s;
      font-size: 15px;
    }

    button:hover {
      background: #f1f1f1;
    }

    .copy {
      margin-top: 10px;
      background: #ffeb3b;
    }
  </style>
</head>
<body>

  <div class="box">
    <h2>🎨 تولید رنگ تصادفی</h2>

    <div id="colorBox"></div>
    <div id="colorCode">#000000</div>

    <button onclick="generateColor()">تولید رنگ 🔁</button>
    <button class="copy" onclick="copyColor()">کپی رنگ 📋</button>
  </div>

  <script>
    function generateColor() {
      let color = "#" + Math.floor(Math.random() * 16777215).toString(16);
      document.getElementById("colorBox").style.background = color;
      document.getElementById("colorCode").textContent = color.toUpperCase();
    }

    function copyColor() {
      const colorText = document.getElementById("colorCode").textContent;
      navigator.clipboard.writeText(colorText);
      alert("کپی شد: " + colorText);
    }

    generateColor(); // تولید رنگ اولیه
  </script>

</body>
</html>
