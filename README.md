<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Moje Portfolio - Projekt</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            text-align: center;
        }
        .container {
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            background: white;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #333;
        }
        p {
            color: #666;
        }
        .screenshot {
            width: 100%;
            border-radius: 10px;
            margin: 20px 0;
        }
        .btn {
            display: inline-block;
            padding: 10px 20px;
            margin-top: 10px;
            text-decoration: none;
            background: #007BFF;
            color: white;
            border-radius: 5px;
        }
        .btn:hover {
            background: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Nazwa Twojego Projektu</h1>
        <p>Krótki opis projektu - co robi, jakie technologie wykorzystuje, dlaczego jest wyjątkowy.</p>
        <img src="screenshot.png" alt="Zrzut ekranu projektu" class="screenshot">
        <p>Więcej informacji oraz kod źródłowy znajdziesz tutaj:</p>
        <a href="https://github.com/twoj-repozytorium" class="btn" target="_blank">Zobacz na GitHub</a>
    </div>
</body>
</html>
