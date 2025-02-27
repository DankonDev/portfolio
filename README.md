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
            overflow-x: hidden;
            animation: fadeIn 1s ease-in-out;
        }

        @keyframes fadeIn {
            0% {
                opacity: 0;
            }
            100% {
                opacity: 1;
            }
        }

        .container {
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            background: #444;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
            opacity: 0;
            animation: slideIn 0.8s ease-out forwards;
        }

        @keyframes slideIn {
            0% {
                transform: translateY(50px);
                opacity: 0;
            }
            100% {
                transform: translateY(0);
                opacity: 1;
            }
        }

        h1, h3, p {
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
            background: transparent;
        }

        .skill-item img.nodejs {
            width: 50px;
            height: 50px;
        }

        .skill-item span {
            margin-top: 5px;
            font-size: 14px;
            color: #fff;
        }

        /* Animacja przy przewijaniu */
        .animate-scroll {
            opacity: 0;
            transform: translateY(30px);
            animation: fadeUp 1s forwards;
        }

        @keyframes fadeUp {
            0% {
                opacity: 0;
                transform: translateY(30px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .projects-container {
            opacity: 1 !important;
            animation: fadeIn 1.5s ease-in-out !important;
        }

        /* Styl przełącznika języka */
        .language-switcher {
            position: fixed;
            top: 20px;
            right: 20px;
            background-color: #444;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            color: white;
        }

        .language-switcher:hover {
            background-color: #555;
        }

    </style>
</head>
<body>
    <!-- Przełącznik języka -->
    <div class="language-switcher" onclick="toggleLanguage()">
        <span id="lang-switch-text">PL</span>
    </div>

    <div class="container" id="container-name">
        <h1 id="name">Daniel Sitkiewicz</h1>
    </div>

    <div class="container animate-scroll" id="container-about">
        <h1 id="about-heading">O mnie</h1>
        <p id="about-text">Jestem twórcą gier i programistą z ponad 5-letnim stażem pracy na silniku Unity...</p>
    </div>
    
    <div class="container animate-scroll" id="container-tools">
        <h1 id="tools-heading">Narzędzia i doświadczenie</h1>
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
    
    <div class="container animate-scroll" id="container-bouncy">
        <h1 id="bouncy-heading">Bouncy Escape</h1>
        <p id="bouncy-description">Bouncy Escape to dynamiczna gra platformowa 3D z trybem wieloosobowym.</p>
        <p><strong id="bouncy-features-heading">Funkcje w grze:</strong></p>
        <ul id="bouncy-features">
            <li>Multiplayer z użyciem Unity Netcode</li>
            <li>Synchronizacja ze Steamworks (statystyki, achievementy i DLC)</li>
            <li>Synchronizacja z Discord Rich Presence</li>
            <li>Fizyka i synchronizacja objektów dynamicznych między klientami (np. piłka)</li>
            <li>Losowy generator poziomów</li>
            <li>System emoji umożliwiający graczom komunikację</li>
            <li>System tworzenia i zarządzania lobby</li>
        </ul>
        <img src="screenshot.png" alt="Zrzut ekranu projektu" class="screenshot">
    </div>

    <div class="container projects-container animate-scroll" id="container-projects">
        <h1 id="projects-heading">Projekty mobilne</h1>
        
        <div>
            <h3 id="kill-apps-title">Kill Apps Challenge</h3>
            <p id="kill-apps-desc">Gra stworzona na wzór popularnego trendu na aplikacji TikTok...</p>
            <a href="https://play.google.com/store/apps/details?id=com.Dankon.KillAppsChallenge.KillApps.Challenge.Freegame&hl=pl" class="btn" target="_blank">Zobacz na Google Play</a>
        </div>
        
        <div>
            <h3 id="idle-candy-title">Idle Candy Clicker Tycoon</h3>
            <p id="idle-candy-desc">Gra typu idle, która pozwala graczowi zarządzać cukierkowym imperium...</p>
            <a href="https://play.google.com/store/apps/details?id=com.Dankon.IdleCandyClicker.IdleClicker.CandyClicker.Clicker.IdleGame.Idle" class="btn" target="_blank">Zobacz na Google Play</a>
        </div>

        <div>
            <h3 id="build-master-title">Build Master: City Island</h3>
            <p id="build-master-desc">Gra, w której gracz może zarządzać budową wyspy i rozwijać swoje miasto...</p>
            <a id="build-master-btn" href="https://play.google.com/store/apps/details?id=com.Dankon.BuildMasterCityIsland.BuildCity.CityBuilder.MasterBuilder" class="btn" target="_blank">Zobacz na Google Play</a>
        </div>
    </div>

    <script>
        let language = 'pl'; // Domyślnie polski

        const translations = {
            pl: {
                name: "Daniel Sitkiewicz",
                aboutHeading: "O mnie",
                aboutText: "Jestem twórcą gier i programistą z ponad 5-letnim stażem pracy na silniku Unity...",
                toolsHeading: "Narzędzia i doświadczenie",
                bouncyHeading: "Bouncy Escape",
                bouncyDescription: "Bouncy Escape to dynamiczna gra platformowa 3D z trybem wieloosobowym.",
                bouncyFeaturesHeading: "Funkcje w grze",
                killAppsTitle: "Kill Apps Challenge",
                killAppsDesc: "Gra stworzona na wzór popularnego trendu na aplikacji TikTok...",
                idleCandyTitle: "Idle Candy Clicker Tycoon",
                idleCandyDesc: "Gra typu idle, która pozwala graczowi zarządzać cukierkowym imperium...",
                buildMasterTitle: "Build Master: City Island",
                buildMasterDesc: "Gra, w której gracz może zarządzać budową wyspy i rozwijać swoje miasto...",
                bouncyFeatures: [
                    "Multiplayer z użyciem Unity Netcode",
                    "Synchronizacja ze Steamworks (statystyki, achievementy i DLC)",
                    "Synchronizacja z Discord Rich Presence",
                    "Fizyka i synchronizacja objektów dynamicznych między klientami (np. piłka)",
                    "Losowy generator poziomów",
                    "System emoji umożliwiający graczom komunikację",
                    "System tworzenia i zarządzania lobby"
                ],
                killAppsBtn: "Zobacz na Google Play",
                idleCandyBtn: "Zobacz na Google Play",
                buildMasterBtn: "Zobacz na Google Play",
            },
            en: {
                name: "Daniel Sitkiewicz",
                aboutHeading: "About Me",
                aboutText: "I am a game developer and programmer with over 5 years of experience working with Unity engine...",
                toolsHeading: "Tools and Experience",
                bouncyHeading: "Bouncy Escape",
                bouncyDescription: "Bouncy Escape is a dynamic 3D platform game with a multiplayer mode.",
                bouncyFeaturesHeading: "Game Features",
                killAppsTitle: "Kill Apps Challenge",
                killAppsDesc: "A game inspired by the popular trend on TikTok...",
                idleCandyTitle: "Idle Candy Clicker Tycoon",
                idleCandyDesc: "An idle game where the player manages a candy empire...",
                buildMasterTitle: "Build Master: City Island",
                buildMasterDesc: "A game where the player can manage building an island and developing a city...",
                bouncyFeatures: [
                    "Multiplayer using Unity Netcode",
                    "Synchronization with Steamworks (stats, achievements, and DLC)",
                    "Synchronization with Discord Rich Presence",
                    "Physics and synchronization of dynamic objects between clients (e.g., ball)",
                    "Random level generator",
                    "Emoji system allowing players to communicate",
                    "Lobby creation and management system"
                ],
                killAppsBtn: "View on Google Play",
                idleCandyBtn: "View on Google Play",
                buildMasterBtn: "View on Google Play",
            }
        };

        // Funkcja zmieniająca język
        function toggleLanguage() {
            language = (language === 'pl') ? 'en' : 'pl'; // Zmieniamy język
            document.getElementById("lang-switch-text").textContent = (language === 'pl') ? "PL" : "EN"; // Zmiana tekstu przycisku
            applyTranslations();
        }

        // Funkcja stosująca tłumaczenia
        function applyTranslations() {
            document.getElementById("name").textContent = translations[language].name;
            document.getElementById("about-heading").textContent = translations[language].aboutHeading;
            document.getElementById("about-text").textContent = translations[language].aboutText;
            document.getElementById("tools-heading").textContent = translations[language].toolsHeading;
            document.getElementById("bouncy-heading").textContent = translations[language].bouncyHeading;
            document.getElementById("bouncy-description").textContent = translations[language].bouncyDescription;
            document.getElementById("bouncy-features-heading").textContent = translations[language].bouncyFeaturesHeading;
            document.getElementById("kill-apps-title").textContent = translations[language].killAppsTitle;
            document.getElementById("kill-apps-desc").textContent = translations[language].killAppsDesc;
            document.getElementById("idle-candy-title").textContent = translations[language].idleCandyTitle;
            document.getElementById("idle-candy-desc").textContent = translations[language].idleCandyDesc;
            document.getElementById("build-master-title").textContent = translations[language].buildMasterTitle;
            document.getElementById("build-master-desc").textContent = translations[language].buildMasterDesc;

            // Przyciski
            document.querySelectorAll('.btn').forEach((btn) => {
                if (btn.parentElement.querySelector('h3') && btn.parentElement.querySelector('h3').textContent === "Build Master: City Island") {
                    btn.textContent = translations[language].buildMasterBtn;
                }
                // Pozostałe przyciski
                else if(btn.textContent.includes('Zobacz na Google Play') && language === 'pl') {
                    btn.textContent = translations[language].killAppsBtn;
                }
            });
        }

        // Naładowanie tłumaczeń przy starcie
        window.onload = applyTranslations;
    </script>
</body>
</html>
