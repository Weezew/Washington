<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Природа штата Вашингтон</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Базовые стили */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #333;
            overflow-x: hidden;
            background: linear-gradient(135deg, #f0f4f8, #d9e2ec);
            user-select: none; /* Запрещаем выделение текста */
            -webkit-user-select: none; /* Для Safari */
            -moz-user-select: none; /* Для Firefox */
            -ms-user-select: none; /* Для Internet Explorer */
        }
        header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 20px 50px;
            background-color: #1d3557;
            color: #fff;
            position: fixed;
            width: 100%;
            z-index: 10;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        header h1 {
            font-size: 24px;
            font-weight: bold;
            font-family: 'Georgia', serif;
        }
        header nav a {
            color: #fff;
            margin-left: 20px;
            text-decoration: none;
            transition: color 0.3s;
        }
        header nav a:hover {
            color: #a8dadc;
        }

        .parallax-section {
            position: relative;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            text-align: center;
            background-image: url('https://puzzleit.ru/files/puzzles/231/230811/_original.jpg');
            background-size: cover;
            background-attachment: fixed;
            color: #fff;
            background-blend-mode: multiply;
            background-color: rgba(29, 53, 87, 0.7);
        }
        .parallax-section h2 {
            font-size: 48px;
            color: #f1faee;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.7);
            margin-bottom: 15px;
        }
        .parallax-section p {
            font-size: 20px;
            max-width: 600px;
            color: #a8dadc;
            text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.5);
        }
        .parallax-section .button {
            padding: 15px 30px;
            font-size: 18px;
            color: #fff;
            background-color: #457b9d; /* Неброский синий */
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: background 0.3s;
            margin-top: 20px;
        }
        .parallax-section .button:hover {
            background-color: #1d3557;
        }

        /* Основные секции */
        .section {
            padding: 100px 50px;
            text-align: center;
        }
        .section h2 {
            font-size: 36px;
            margin-bottom: 20px;
            color: #1d3557;
            font-family: 'Georgia', serif;
        }
        .section p {
            max-width: 700px;
            margin: 0 auto;
            line-height: 1.6;
            color: #333;
        }

        /* Карточки с иконками */
        .features {
            display: flex;
            justify-content: space-around;
            margin-top: 50px;
            flex-wrap: wrap;
        }
        .feature-card {
            background: rgba(255, 255, 255, 0.8);
            border-radius: 15px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            padding: 40px 20px;
            width: 250px;
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
            backdrop-filter: blur(5px);
            margin: 10px;
        }
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 24px rgba(0, 0, 0, 0.3);
        }
        .feature-card i {
            font-size: 40px;
            color: #457b9d;
            margin-bottom: 20px;
        }
        .feature-card h3 {
            font-size: 24px;
            margin-bottom: 10px;
            color: #1d3557;
        }

        /* Кнопка и модальное окно */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 20;
        }
        .modal-content {
            background: #f1faee;
            padding: 30px;
            border-radius: 10px;
            text-align: center;
            width: 80%;
            max-width: 500px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4);
        }
        .close-btn {
            background: #457b9d;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
            transition: background 0.3s;
        }
        .close-btn:hover {
            background: #1d3557;
        }

        /* Плавный скроллинг */
        html {
            scroll-behavior: smooth; /* Плавный скроллинг */
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <h1>Вашингтонская Природа</h1>
        <nav>
            <a href="#features">Особенности</a>
            <a href="#about">О нас</a>
            <a href="#contact">Контакты</a>
        </nav>
    </header>

    <!-- Параллакс-секция -->
    <section class="parallax-section">
        <h2>Добро пожаловать в природу</h2>
        <p>Откройте для себя удивительные ландшафты и удивительное биоразнообразие штата Вашингтон.</p>
        <button class="button" onclick="openModal()">Узнать больше</button>
    </section>

    <!-- Секция с иконками -->
    <section id="features" class="section">
        <h2>Особенности Штата Вашингтон</h2>
        <div class="features">
            <div class="feature-card">
                <i class="fas fa-mountain"></i>
                <h3>Горы</h3>
                <p>Высокие и величественные горы ждут исследователей.</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-water"></i>
                <h3>Озера</h3>
                <p>Чистые озера - идеальные места для отдыха.</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-tree"></i>
                <h3>Леса</h3>
                <p>Густые леса для пеших прогулок и приключений.</p>
            </div>
        </div>
    </section>

    <!-- Модальное окно -->
    <div class="modal" id="myModal">
        <div class="modal-content">
            <h2>Добро пожаловать в Вашингтон!</h2>
            <p>Вашингтон, штат, известный своей живописной природой, предлагает путешественникам удивительные природные ландшафты и разнообразие заповедников. В среднем штат Вашингтон посещает около 40 миллионов туристов ежегодно, из которых значительная часть выбирает природные достопримечательности.</p>
            <button class="close-btn" onclick="closeModal()">Закрыть</button>
        </div>
    </div>

    <script>
        function openModal() {
            document.getElementById('myModal').style.display = 'flex';
        }

        function closeModal() {
            document.getElementById('myModal').style.display = 'none';
        }

        // Закрытие модального окна при нажатии вне его
        window.onclick = function(event) {
            const modal = document.getElementById('myModal');
            if (event.target === modal) {
                modal.style.display = "none";
            }
        }
    </script>

</body>
</html>
