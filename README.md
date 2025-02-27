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
            background-color: #333;
            color: white;
            text-align: center;
        }
        .container {
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            background: #444;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
        }
        h1 {
            color: #f4f4f4;
        }
        p {
            color: #ddd;
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
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 10px;
            background: #555;
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
        }
        .skill-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            background: #666;
            padding: 10px;
            border-radius: 8px;
            box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.3);
        }
        .skill-item img {
            width: 50px;
            height: 50px;
        }
        .skill-item span {
            margin-top: 5px;
            font-size: 14px;
            color: #fff;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>O mnie</h1>
        <p>Jestem doświadczonym twórcą gier i programistą, który prowadził projekty od A do Z. Mam doświadczenie w programowaniu, marketingu i zarządzaniu projektami.</p>
    </div>
    
    <div class="container">
        <h1>Bouncy Escape</h1>
        <p>Bouncy Escape to dynamiczna gra platformowa 3D z trybem wieloosobowym. Oferuje różne tryby gry, personalizację postaci i intensywną rozgrywkę.</p>
        <img src="screenshot.png" alt="Zrzut ekranu projektu" class="screenshot">
        <p>Więcej informacji oraz kod źródłowy znajdziesz tutaj:</p>
        <a href="https://store.steampowered.com/app/3256880/Bouncy_Escape/" class="btn" target="_blank">Zobacz na Steam</a>
    </div>
    
    <div class="container">
        <h1>Narzędzia i doświadczenie</h1>
        <p>Pracowałem z wieloma technologiami i narzędziami:</p>
        <div class="skills-grid">
            <div class="skill-item">
                <img src="unity.png" alt="Unity Engine">
                <span>Unity Engine</span>
            </div>
            <div class="skill-item">
                <img src="firebase.png" alt="Firebase">
                <span>Firebase</span>
            </div>
            <div class="skill-item">
                <img src="vscode.png" alt="VS Code">
                <span>VS Code</span>
            </div>
            <div class="skill-item">
                <img src="nodejs.png" alt="NodeJS">
                <span>NodeJS</span>
            </div>
            <div class="skill-item">
                <img src="googleads.png" alt="Google Ads">
                <span>Google Ads</span>
            </div>
        </div>
    </div>
</body>
</html>
