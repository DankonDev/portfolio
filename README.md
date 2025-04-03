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
        .code-container {
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            background: #444; /* Ustawienie tła na kolor taki jak inne kontenery */
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
            opacity: 0;
            animation: slideIn 0.8s ease-out forwards;
            text-align: left;
            overflow-x: auto;
            font-family: 'Courier New', monospace;
            white-space: pre-wrap;
        }

        .code-container pre {
            margin: 0;
            text-align: left;
            background-color: #333;
            color: white;
        }
    </style>
</head>
<body>
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
        <a id="bouncy-steam-btn" href="https://store.steampowered.com/app/3256880/Bouncy_Escape/" class="btn" target="_blank">Zobacz na Steam</a>
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
            <div class="container code-container">
        <pre>
using System.Collections;
using System.Collections.Generic;
using Unity.Netcode;
using UnityEngine;
using TMPro;
using System;

public class CrossTheRoadSpawner : NetworkBehaviour
{
    [Header("Vehicle Settings")]
    public List&lt;GameObject&gt; vehicles;
    [Header("Spawn Points")]
    public Transform left1;
    public Transform left2;
    public Transform right1;
    public Transform right2;
    [Header("Spawn Config")]
    public GameObject PointsDetector;
    public float minSpawnTime = 1f;
    public float maxSpawnTime = 3f;
    public float vehicleSpeed = 3f;

    private Transform selectedSpawnPoint1;
    private Transform selectedSpawnPoint2;
    private Vector3 moveDirection1;
    private Vector3 moveDirection2;
    private float rotationY1;
    private float rotationY2;
    public int currentSeed;
    private System.Random random;
    private float nextSpawnTime;
    private float elapsedTime;
    private float lastSpawnTime = 0f;

    public override void OnNetworkSpawn()
    {
        base.OnNetworkSpawn();
        Debug.Log($"[OnNetworkSpawn] IsServer: {IsServer}, IsClient: {IsClient}");
    }

    void Start()
    {
        if (LobbyData.Instance.isConnected)
        {
            Debug.Log("[Start] Connected to Lobby, using Lobby Time.");
            random = new System.Random(currentSeed);
            SelectSpawnPoints();
            InitializeSpawnTimes();
            lastSpawnTime = CrossTheRoadGameplay.Instance.GetElapsedTime();
        }
        else
        {
            Debug.Log("[Start] Not connected to Lobby, using Time.time.");
            random = new System.Random(currentSeed);
            SelectSpawnPoints();
            InitializeSpawnTimes();
            lastSpawnTime = Time.time;
        }
        Debug.Log($"[Start] Initial lastSpawnTime: {lastSpawnTime}");
    }

    void InitializeSpawnTimes()
    {
        elapsedTime = 0f;
        nextSpawnTime = (float)random.NextDouble() * (maxSpawnTime - minSpawnTime) + minSpawnTime;
        Debug.Log($"[InitializeSpawnTimes] nextSpawnTime: {nextSpawnTime}");
    }

    void SelectSpawnPoints()
    {
        int choice = random.Next(0, 4);
        Debug.Log($"[SelectSpawnPoints] Choice: {choice}");

        switch (choice)
        {
            case 0:
                selectedSpawnPoint1 = left1;
                selectedSpawnPoint2 = left2;
                right1.gameObject.tag = "VehicleDestroyer";
                right2.gameObject.tag = "VehicleDestroyer";
                break;
            case 1:
                selectedSpawnPoint1 = right1;
                selectedSpawnPoint2 = right2;
                left1.gameObject.tag = "VehicleDestroyer";
                left2.gameObject.tag = "VehicleDestroyer";
                break;
            case 2:
                selectedSpawnPoint1 = left1;
                selectedSpawnPoint2 = right2;
                left2.gameObject.tag = "VehicleDestroyer";
                right1.gameObject.tag = "VehicleDestroyer";
                break;
            case 3:
                selectedSpawnPoint1 = right1;
                selectedSpawnPoint2 = left2;
                right2.gameObject.tag = "VehicleDestroyer";
                left1.gameObject.tag = "VehicleDestroyer";
                break;
        }

        moveDirection1 = (selectedSpawnPoint1 == left1 || selectedSpawnPoint1 == left2) ? Vector3.right : Vector3.left;
        moveDirection2 = (selectedSpawnPoint2 == left1 || selectedSpawnPoint2 == left2) ? Vector3.right : Vector3.left;
        rotationY1 = (moveDirection1 == Vector3.right) ? 90f : -90f;
        rotationY2 = (moveDirection2 == Vector3.right) ? 90f : -90f;

        Debug.Log($"[SelectSpawnPoints] selectedSpawnPoint1: {selectedSpawnPoint1.name}, moveDirection1: {moveDirection1}, rotationY1: {rotationY1}");
        Debug.Log($"[SelectSpawnPoints] selectedSpawnPoint2: {selectedSpawnPoint2.name}, moveDirection2: {moveDirection2}, rotationY2: {rotationY2}");

        if (LobbyData.Instance.isConnected && LobbyData.Instance.isHost)
        {
            Debug.Log("[SelectSpawnPoints] SPAWNPOINTS sent to client");
            UpdateSpawnPointsClientRpc(moveDirection1, moveDirection2, rotationY1, rotationY2, choice);
        }
    }

    void Update()
    {
        if (LobbyData.Instance.isConnected)
        {
            elapsedTime = CrossTheRoadGameplay.Instance.GetElapsedTime();
        }
        else
        {
            elapsedTime = Time.time;
        }

        if (elapsedTime - lastSpawnTime >= nextSpawnTime)
        {
            Debug.Log($"[Update] Time to spawn vehicle. elapsedTime: {elapsedTime}, lastSpawnTime: {lastSpawnTime}, nextSpawnTime: {nextSpawnTime}");
            SpawnVehicle();
            lastSpawnTime = elapsedTime;
            nextSpawnTime = (float)random.NextDouble() * (maxSpawnTime - minSpawnTime) + minSpawnTime;
            Debug.Log($"[Update] Next spawn time set to: {nextSpawnTime}");
        }
    }

    [ClientRpc]
    private void UpdateSpawnPointsClientRpc(Vector3 hostMoveDirection1, Vector3 hostMoveDirection2, float hostRotationY1, float hostRotationY2, int hostChoice)
    {
        Debug.Log("[UpdateSpawnPointsClientRpc] SPAWNPOINTS client received");
        Debug.Log($"[UpdateSpawnPointsClientRpc] hostChoice: {hostChoice}, hostMoveDirection1: {hostMoveDirection1}, hostMoveDirection2: {hostMoveDirection2}, hostRotationY1: {hostRotationY1}, hostRotationY2: {hostRotationY2}");

        switch (hostChoice)
        {
            case 0:
                selectedSpawnPoint1 = left1;
                selectedSpawnPoint2 = left2;
                right1.gameObject.tag = "VehicleDestroyer";
                right2.gameObject.tag = "VehicleDestroyer";
                break;
            case 1:
                selectedSpawnPoint1 = right1;
                selectedSpawnPoint2 = right2;
                left1.gameObject.tag = "VehicleDestroyer";
                left2.gameObject.tag = "VehicleDestroyer";
                break;
            case 2:
                selectedSpawnPoint1 = left1;
                selectedSpawnPoint2 = right2;
                left2.gameObject.tag = "VehicleDestroyer";
                right1.gameObject.tag = "VehicleDestroyer";
                break;
            case 3:
                selectedSpawnPoint1 = right1;
                selectedSpawnPoint2 = left2;
                right2.gameObject.tag = "VehicleDestroyer";
                left1.gameObject.tag = "VehicleDestroyer";
                break;
        }

        moveDirection1 = hostMoveDirection1;
        moveDirection2 = hostMoveDirection2;
        rotationY1 = hostRotationY1;
        rotationY2 = hostRotationY2;

        Debug.Log($"[UpdateSpawnPointsClientRpc] Client selectedSpawnPoint1: {selectedSpawnPoint1.name}, moveDirection1: {moveDirection1}, rotationY1: {rotationY1}");
        Debug.Log($"[UpdateSpawnPointsClientRpc] Client selectedSpawnPoint2: {selectedSpawnPoint2.name}, moveDirection2: {moveDirection2}, rotationY2: {rotationY2}");
    }

    void SpawnVehicle()
    {
        if (vehicles.Count > 0)
        {
            Transform spawnPoint = random.NextDouble() > 0.5f ? selectedSpawnPoint1 : selectedSpawnPoint2;
            Vector3 moveDirection = (spawnPoint == selectedSpawnPoint1) ? moveDirection1 : moveDirection2;
            float rotationY = (spawnPoint == selectedSpawnPoint1) ? rotationY1 : rotationY2;

            int vehicleId = random.Next(0, vehicles.Count);
            GameObject vehiclePrefab = vehicles[vehicleId];

            GameObject vehicle = Instantiate(vehiclePrefab, spawnPoint.position, Quaternion.Euler(0, rotationY, 0), transform);
            vehicle.transform.localScale = new Vector3(0.25f, 0.25f, 0.25f);
            vehicle.AddComponent&lt;VehicleMover&gt;().Initialize(moveDirection, vehicleSpeed);

            Debug.Log($"[SpawnVehicle] Spawned vehicle: {vehiclePrefab.name} at {spawnPoint.name} with direction {moveDirection} and rotation {rotationY}");
        }
        else
        {
            Debug.LogWarning("[SpawnVehicle] No vehicles available to spawn.");
        }
    }
}

public class VehicleMover : MonoBehaviour
{
    public Vector3 moveDirection;
    public float speed;

    public void Initialize(Vector3 direction, float moveSpeed)
    {
        moveDirection = direction;
        speed = moveSpeed;
        Debug.Log($"[VehicleMover] Initialized with direction: {moveDirection}, speed: {speed}");
    }

    void Update()
    {
        transform.position += moveDirection * speed * Time.deltaTime;
    }
}
        </pre>
    </div>

    <script>
        let language = 'pl';

        const translations = {
            pl: {
                name: "Daniel Sitkiewicz",
                aboutHeading: "O mnie",
                aboutText: "Jestem twórcą gier i programistą z ponad 5-letnim stażem pracy na silniku Unity. Od początku koncentruję się na tworzeniu gier mobilnych i komputerowych, z sukcesem wydając projekty na różne platformy. W przeszłości współpracowałem w ramach zespołów projektowych, ale od niedawna podejmuję się pełnej odpowiedzialności za wszystkie etapy realizacji gier - od pomysłu, przez produkcję, aż po publikację. Ta droga pozwoliła mi poszerzyć moje umiejętności w wielu dziedzinach związanych z tworzeniem i wydawaniem gier. Regularnie korzystam z najnowszych technologii, w tym z narzędzi sztucznej inteligencji, by usprawniać procesy i tworzyć innowacyjne rozwiązania. Wciąż rozwijam swoje umiejętności, angażując się w nowe, ambitne projekty.",
                toolsHeading: "Narzędzia i doświadczenie",
                bouncyHeading: "Bouncy Escape",
                bouncyDescription: "Bouncy Escape to dynamiczna gra platformowa 3D z trybem wieloosobowym.",
                bouncyFeaturesHeading: "Funkcje w grze",
                killAppsTitle: "Kill Apps Challenge",
                killAppsDesc: "Gra stworzona na wzór popularnego trendu na aplikacji TikTok. Ponad 3450 pobrań.",
                idleCandyTitle: "Idle Candy Clicker Tycoon",
                idleCandyDesc: "Gra typu idle, która pozwala graczowi zarządzać cukierkowym imperium. Ponad 2900 pobrań.",
                buildMasterTitle: "Build Master: City Island",
                buildMasterDesc: "Gra, w której gracz może zarządzać budową wyspy i rozwijać swoje miasto. Ponad 130 pobrań.",
                bouncyFeatures: [
                    "Multiplayer z użyciem Unity Netcode",
                    "Synchronizacja ze Steamworks (statystyki, achievementy i DLC)",
                    "Synchronizacja z Discord Rich Presence",
                    "Fizyka i synchronizacja objektów dynamicznych między klientami (np. piłka)",
                    "Losowy generator poziomów",
                    "System emoji umożliwiający graczom komunikację",
                    "System tworzenia i zarządzania lobby"
                ],
                bouncySteamBtn: "Zobacz na Steam",
                killAppsBtn: "Zobacz na Google Play",
                idleCandyBtn: "Zobacz na Google Play",
                buildMasterBtn: "Zobacz na Google Play",
                projectsHeading: "Projekty mobilne",
            },
            en: {
                name: "Daniel Sitkiewicz",
                aboutHeading: "About Me",
                aboutText: "I am a game developer and programmer with over 5 years of experience working with Unity engine. I have focused on mobile and computer game development from the start, successfully releasing projects on various platforms. In the past, I have collaborated within project teams, but recently I have taken full responsibility for all stages of game creation – from idea, through production, to publication. This path has allowed me to expand my skills in many areas related to game creation and publishing. I regularly use the latest technologies, including AI tools, to streamline processes and create innovative solutions. I am still developing my skills by engaging in new, ambitious projects.",
                toolsHeading: "Tools and Experience",
                bouncyHeading: "Bouncy Escape",
                bouncyDescription: "Bouncy Escape is a dynamic 3D platform game with a multiplayer mode.",
                bouncyFeaturesHeading: "Game Features",
                killAppsTitle: "Kill Apps Challenge",
                killAppsDesc: "A game inspired by the popular trend on TikTok. Over 3450 downloads.",
                idleCandyTitle: "Idle Candy Clicker Tycoon",
                idleCandyDesc: "An idle game where the player manages a candy empire. Over 2900 downloads..",
                buildMasterTitle: "Build Master: City Island",
                buildMasterDesc: "A game where the player can manage building an island and developing a city. Over 130 downloads.",
                bouncyFeatures: [
                    "Multiplayer using Unity Netcode",
                    "Synchronization with Steamworks (stats, achievements, and DLC)",
                    "Synchronization with Discord Rich Presence",
                    "Physics and synchronization of dynamic objects between clients (e.g., ball)",
                    "Random level generator",
                    "Emoji system allowing players to communicate",
                    "Lobby creation and management system"
                ],
                bouncySteamBtn: "View on Steam",
                killAppsBtn: "View on Google Play",
                idleCandyBtn: "View on Google Play",
                buildMasterBtn: "View on Google Play",
                projectsHeading: "Mobile Projects",
            }
        };

        function toggleLanguage() {
            language = (language === 'pl') ? 'en' : 'pl';
            document.getElementById("lang-switch-text").textContent = (language === 'pl') ? "PL" : "EN";
            applyTranslations();
        }

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
            document.getElementById("projects-heading").textContent = translations[language].projectsHeading;
            document.getElementById("bouncy-steam-btn").textContent = translations[language].bouncySteamBtn;

            document.querySelectorAll('.btn').forEach((btn) => {
                if (btn.parentElement.querySelector('h3') && btn.parentElement.querySelector('h3').textContent === "Build Master: City Island") {
                    btn.textContent = translations[language].buildMasterBtn;
                } else if (btn.parentElement.querySelector('h3') && btn.parentElement.querySelector('h3').textContent === "Idle Candy Clicker Tycoon") {
                    btn.textContent = translations[language].idleCandyBtn;
                } else if (btn.parentElement.querySelector('h3') && btn.parentElement.querySelector('h3').textContent === "Kill Apps Challenge") {
                    btn.textContent = translations[language].killAppsBtn;
                }
            });

            const bouncyFeaturesList = document.getElementById("bouncy-features");
            bouncyFeaturesList.innerHTML = '';
            translations[language].bouncyFeatures.forEach(feature => {
                const li = document.createElement("li");
                li.textContent = feature;
                bouncyFeaturesList.appendChild(li);
            });
        }

        window.onload = applyTranslations;
    </script>
</body>
</html>