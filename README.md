<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Обезьяна Осыпь</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #000;
            color: #fff;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #1a1a1a;
            padding: 20px;
            text-align: center;
        }

        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px;
        }

        h1, h2 {
            color: #fff;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
        }

        .gallery-item {
            margin: 10px;
        }

        .gallery-item img {
            width: 100%;
            max-width: 300px;
            border-radius: 8px;
            transition: transform 0.3s ease;
            cursor: pointer;
        }

        .gallery-item img:hover {
            transform: scale(1.05);
        }

        footer {
            text-align: center;
            padding: 10px;
            background-color: #1a1a1a;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
        }

        .modal-content {
            margin: auto;
            display: block;
            max-width: 90%;
            max-height: 90%;
        }

        .close {
            position: absolute;
            top: 20px;
            right: 35px;
            color: #fff;
            font-size: 40px;
            cursor: pointer;
        }
    </style>
</head>
<body>

<header>
    <h1>Обезьяна Осыпь: Загадочная Болезнь</h1>
</header>

<div class="container">
    <h2>Введение</h2>
    <p>Обезьяна осыпь — это редкая и загадочная болезнь, которая поражает как людей, так и обезьян.</p>

    <h2>Галерея Исследований</h2>
    <div class="gallery">
        <div class="gallery-item">
            <img src="images/rost.png" alt="Рост высыпаний на коже" onclick="openModal(this)">
        </div>
        <div class="gallery-item">
            <img src="images/tolstaya.png" alt="Толстая обезьяна с симптомами" onclick="openModal(this)">
        </div>
        <!-- Добавь другие изображения -->
    </div>
</div>

<footer>
    <p>&copy; 2024 Обезьяна Осыпь. Все права защищены.</p>
</footer>

<div id="modal" class="modal">
    <span class="close" onclick="closeModal()">&times;</span>
    <img class="modal-content" id="modalImage">
</div>

<script>
    function openModal(img) {
        const modal = document.getElementById("modal");
        const modalImg = document.getElementById("modalImage");
        modal.style.display = "block";
        modalImg.src = img.src;
    }

    function closeModal() {
        const modal = document.getElementById("modal");
        modal.style.display = "none";
    }

    window.onclick = function(event) {
        const modal = document.getElementById("modal");
        if (event.target == modal) {
            modal.style.display = "none";
        }
    }
</script>

</body>
</html>
