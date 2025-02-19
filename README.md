<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>День Святого Валентина</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #ffe6f1;
            text-align: center;
            padding-top: 100px;
        }
        .btn {
            font-size: 24px;
            padding: 20px 40px;
            cursor: pointer;
            border: none;
            border-radius: 10px;
            margin: 20px;
            transition: background-color 0.3s;
        }
        .btn-yes {
            background-color: #ff66b2;
            color: white;
        }
        .btn-yes:hover {
            background-color: #ff3399;
        }
        .btn-no {
            background-color: #ff4d4d;
            color: white;
        }
        .btn-no:hover {
            background-color: #ff1a1a;
        }
        .heart {
            font-size: 100px;
            color: red;
            margin-top: 50px;
        }
    </style>
</head>
<body>
    <h1>Ты любишь меня?</h1>
    <button class="btn btn-yes">Да</button>
    <button class="btn btn-no" id="noBtn">Нет</button>
    <div class="heart">❤️</div>
    <script>
        const noBtn = document.getElementById('noBtn');
        document.addEventListener('mousemove', (event) => {
            const x = event.clientX;
            const y = event.clientY;
            noBtn.style.position = 'absolute';
            noBtn.style.left = (x + 20) + 'px';
            noBtn.style.top = (y + 20) + 'px';
        });
        document.querySelector('.btn-yes').addEventListener('click', () => {
            alert('Я тебя тоже люблю! ❤️');
        });
        noBtn.addEventListener('click', () => {
            alert('Почему так? Давай обнимемся!');
        });
    </script>
</body>
</html>
