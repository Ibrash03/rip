# <!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Валентинка</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: pink;
        }
        .container {
            margin-top: 100px;
        }
        h1 {
            color: red;
        }
        .buttons {
            position: relative;
            display: inline-block;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            transition: 0.3s;
        }
        #yes {
            background-color: red;
            color: white;
        }
        #no {
            background-color: white;
            color: red;
            position: absolute;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1> Азиза скоро 14 февраля станешь моей валентинкой? ❤</h1>
        <div class="buttons">
            <button id="yes">Да</button>
            <button id="no">Нет</button>
        </div>
    </div>

    <script>
        let yesButton = document.getElementById("yes");
        let noButton = document.getElementById("no");

        noButton.addEventListener("mouseover", function () {
            let x = Math.random() * window.innerWidth * 0.8;
            let y = Math.random() * window.innerHeight * 0.8;
            noButton.style.left = x + "px";
            noButton.style.top = y + "px";
            
            // Увеличиваем кнопку "Да"
            let currentSize = parseFloat(window.getComputedStyle(yesButton).fontSize);
            yesButton.style.fontSize = (currentSize + 5) + "px";
            yesButton.style.padding = (parseFloat(yesButton.style.padding) + 5) + "px";
        });

        yesButton.addEventListener("click", function () {
            alert("Ура! ❤ Я знал, что ты согласишься!");
        });
    </script>

</body>
</html>
