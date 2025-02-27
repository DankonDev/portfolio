<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
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
            background: transparent; /* Usuwa tło z ikonek */
        }
        .skill-item img.nodejs {
            width: 60px;
            height: 60px; /* Zwiększa szerokość i wysokość Node.js */
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
        <h1>Daniel Sitkiewicz</h1>
    </div>

    <div class="container">
        <h1>O mnie</h1>
        <p>Jestem twórcą gier i programistą z ponad 5-letnim stażem pracy na silniku Unity. Od początku koncentruję się na tworzeniu gier mobilnych i komputerowych, z sukcesem wydając projekty na różne platformy. W przeszłości współpracowałem w ramach zespołów projektowych, ale od niedawna podejmuję się pełnej odpowiedzialności za wszystkie etapy realizacji gier — od pomysłu, przez produkcję, aż po publikację. Ta droga pozwoliła mi poszerzyć moje umiejętności w wielu dziedzinach związanych z tworzeniem i wydawaniem gier. Regularnie korzystam z najnowszych technologii, w tym z narzędzi sztucznej inteligencji, by usprawniać procesy i tworzyć innowacyjne rozwiązania. Wciąż rozwijam swoje umiejętności, angażując się w nowe, ambitne projekty.</p>
    </div>
    
    <div class="container">
        <h1>Narzędzia i doświadczenie</h1>
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
                <img src="nodejs.png" alt="NodeJS" class="nodejs">
                <span>NodeJS</span>
            </div>
            <div class="skill-item">
                <img src="googleads.png" alt="Google Ads">
                <span>Google Ads</span>
            </div>
        </div>
    </div>
    
    <div class="container">
        <h1>Bouncy Escape</h1>
        <p>Bouncy Escape to dynamiczna gra platformowa 3D z trybem wieloosobowym.</p>
        <p><strong>Funkcje w grze:</strong></p>
        <ul>
            <li>Multiplayer z użyciem Unity Netcode</li>
            <li>Synchronizacja ze Steamworks (statystyki, achievementy i DLC)</li>
            <li>Synchronizacja z Discord Rich Presence</li>
            <li>Fizyka i synchronizacja objektów dynamicznych między klientami (np. piłka)</li>
            <li>Losowy generator poziomów</li>
            <li>System emoji umożliwiający graczom komunikację</li>
            <li>System tworzenia i zarządzania lobby</li>
        </ul>
        <img src="screenshot.png" alt="Zrzut ekranu projektu" class="screenshot">
        <a href="https://store.steampowered.com/app/3256880/Bouncy_Escape/" class="btn" target="_blank">Zobacz na Steam</a>
    </div>

    <div class="container">
        <h1>Projekty mobilne</h1>
        
        <div>
            <h3>Kill Apps Challenge</h3>
            <p>Gra stworzona na wzór popularnego trendu na aplikacji TikTok. Ponad 3450 pobrań.</p>
            <a href="https://play.google.com/store/apps/details?id=com.Dankon.KillAppsChallenge.KillApps.Challenge.Freegame&hl=pl" class="btn" target="_blank">Zobacz na Google Play</a>
        </div>
        
        <div>
            <h3>Idle Candy Clicker Tycoon</h3>
            <p>Gra typu idle, która pozwala graczowi zarządzać cukierkowym imperium. Ponad 2900 pobrań.</p>
            <a href="https://play.google.com/store/apps/details?id=com.Dankon.IdleCandyClicker.IdleClicker.CandyClicker.Clicker.IdleGame.Idle" class="btn" target="_blank">Zobacz na Google Play</a>
        </div>

        <div>
            <h3>Build Master: City Island</h3>
            <p>Gra, w której gracz może zarządzać budową wyspy i rozwijać swoje miasto. Ponad 130 pobrań.</p>
            <a href="https://play.google.com/store/apps/details?id=com.Dankon.BuildMasterCityIsland.BuildCity.CityBuilder.MasterBuilder" class="btn" target="_blank">Zobacz na Google Play</a>
        </div>
    </div>
</body>
</html>
