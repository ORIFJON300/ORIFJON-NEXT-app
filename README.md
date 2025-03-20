<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Ekran Buzildi 😈</title>
  <style>
    html, body {
      margin: 0;
      padding: 0;
      overflow: hidden;
      background-color: black;
    }

    #crack {
      position: absolute;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background: url('https://i.ibb.co/4WqvdyN/cracked-screen.png') no-repeat center center;
      background-size: cover;
      z-index: 10;
    }

    #exit-btn {
      position: absolute;
      top: 10px;
      right: 10px;
      width: 50px;
      height: 50px;
      background: rgba(255, 0, 0, 0.0); /* ko'rinmas */
      border: none;
      z-index: 20;
    }

    /* Optional: Fake touch lock */
    #blocker {
      position: absolute;
      width: 100vw;
      height: 100vh;
      z-index: 15;
    }

    h1 {
      color: white;
      text-align: center;
      font-size: 24px;
      margin-top: 20px;
    }
  </style>
</head>
<body>

  <div id="crack"></div>

  <!-- Bu tugma faqat bilgan odam bosadi va app "yopiladi" -->
  <button id="exit-btn"></button>

  <!-- Bu blok hamma narsani bloklaydi -->
  <div id="blocker"></div>

  <h1>Ekran ishlamayapti! Qurilmani servisga olib boring 😈</h1>

  <script>
    const exitBtn = document.getElementById('exit-btn');
    const blocker = document.getElementById('blocker');

    exitBtn.addEventListener('click', () => {
      document.getElementById('crack').style.display = 'none';
      blocker.style.display = 'none';
      document.querySelector('h1').innerText = 'Prank tugadi! 😊';
    });

    // Prank yanada ishonarli bo'lishi uchun sensorni bloklab qo'yamiz
    blocker.addEventListener('click', (e) => {
      e.preventDefault();
    });
  </script>

</body>
</html>
