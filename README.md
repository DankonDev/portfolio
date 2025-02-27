<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio - Daniel Sitkiewicz</title>
    <style>
        /* General styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #333;
            color: white;
            text-align: center;
            overflow-x: hidden;
        }

        .container {
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            background: #444;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }

        .container.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Animation classes for sliding and fading in */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .slide-in {
            opacity: 0;
            transform: translateX(-30px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }

        .slide-in.visible {
            opacity: 1;
            transform: translateX(0);
        }

        h1, h3 {
            color: #f4f4f4;
        }

        p, span {
            color: #ddd;
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

        /* Skills image size for NodeJS */
        .skill-item img.nodejs {
            width: 50px;
            height: 50px; /* Keeping size uniform */
        }

        /* Add styles for the language switcher */
        .lang-switcher {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #333;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="lang-switcher" onclick="toggleLanguage()">
        EN / PL
    </div>

    <div class="container fade-in" id="name-container">
        <h1 id="name">Daniel Sitkiewicz</h1>
    </div>

    <div class="container fade-in" id="about-container">
        <h1 id="about-title">O mnie</h1>
        <p id="about-text">Jestem twórcą gier i programistą z ponad 5-letnim stażem pracy na silniku Unity. Od początku koncentruję się na tworzeniu gier mobilnych i komputerowych, z sukcesem wydając projekty na różne platformy...</p>
    </div>

    <div class="container slide-in" id="skills-container">
        <h1 id="skills-title">Narzędzia i doświadczenie</h1>
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

    <div class="container fade-in" id="game-container">
        <h1 id="game-title">Bouncy Escape</h1>
        <p id="game-description">Bouncy Escape to dynamiczna gra platformowa 3D...</p>
        <a href="https://store.steampowered.com/app/3256880/Bouncy_Escape/" class="btn" target="_blank" id="steam-btn">Zobacz na Steam</a>
    </div>

    <div class="container fade-in" id="mobile-games-container">
        <h1 id="mobile-games-title">Projekty mobilne</h1>
        <div>
            <h3 id="kill-apps-title">Kill Apps Challenge</h3>
            <p id="kill-apps-desc">Gra stworzona na wzór popularnego trendu na aplikacji TikTok. Ponad 3450 pobrań.</p>
            <a href="https://play.google.com/store/apps/details?id=com.Dankon.KillAppsChallenge.KillApps.Challenge.Freegame&hl=pl" class="btn" target="_blank">Zobacz na Google Play</a>
        </div>

        <div>
            <h3 id="idle-candy-title">Idle Candy Clicker Tycoon</h3>
            <p id="idle-candy-desc">Gra typu idle, która pozwala graczowi zarządzać cukierkowym imperium. Ponad 2900 pobrań.</p>
            <a href="https://play.google.com/store/apps/details?id=com.Dankon.IdleCandyClicker.IdleClicker.CandyClicker.Clicker.IdleGame.Idle" class="btn" target="_blank">Zobacz na Google Play</a>
        </div>

        <div>
            <h3 id="build-master-title">Build Master: City Island</h3>
            <p id="build-master-desc">Gra, w której gracz może zarządzać budową wyspy i rozwijać swoje miasto. Ponad 130 pobrań.</p>
            <a href="https://play.google.com/store/apps/details?id=com.Dankon.BuildMasterCityIsland.BuildCity.CityBuilder.MasterBuilder" class="btn" target="_blank">Zobacz na Google Play</a>
        </div>
    </div>

    <script>
        // Toggle language function
        let isEnglish = false;

        function toggleLanguage() {
            isEnglish = !isEnglish;

            // Update text content based on the selected language
            document.getElementById('about-title').innerText = isEnglish ? 'About Me' : 'O mnie';
            document.getElementById('about-text').innerText = isEnglish ? 
                'I am a game developer and programmer with over 5 years of experience working on Unity Engine. From the start, I focused on creating mobile and computer games, successfully releasing projects on various platforms...' : 
                'Jestem twórcą gier i programistą z ponad 5-letnim stażem pracy na silniku Unity...';

            document.getElementById('skills-title').innerText = isEnglish ? 'Tools and Experience' : 'Narzędzia i doświadczenie';
            document.getElementById('game-title').innerText = isEnglish ? 'Bouncy Escape' : 'Bouncy Escape';
            document.getElementById('game-description').innerText = isEnglish ? 'Bouncy Escape is a dynamic 3D platform game...' : 'Bouncy Escape to dynamiczna gra platformowa 3D...';
            document.getElementById('steam-btn').innerText = isEnglish ? 'See on Steam' : 'Zobacz na Steam';

            document.getElementById('mobile-games-title').innerText = isEnglish ? 'Mobile Projects' : 'Projekty mobilne';

            document.getElementById('kill-apps-title').innerText = isEnglish ? 'Kill Apps Challenge' : 'Kill Apps Challenge';
            document.getElementById('kill-apps-desc').innerText = isEnglish ? 'A game created based on the popular TikTok trend. Over 3450 downloads.' : 'Gra stworzona na wzór popularnego trendu na aplikacji TikTok. Ponad 3450 pobrań.';

            document.getElementById('idle-candy-title').innerText = isEnglish ? 'Idle Candy Clicker Tycoon' : 'Idle Candy Clicker Tycoon';
            document.getElementById('idle-candy-desc').innerText = isEnglish ? 'An idle game where the player manages a candy empire. Over 2900 downloads.' : 'Gra typu idle, która pozwala graczowi zarządzać cukierkowym imperium. Ponad 2900 pobrań.';

            document.getElementById('build-master-title').innerText = isEnglish ? 'Build Master: City Island' : 'Build Master: City Island';
            document.getElementById('build-master-desc').innerText = isEnglish ? 'A game where the player manages the construction of an island and develops their city. Over 130 downloads.' : 'Gra, w której gracz może zarządzać budową wyspy i rozwijać swoje miasto. Ponad 130 pobrań.';
        }

        // Function to handle scroll animations
        const elementsToAnimate = document.querySelectorAll('.fade-in, .slide-in');

        // Function to check if elements are in view
        const isInViewport = (element) => {
            const rect = element.getBoundingClientRect();
            return rect.top >= 0 && rect.bottom <= window.innerHeight;
        };

        // Add or remove the 'visible' class on scroll
        const checkScrollAnimations = () => {
            elementsToAnimate.forEach(element => {
                if (isInViewport(element)) {
                    element.classList.add('visible');
                }
            });
        };

        // Check on page load and scroll
        window.addEventListener('scroll', checkScrollAnimations);
        window.addEventListener('load', checkScrollAnimations); // Ensure animations work on page load
    </script>
</body>
</html>
