<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menu Game Belajar</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Selamat Datang di Game Belajar!</h1>
        <button onclick="startGame()">Mulai Game</button>
    </div>
    <script>
        function startGame() {
            window.location.href = 'question1.html';
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pertanyaan 1</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Pertanyaan 1</h1>
        <p>Berapa 2 + 2?</p>
        <button onclick="checkAnswer(4)">4</button>
        <button onclick="checkAnswer(5)">5</button>
        <button onclick="checkAnswer(6)">6</button>
        <button onclick="checkAnswer(7)">7</button>
    </div>
    <script>
        function checkAnswer(answer) {
            if (answer === 4) {
                sessionStorage.setItem('score', (parseInt(sessionStorage.getItem('score') || '0') + 1).toString());
            }
            window.location.href = 'question2.html';
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pertanyaan 2</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Pertanyaan 2</h1>
        <p>Berapa 5 - 3?</p>
        <button onclick="checkAnswer(2)">2</button>
        <button onclick="checkAnswer(3)">3</button>
        <button onclick="checkAnswer(4)">4</button>
        <button onclick="checkAnswer(5)">5</button>
    </div>
    <script>
        function checkAnswer(answer) {
            if (answer === 2) {
                sessionStorage.setItem('score', (parseInt(sessionStorage.getItem('score') || '0') + 1).toString());
            }
            window.location.href = 'question3.html';
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pertanyaan 3</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Pertanyaan 3</h1>
        <p>Berapa 6 x 2?</p>
        <button onclick="checkAnswer(10)">10</button>
        <button onclick="checkAnswer(12)">12</button>
        <button onclick="checkAnswer(14)">14</button>
        <button onclick="checkAnswer(16)">16</button>
    </div>
    <script>
        function checkAnswer(answer) {
            if (answer === 12) {
                sessionStorage.setItem('score', (parseInt(sessionStorage.getItem('score') || '0') + 1).toString());
            }
            window.location.href = 'results.html';
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hasil Akhir</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Hasil Akhir</h1>
        <p>Skor Anda: <span id="score"></span></p>
        <button onclick="restartGame()">Main Lagi</button>
        <div class="animation">
            <!-- Tambahkan animasi atau gambar di sini -->
            <img src="animation.gif" alt="Animasi" />
        </div>
    </div>
    <script>
        document.getElementById('score').innerText = sessionStorage.getItem('score') || '0';

        function restartGame() {
            sessionStorage.removeItem('score');
            window.location.href = 'index.html';
        }
    </script>
</body>
</html>
