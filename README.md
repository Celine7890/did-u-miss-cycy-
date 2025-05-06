# did-u-miss-cycy-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Did You Miss Cycy?</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-image: url('background.png');
      background-size: cover;
      background-position: center;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      color: white;
      text-align: center;
    }

    .container {
      background: rgba(0, 0, 0, 0.6);
      padding: 40px;
      border-radius: 20px;
    }

    button {
      margin: 10px;
      padding: 10px 20px;
      font-size: 18px;
      cursor: pointer;
      border: none;
      border-radius: 10px;
      transition: 0.3s ease;
    }

    #yes {
      background-color: #e74c3c;
      color: white;
    }

    #no {
      background-color: #2c3e50;
      color: white;
      position: relative;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1 id="question">Did you miss Cycy?</h1>
    <div class="buttons">
      <button id="yes">Yes</button>
      <button id="no">No</button>
    </div>
    <p id="response" style="display:none;">Aww, that’s cute. I missed you too.</p>
  </div>

  <script>
    document.getElementById('yes').onclick = function () {
      document.getElementById('response').style.display = 'block';
    };

    const noBtn = document.getElementById('no');
    noBtn.addEventListener('mouseover', () => {
      const container = document.querySelector('.container');
      const maxX = container.clientWidth - noBtn.offsetWidth;
      const maxY = container.clientHeight - noBtn.offsetHeight;
      const randX = Math.random() * maxX;
      const randY = Math.random() * maxY;
      noBtn.style.position = 'absolute';
      noBtn.style.left = `${randX}px`;
      noBtn.style.top = `${randY}px`;
    });
  </script>
</body>
</html>
