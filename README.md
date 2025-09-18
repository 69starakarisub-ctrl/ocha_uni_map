<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>キャンパスマップ - 門表示</title>
  <style>
    body {
      font-family: 'Helvetica Neue', sans-serif;
      background-color: #fafafa;
      margin: 0;
      padding: 0;
    }

    header {
      background-color: #cccccc;
      color: rgb(201, 17, 146);
      padding: 20px;
      text-align: center;
    }

    main {
      padding: 20px;
      text-align: center;
    }

    #container {
      position: relative;
      display: inline-block;
      margin-top: 20px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
      border-radius: 8px;
      overflow: hidden;
      background-color: rgb(204, 36, 140);
    }

    #baseMap {
      display: block;
      width: 100%;
      height: auto;
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: auto;
      display: none;
      pointer-events: none;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      margin-top: 10px;
      background-color: #f73ec2;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    button:hover {
      background-color: #d43fac;
    }

    footer {
      text-align: center;
      margin-top: 40px;
      padding: 20px;
      color: #2e2e2e;
    }
  </style>
</head>
<body>

  <header>
    <h1><font face ="Century Gothic">お茶の水女子大学カスタムキャンパスマップ</font></h1>
    <p><font face ="Century Gothic">お茶の水女子大学の地図を用途別に表示できます。表示したい項目を選択してください。</font></p>
  </header>

  <main>
    <button onclick="toggleGate()"><font face ="Century Gothic">オストメイト</font></button>
    <button onclick="toggleAED()"><font face ="Century Gothic">スロープ</font></button>
    <button onclick="toggleElevator()"><font face ="Century Gothic">エレベーター</font></button>
    <button onclick="toggleNursing()"><font face ="Century Gothic">段差</font></button>
    <button onclick="toggleRestArea()"><font face ="Century Gothic">点字ブロック</font></button>
    <button onclick="toggleSlope()"><font face ="Century Gothic">随時情報を追加</font></button>
    <div id="container">
      <img id="baseMap" src="白地図.jpg" alt="白地図">
      <img id="gateOverlay" class="overlay" src="osuto-removebg-preview.png" alt="門">
      <img id="aedOverlay" class="overlay" src="suro-removebg-preview.png" alt="AED">
      <img id="elevatorOverlay" class="overlay" src="EV2-removebg-preview.png" alt="エレベーター">
      <img id="nursingOverlay" class="overlay" src="dan-removebg-preview.png" alt="授乳室">
      <img id="restAreaOverlay" class="overlay" src="点字-removebg-preview.png" alt="展示ブロック">
      <img id="slopeOverlay" class="overlay" src="toilet.png" alt="情報追加も簡単に行えます!">
    </div>
  </main>

  <footer>
    <p><font face ="Century Gothic"> 2025年5月7日更新　Made by 生活科学部人間環境科学科　市川・濱田・松原・新野(2023年度入学世代)</font></p>
  </footer>

  <script>
    function toggleGate() {
      const gateOverlay = document.getElementById('gateOverlay');
      gateOverlay.style.display = (gateOverlay.style.display === 'none' || gateOverlay.style.display === '') ? 'block' : 'none';
    }

    function toggleAED() {
      const aedOverlay = document.getElementById('aedOverlay');
      aedOverlay.style.display = (aedOverlay.style.display === 'none' || aedOverlay.style.display === '') ? 'block' : 'none';
    }
  
function toggleSlope() {
  const overlay = document.getElementById('slopeOverlay');
  overlay.style.display = (overlay.style.display === 'none' || overlay.style.display === '') ? 'block' : 'none';
}

function toggleElevator() {
  const overlay = document.getElementById('elevatorOverlay');
  overlay.style.display = (overlay.style.display === 'none' || overlay.style.display === '') ? 'block' : 'none';
}

function toggleNursing() {
  const overlay = document.getElementById('nursingOverlay');
  overlay.style.display = (overlay.style.display === 'none' || overlay.style.display === '') ? 'block' : 'none';
}

function toggleRestArea() {
  const overlay = document.getElementById('restAreaOverlay');
  overlay.style.display = (overlay.style.display === 'none' || overlay.style.display === '') ? 'block' : 'none';
}

</script>
</body>
</html>
