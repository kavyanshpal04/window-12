# window-12 code 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KPos 12</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', sans-serif;
        }

        body {
            overflow: hidden;
            background-color: #000;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .desktop {
        /* Desktop */
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
            box-shadow: 0 5px 20px rgb(92 0 255);

            background-size: cover;
            background-position: center;
            position: relative;
            overflow: hidden;
        }

        /* Taskbar */
        .taskbar {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 48px;
            background-color: rgba(30, 30, 30, 0.8);
            backdrop-filter: blur(10px);
            display: flex;
            align-items: center;
            padding: 0 10px;
            z-index: 1000;
            user-select: none;
        }

        .start-button {
            width: 45px;
            height: 45px;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 20px;
            cursor: pointer;
            transition: background-color 0.3s;
            user-select: none;
            
        }

        .start-button:hover {
            background-color: rgba(255, 255, 255, 0.1);
            box-shadow: 0 5px 20px rgb(92 0 255);
            border-radius: 200px;

        }

        .search-bar {
            width: 300px;
    height: 32px;
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 5px;
    display: flex;
    align-items: center;
    padding: 0 10px;
    color: rgba(255, 255, 255, 0.7);
    margin-right: 10px;
    cursor: pointer;
    margin-left: 1%;
}
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', sans-serif;
    user-select: none;
        }

        .taskbar-icons {
            display: flex;
            align-items: center;
            margin-left: 10px;
        }

        .task-icon {
            width: 40px;
            height: 40px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            margin: 0 2px;
            font-size: 18px;
            color: white;
        }

        .task-icon:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }

        .task-icon.active {
            background-color: rgba(255, 255, 255, 0.2);
        }

        .system-tray {
            display: flex;
            align-items: center;
            margin-left: auto;
            color: white;
            height: 100%;
        }

        .tray-icon {
            padding: 0 5px;
            font-size: 14px;
            cursor: pointer;
        }

        .time-date {
            padding: 0 10px;
            font-size: 12px;
            text-align: center;
            cursor: pointer;
            
        }

        /* Start Menu */
        .start-menu {
            position: absolute;
            bottom: 48px;
            left: 0;
            width: 450px;
            height: 550px;
            background-color: rgba(30, 30, 30, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 8px 8px 0 0;
            display: none;
            flex-direction: column;
            z-index: 999;
            overflow: hidden;
            box-shadow: 0 -5px 20px rgba(0, 0, 0, 0.5);
            box-shadow: 0 5px 20px rgb(92 0 255);

        }

        .user-section {
            padding: 20px;
            display: flex;
            align-items: center;
            color: white;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .user-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: #0078d7;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 20px;
            color: white;
            margin-right: 15px;
            background-size: cover;
            background-position: center;
        }

        .user-info {
            flex-grow: 1;
        }

        .user-name {
            margin-bottom: 17px;
    font-weight: 600;
    font-size: 16px;
    margin-top: 8px;
        }

        .user-status {
            font-size: 12px;
            opacity: 0.8;
        }

        .apps-grid {
            flex-grow: 1;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            padding: 20px;
            overflow-y: auto;
        }

        .app-tile {
            height: 90px;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 4px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            cursor: pointer;
            transition: all 0.2s;
        }

        .app-tile:hover {
            background-color: rgba(255, 255, 255, 0.1);
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgb(92 0 255);

        }

        .app-icon {
            font-size: 24px;
            margin-bottom: 5px;
        }

        .app-name {
            font-size: 12px;
        }

        .power-options {
            height: 60px;
            display: flex;
            justify-content: flex-end;
            align-items: center;
            padding: 0 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .power-button {
            padding: 8px 15px;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            border-radius: 4px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .power-button:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }

        /* Window */
        .window {
            position: absolute;
            background-color: #1e1e1e;
            border-radius: 8px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            overflow: hidden;
            min-width: 400px;
            min-height: 300px;
            z-index: 100;
        }

        .window-header {
            height: 32px;
            background-color: #2d2d2d;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 5px 20px rgb(92 0 255);
            padding: 0 10px;
            color: white;
            font-size: 14px;
            cursor: move;
        }

        .window-title {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .window-controls {
            display: flex;
            box-shadow: 0 5px 20px rgb(92 0 255);
        }

        .window-control {
            width: 46px;
            height: 32px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            color: rgba(255, 255, 255, 0.7);
        }

        .window-control:hover {
            background-color: rgba(255, 255, 255, 0.1);
            box-shadow: 0 5px 20px rgb(92 0 255);
        }

        .close:hover {
            background-color: #e81123;
            color: white;
        }

        .window-content {
            flex-grow: 1;
            padding: 15px;
            overflow: auto;
            color: white;
            box-shadow: 0 5px 20px rgb(92 0 255);
        }

        /* Desktop Icons */
        .desktop-icons {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 48px;
            padding: 20px;
            display: grid;
            grid-template-columns: repeat(auto-fill, 80px);
            grid-auto-rows: 90px;
            gap: 10px;
            align-content: start;
        }

        .desktop-icon {
            width: 80px;
            height: 90px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: white;
            cursor: pointer;
            border-radius: 4px;
            transition: background-color 0.2s;
            user-select: none;
        }

        .desktop-icon:hover {
            background-color: rgba(255, 255, 255, 0.1);
            box-shadow: 0 5px 20px rgb(92 0 255);

        }

        .desktop-icon i {
            font-size: 32px;
            margin-bottom: 5px;        
        }

        .desktop-icon span {
            font-size: 12px;
            text-align: center;
        }

        /* Settings App */
        .settings-content {
            display: grid;
            grid-template-columns: 200px 1fr;
            gap: 20px;
            height: 100%;
        }

        .settings-nav {
            background-color: #252525;
            border-radius: 4px;
            padding: 15px 0;
        }

        .settings-nav-item {
            padding: 10px 15px;
            color: rgba(255, 255, 255, 0.7);
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .settings-nav-item.active {
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            border-left: 3px solid #0078d7;
        }

        .settings-nav-item:hover {
            background-color: rgba(255, 255, 255, 0.05);
        }

        .settings-panel {
            padding: 10px;
            overflow-y: auto;
            height: 403px;
        }

        .settings-section {
            margin-bottom: 25px;
        }

        .settings-section h3 {
            margin-bottom: 15px;
            color: white;
            font-weight: 600;
        }

        .setting-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 10px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .setting-info {
            flex-grow: 1;
        }

        .setting-title {
            color: white;
            font-size: 14px;
            margin-bottom: 3px;
        }

        .setting-desc {
            color: rgba(255, 255, 255, 0.6);
            font-size: 12px;
        }

        .setting-control {
            min-width: 100px;
            display: flex;
            justify-content: flex-end;
        }

        input[type="range"] {
            width: 150px;
        }

        input[type="text"], input[type="password"] {
            background-color: #2d2d2d;
            border: 1px solid #3d3d3d;
            border-radius: 4px;
            padding: 8px;
            color: white;
        }

        button {
            background-color: #0078d7;
            color: white;
            border: none;
            border-radius: 4px;
            padding: 8px 15px;
            cursor: pointer;
        }

        button:hover {
            background-color: #0066b4;
            box-shadow: 0 5px 20px rgb(92 0 255);

        }

        /* Notepad */
        .notepad-content {
            height: 100%;
            display: flex;
            flex-direction: column;
        }

        textarea {
            flex-grow: 1;
            background-color: #1e1e1e;
            border: none;
            color: white;
            resize: none;
            padding: 10px;
            border-radius: 4px;
            font-family: 'Consolas', monospace;

        }
        .notepad-actions {
            display: flex;
            justify-content: flex-end;
            gap: 10px;
            margin-top: 10px;
        }

        /* File Explorer */
        .file-explorer-content {
            height: 100%;
            display: flex;
            flex-direction: column;
        }

        .explorer-toolbar {
            display: flex;
            gap: 10px;
            padding: 10px 0;
        }

        .explorer-body {
            display: grid;
            grid-template-columns: 200px 1fr;
            gap: 10px;
            flex-grow: 1;
        }

        .explorer-sidebar {
            background-color: #252525;
            border-radius: 4px;
            padding: 10px;
        }

        .explorer-files {
            background-color: #252525;
            border-radius: 4px;
            padding: 10px;
            overflow-y: auto;
        }

        .file-item {
            display: flex;
            align-items: center;
            padding: 8px;
            gap: 10px;
            cursor: pointer;
            border-radius: 4px;
        }

        .file-item:hover {
            background-color: rgba(255, 255, 255, 0.05);
        }

        /* Camera App */
        .camera-content {
            display: flex;
            flex-direction: column;
            height: 100%;
            align-items: center;
            justify-content: center;
            gap: 20px;
        }

        #camera-preview {
            width: 320px;
            height: 240px;
            background-color: #000;
            border-radius: 4px;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #666;
        }

        /* Profile Picture Upload */
        .profile-picture-upload {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
            margin-top: 20px;
        }

        .profile-preview {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background-color: #0078d7;
            background-size: cover;
            background-position: center;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 40px;
        }

        /* Login Screen */
        .login-screen {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #000000;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 2000;
        }

        .login-container {
            width: 452px;
            padding: 47px;
            background-color: rgb(30 30 30 / 0%);
            border-radius: 8px;
            box-shadow: 0 5px 20px rgb(92 0 255);
            text-align: center;
        }

        .user-login {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background-color: #0078d7;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 32px;
            color: white;
            margin: 0 auto 20px;
            background-size: cover;
            background-position: center;
        }

        .login-input {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            background-color: rgba(255, 255, 255, 0.1);
            border: none;
            border-radius: 4px;
            color: white;
            text-align: center;
        }

        .login-button {
            width: 100%;
            padding: 12px;
            background-color: #0078d7;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        .login-button:hover {
            background-color: #0066b4;
        }

        .login-footer {
            margin-top: 20px;
            color: rgba(255, 255, 255, 0.6);
            font-size: 12px;
        }

        /* Battery indicator */
        .battery {
            display: flex;
            align-items: center;
            gap: 5px;

        }

        .battery-level {
            width: 30px;
            height: 11px;
            border: 1px solid rgba(255, 255, 255, 0.7);
            border-radius: 2px;
            position: relative;
        }

        .battery-level::after {
            content: '';
            position: absolute;
            top: 2px;
            left: 2px;
            width: 75%;
            height: 6px;
            background-color: hsl(0, 0%, 100%);
            border-radius: 1px;

        }

        .battery-percentage {
            font-size: 12px;
            
        }

        /* Game Windows */
        .game-content {
            display: flex;
            flex-direction: column;
            height: 100%;
            align-items: center;
            justify-content: center;
            gap: 20px;
            padding: 20px;
        }

        .game-container {
            width: 100%;
            height: 100%;
            background-color: #0c0c0c;
            border-radius: 8px;
            overflow: hidden;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
        }
                /* Context Menu */
                #context-menu {
            position: absolute;
            background: rgba(255, 255, 255, 0);
            border-radius: 5px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            display: none;
            z-index: 2000;
        }
                /* Context Menu */
                #context-menu {
            position: absolute;
            background: rgba(255, 255, 255, 0.842);
            border-radius: 5px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            display: none;
            z-index: 2000;
            box-shadow: 0 5px 20px rgb(92 0 255);
        }
        .context-menu-item,.context-menu-ittem {

            padding: 10px 40px;
            cursor: pointer;
            align-items: center;
            justify-content: center;
            font-size: 13px;
            
        }


        .context-menu-item:hover {
            background: rgba(0, 0, 0, 0.103);
            color: rgb(0, 0, 0);
            box-shadow: 0 5px 20px rgb(92 0 255);
        }

        h5{
            color: #673AB7;
            font-size: 50px;
            font-weight:bolder ;
            font-family: cursive;
        }
        .file{
            width: 100%;
            height: calc(100% - 4px);
            border: none;
        }

    </style>
</head>
<body>
    
    <div class="desktop" id="desktop">
        <div class="desktop-icons">
            <div class="desktop-icon" data-app="fileExplorer">
                <i class="fas fa-folder"></i>
                <span>File Explorer</span>
            </div>
            <div class="desktop-icon" data-app="notepad">
                <i class="fas fa-sticky-note"></i>
                <span>Notepad</span>
            </div>
            <div class="desktop-icon" data-app="camera">
                <i class="fas fa-camera"></i>
                <span>Camera</span>
            </div>
            <div class="desktop-icon" data-app="minecraft">
                <i class="fas fa-cube"></i>
                <span>Minecraft</span>
            </div>
            <div class="desktop-icon" data-app="settings">
                <i class="fas fa-cog"></i>
                <span>Settings</span>
            </div>
        </div>
        <div id="context-menu">
            <!-- Context Menu -->
        <div class="context-menu-item" onclick="pinToTaskbar()">view</div>
        <div class="context-menu-item" onclick="createShortcut()">shot by</div>
        <div class="context-menu-item" onclick="createShortcut()">refresh</div>
        <div class="context-menu-item" onclick="createShortcut()">paste</div>

        <div class="context-menu-item" onclick="createShortcut()">Create Shortcut</div>



    </div>
        <div class="taskbar">
            <div class="start-button" id="start-button">
                <img style="width: 90%; border-radius: 15px;" src="images.jpg">
                
            </div>
            <div class="search-bar">
                <i class="fas fa-search"></i> Search
            </div>
            <div class="taskbar-icons" id="taskbar-icons">
                <!-- App icons will be added here dynamically -->
            </div>
            
            <div class="system-tray">
                <i id="wifi" class="fas fa-wifi"></i>
                <div class="tray-icon"><i class="fas fa-bell"></i>
                            
                </div>
                <div class="battery">
                    <div class="battery-level"></div>
                    <div class="battery-percentage">100%</div>
                </div>
                <div class="time-date" id="time-date">
                    <div>3:45 PM</div>
                    <div>6/15/2023</div>
                </div>
            </div>
        </div>

        

        <div class="start-menu" id="start-menu">
            <div class="user-section">
                <div class="user-avatar" id="user-avatar">U</div>
                <div class="user-info">
                    <div class="user-name" id="user-name">User</div>
                    <div class="user-status">Administrator</div>
                </div>
            </div>
            <div class="apps-grid">
                <div class="app-tile" data-app="settings">
                    <div class="app-icon"><i class="fas fa-cog"></i></div>
                    <div class="app-name">Settings</div>
                </div>
                <div class="app-tile" data-app="fileExplorer">
                    <div class="app-icon"><i class="fas fa-folder"></i></div>
                    <div class="app-name">File Explorer</div>
                </div>
                <div class="app-tile" data-app="notepad">
                    <div class="app-icon"><i class="fas fa-sticky-note"></i></div>
                    <div class="app-name">Notepad</div>
                </div>
                <div class="app-tile" data-app="camera">
                    <div class="app-icon"><i class="fas fa-camera"></i></div>
                    <div class="app-name">Camera</div>
                </div>
                <div class="app-tile" data-app="minecraft">
                    <div class="app-icon"><i class="fas fa-cube"></i></div>
                    <div class="app-name">Minecraft</div>
                </div>
                <div class="app-tile" data-app="tictactoe">
                    <div class="app-icon"><i class="fas fa-times"></i></div>
                    <div class="app-name">Tic Tac Toe</div>
                </div>
                <div class="app-tile" data-app="snake">
                    <div class="app-icon"><i class="fas fa-worm"></i></div>
                    <div class="app-name">Snake Game</div>
                </div>
                <div class="app-tile" data-app="memory">
                    <div class="app-icon"><i class="fas fa-brain"></i></div>
                    <div class="app-name">Memory Game</div>
                </div>
                <div class="app-tile" data-app="bird">
                    <div class="app-icon"><i class="fas fa-dove"></i></div>
                    <div class="app-name">Flying Bird</div>
                </div>
                </div>
            <div class="power-options">
                <div class="power-button" id="power-button">
                    <i class="fas fa-power-off"></i> Power
                </div>
            </div>
        </div>
    </div>


    

    <div class="login-screen" id="login-screen">
        <div class="login-container">
            <div class="user-login" id="login-avatar">U</div>
            <div class="user-name" id="login-name">User</div>
            <input type="password" class="login-input" id="password-input" placeholder="Enter password">
            <button class="login-button" id="login-button">Enter</button>
            <div class="login-footer">
                KPos 12 Simulation • 2025
            </div>
        </div>
    </div>




    <script>
        // DOM Elements
        const desktop = document.getElementById('desktop');
        const startButton = document.getElementById('start-button');
        const startMenu = document.getElementById('start-menu');
        const powerButton = document.getElementById('power-button');
        const timeDate = document.getElementById('time-date');
        const loginScreen = document.getElementById('login-screen');
        const passwordInput = document.getElementById('password-input');
        const loginButton = document.getElementById('login-button');
        const userName = document.getElementById('user-name');
        const userAvatar = document.getElementById('user-avatar');
        const loginName = document.getElementById('login-name');
        const loginAvatar = document.getElementById('login-avatar');
        const taskbarIcons = document.getElementById('taskbar-icons');

        // App windows (will be created dynamically)
        let windows = {};
        let zIndex = 100;
        let dragOffset = { x: 0, y: 0 };

        // System state
        let systemState = {
            password: null,
            computerName: "Windows-PC",
            userName: "User",
            profilePicture: null,
            background: "default",
            brightness: 100,
            memory: {
                total: 16,
                used: 8.2
            },
            bits: 64,
            battery: 85,
            files: {
                documents: [
                    { name: "notes.txt", content: "Welcome to Windows 12 Notepad!\n\nThis is a sample note. You can edit this text and it will be saved to your documents.", type: "text" },
                    { name: "image.png", content: "", type: "image" }
                ]
            },
            openApps: [],
            loggedIn: false,
            desktopIcons: [
                { app: "fileExplorer", x: 20, y: 20 },
                { app: "notepad", x: 20, y: 120 },
                { app: "camera", x: 20, y: 220 },
                { app: "minecraft", x: 20, y: 320 },
                { app: "settings", x: 20, y: 420 }
            ]
        };

        // Initialize the OS
        function initOS() {
            // Load system state from localStorage
            const savedState = localStorage.getItem('os_state');
            if (savedState) {
                const parsedState = JSON.parse(savedState);
                systemState = {...systemState, ...parsedState};
                
                // Apply saved settings
                if (systemState.background && systemState.background !== "default") {
                    desktop.style.backgroundImage = `url(${systemState.background})`;
                }
                desktop.style.filter = `brightness(${systemState.brightness}%)`;
                
                userName.textContent = systemState.userName;
                loginName.textContent = systemState.userName;
                
                // Set profile pictures if available
                if (systemState.profilePicture) {
                    userAvatar.style.backgroundImage = `url(${systemState.profilePicture})`;
                    userAvatar.textContent = '';
                    loginAvatar.style.backgroundImage = `url(${systemState.profilePicture})`;
                    loginAvatar.textContent = '';
                } else {
                    userAvatar.textContent = systemState.userName.charAt(0);
                    loginAvatar.textContent = systemState.userName.charAt(0);
                }
                
                // Position desktop icons
                positionDesktopIcons();
                
                // Check login status
                if (systemState.loggedIn) {
                    loginScreen.style.display = 'none';
                    
                    // Restore open apps
                    if (systemState.openApps && systemState.openApps.length > 0) {
                        systemState.openApps.forEach(app => {
                            openApp(app, true);
                        });
                    }
                } else {
                    showLoginScreen();
                }
            } else {
                showLoginScreen();
                positionDesktopIcons();
            }

            // Update time and date
            updateDateTime();
            setInterval(updateDateTime, 60000);

            // Event listeners
            startButton.addEventListener('click', toggleStartMenu);
            powerButton.addEventListener('click', showPowerOptions);
            loginButton.addEventListener('click', login);

            // App click handlers
            document.querySelectorAll('[data-app]').forEach(element => {
                element.addEventListener('click', (e) => {
                    // Prevent event from bubbling to desktop (which would close start menu)
                    e.stopPropagation();
                    
                    const appName = element.getAttribute('data-app');
                    openApp(appName);
                    
                    // Only close start menu if clicked from start menu
                    if (element.closest('.start-menu')) {
                        startMenu.style.display = 'none';
                    }
                });
            });

            // Close start menu when clicking outside
            document.addEventListener('click', (e) => {
                if (!startMenu.contains(e.target) && !startButton.contains(e.target)) {
                    startMenu.style.display = 'none';
                }
            });
            
            // Save state before unload
            window.addEventListener('beforeunload', () => {
                saveSystemState();
            });
            
            // Make desktop icons draggable
            makeIconsDraggable();
        }

        // Position desktop icons based on saved positions
        function positionDesktopIcons() {
            const icons = document.querySelectorAll('.desktop-icon');
            icons.forEach(icon => {
                const app = icon.getAttribute('data-app');
                const savedPosition = systemState.desktopIcons.find(i => i.app === app);
                
                if (savedPosition) {
                    icon.style.position = 'absolute';
                    icon.style.left = `${savedPosition.x}px`;
                    icon.style.top = `${savedPosition.y}px`;
                }
            });
        }

        // Make desktop icons draggable
        function makeIconsDraggable() {
            const icons = document.querySelectorAll('.desktop-icon');
            
            icons.forEach(icon => {
                let isDragging = false;
                let offset = { x: 0, y: 0 };
                
                icon.addEventListener('mousedown', (e) => {
                    isDragging = true;
                    
                    // Bring to front
                    icons.forEach(i => i.style.zIndex = '1');
                    icon.style.zIndex = '10';
                    
                    // Calculate offset
                    const rect = icon.getBoundingClientRect();
                    offset.x = e.clientX - rect.left;
                    offset.y = e.clientY - rect.top;
                    
                    // Prevent text selection during drag
                    e.preventDefault();
                });
                
                document.addEventListener('mousemove', (e) => {
                    if (!isDragging) return;
                    
                    // Calculate new position
                    const x = e.clientX - offset.x;
                    const y = e.clientY - offset.y;
                    
                    // Apply new position
                    icon.style.left = `${x}px`;
                    icon.style.top = `${y}px`;
                });
                
                document.addEventListener('mouseup', () => {
                    if (!isDragging) return;
                    
                    isDragging = false;
                    
                    // Save new position
                    const app = icon.getAttribute('data-app');
                    const index = systemState.desktopIcons.findIndex(i => i.app === app);
                    
                    if (index !== -1) {
                        const rect = icon.getBoundingClientRect();
                        systemState.desktopIcons[index].x = rect.left;
                        systemState.desktopIcons[index].y = rect.top;
                        saveSystemState();
                    }
                });
            });
        }

        // Save system state to localStorage
        function saveSystemState() {
            // Update open apps list
            systemState.openApps = Object.keys(windows);
            localStorage.setItem('os_state', JSON.stringify(systemState));
        }

        // Update time and date display
        function updateDateTime() {
            const now = new Date();
            const time = now.toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' });
            const date = now.toLocaleDateString();
            timeDate.innerHTML = `<div>${time}</div><div>${date}</div>`;
        }

        // Toggle start menu
        function toggleStartMenu(e) {
            e.stopPropagation();
            if (startMenu.style.display === 'flex') {
                startMenu.style.display = 'none';
            } else {
                startMenu.style.display = 'flex';
            }
        }

        // Show power options
        function showPowerOptions() {
            if (confirm("Do you want to restart this simulation?")) {
                systemState.loggedIn = false;
                saveSystemState();
                location.reload();
            }
        }

        // Show login screen
        function showLoginScreen() {
            loginScreen.style.display = 'flex';
        }

        // Login function
        function login() {
            if (!systemState.password || passwordInput.value === systemState.password) {
                systemState.loggedIn = true;
                saveSystemState();
                loginScreen.style.display = 'none';
                passwordInput.value = '';
            } else {
                alert("Incorrect password");
            }
        }

        // Open an application
        function openApp(appName, fromRestore = false) {
            // Close if already open
            if (windows[appName]) {
                windows[appName].element.style.display = 'flex';
                bringToFront(windows[appName]);
                return;
            }

            // Create window
            const window = document.createElement('div');
            window.className = 'window';
            window.style.zIndex = zIndex++;
            
            // Set initial position if not restoring
            if (!fromRestore) {
                window.style.top = '50px';
                window.style.left = '50px';
            }
            
            // Window header
            const header = document.createElement('div');
            header.className = 'window-header';
            
            const title = document.createElement('div');
            title.className = 'window-title';
            
            const controls = document.createElement('div');
            controls.className = 'window-controls';
            
            const minimize = document.createElement('div');
            minimize.className = 'window-control minimize';
            minimize.innerHTML = '─';
            
            const maximize = document.createElement('div');
            maximize.className = 'window-control maximize';
            maximize.innerHTML = '□';
            
            const close = document.createElement('div');
            close.className = 'window-control close';
            close.innerHTML = '×';
            
            controls.appendChild(minimize);
            controls.appendChild(maximize);
            controls.appendChild(close);
            
            header.appendChild(title);
            header.appendChild(controls);
            
            // Window content
            const content = document.createElement('div');
            content.className = 'window-content';
            
            window.appendChild(header);
            window.appendChild(content);
            
            desktop.appendChild(window);
            
            // Store window reference
            windows[appName] = {
                element: window,
                header: header,
                content: content,
                title: title,
                minimized: false
            };
            
            // Add to taskbar
            addToTaskbar(appName);
            
            // Set app-specific content
            switch (appName) {
                case 'settings':
                    openSettings(content, title);
                    break;
                case 'notepad':
                    openNotepad(content, title);
                    break;
                case 'fileExplorer':
                    openFileExplorer(content, title);
                    break;
                case 'camera':
                    openCamera(content, title);
                    break;
                case 'minecraft':
                case 'tictactoe':
                case 'snake':
                case 'memory':
                case 'bird':
                    openGame(appName, content, title);
                    break;
            }
            
            // Window controls
            minimize.addEventListener('click', () => minimizeWindow(appName));
            maximize.addEventListener('click', () => maximizeWindow(appName));
            close.addEventListener('click', () => closeWindow(appName));
            
            // Make window draggable
            makeDraggable(window, header);
            
            // Bring to front on click
            window.addEventListener('mousedown', () => bringToFront(windows[appName]));
            
            // Save state
            if (!fromRestore) {
                saveSystemState();
            }
        }

        // Add app icon to taskbar
        function addToTaskbar(appName) {
            const appIcons = {
                'settings': '<i class="fas fa-cog"></i>',
                'fileExplorer': '<i class="fas fa-folder"></i>',
                'notepad': '<i class="fas fa-sticky-note"></i>',
                'camera': '<i class="fas fa-camera"></i>',
                'minecraft': '<i class="fas fa-cube"></i>',
                'tictactoe': '<i class="fas fa-times"></i>',
                'snake': '<i class="fas fa-worm"></i>',
                'memory': '<i class="fas fa-brain"></i>',
                'bird': '<i class="fas fa-dove"></i>'
            };
            
            const icon = document.createElement('div');
            icon.className = 'task-icon';
            icon.innerHTML = appIcons[appName] || '<i class="fas fa-window-restore"></i>';
            icon.setAttribute('data-app', appName);
            icon.addEventListener('click', () => {
                if (windows[appName].minimized) {
                    windows[appName].element.style.display = 'flex';
                    windows[appName].minimized = false;
                    icon.classList.add('active');
                } else {
                    bringToFront(windows[appName]);
                }
            });
            
            taskbarIcons.appendChild(icon);
        }

        // Make window draggable
        function makeDraggable(element, handle) {
            let pos1 = 0, pos2 = 0, pos3 = 0, pos4 = 0;
            
            handle.onmousedown = dragMouseDown;
            
            function dragMouseDown(e) {
                e.preventDefault();
                pos3 = e.clientX;
                pos4 = e.clientY;
                document.onmouseup = closeDragElement;
                document.onmousemove = elementDrag;
                bringToFront(windows[Object.keys(windows).find(key => windows[key].element === element)]);
            }
            
            function elementDrag(e) {
                e.preventDefault();
                pos1 = pos3 - e.clientX;
                pos2 = pos4 - e.clientY;
                pos3 = e.clientX;
                pos4 = e.clientY;
                element.style.top = (element.offsetTop - pos2) + "px";
                element.style.left = (element.offsetLeft - pos1) + "px";
            }
            
            function closeDragElement() {
                document.onmouseup = null;
                document.onmousemove = null;
            }
        }

        // Bring window to front
        function bringToFront(window) {
            window.element.style.zIndex = zIndex++;
            
            // Update taskbar icons
            document.querySelectorAll('.task-icon').forEach(icon => {
                icon.classList.remove('active');
            });
            
            const appName = Object.keys(windows).find(key => windows[key] === window);
            if (appName) {
                document.querySelector(`.task-icon[data-app="${appName}"]`).classList.add('active');
            }
        }

        // Minimize window
        function minimizeWindow(appName) {
            windows[appName].element.style.display = 'none';
            windows[appName].minimized = true;
            document.querySelector(`.task-icon[data-app="${appName}"]`).classList.remove('active');
            saveSystemState();
        }

        // Maximize window
        function maximizeWindow(appName) {
            const window = windows[appName].element;
            if (window.style.width === '100%') {
                window.style.width = '600px';
                window.style.height = '400px';
                window.style.top = '50px';
                window.style.left = '50px';
            } else {
                window.style.width = '100%';
                window.style.height = 'calc(100% - 48px)';
                window.style.top = '0';
                window.style.left = '0';
            }
        }

        // Close window
        function closeWindow(appName) {
            desktop.removeChild(windows[appName].element);
            const taskbarIcon = document.querySelector(`.task-icon[data-app="${appName}"]`);
            if (taskbarIcon) {
                taskbarIcons.removeChild(taskbarIcon);
            }
            delete windows[appName];
            saveSystemState();
        }

        // Open Settings app
        function openSettings(content, title) {
            title.innerHTML = '<i class="fas fa-cog"></i> Settings';
            
            const settingsHTML = `
                <div class="settings-content">
                    <div class="settings-nav">
                        <div class="settings-nav-item active" data-panel="personalization"><i class="fas fa-paint-brush"></i> Personalization</div>
                        <div class="settings-nav-item" data-panel="system"><i class="fas fa-desktop"></i> System</div>
                        <div class="settings-nav-item" data-panel="accounts"><i class="fas fa-user"></i> Accounts</div>
                        <div class="settings-nav-item" data-panel="privacy"><i class="fas fa-shield-alt"></i> Privacy & Security</div>
                    </div>
                    <div class="settings-panel">
                        <div class="settings-section" id="personalization">
                            <h3>Background</h3>
                            <div class="setting-item">
                                <div class="setting-info">
                                    <div class="setting-title">Background Image</div>
                                    <div class="setting-desc">Choose your favorite background</div>
                                </div>
                                <div class="setting-control">
                                    <input type="file" id="bg-upload" accept="image/*">
                                </div>
                            </div>
                            <div class="setting-item">
                                <div class="setting-info">
                                    <div class="setting-title">Brightness</div>
                                    <div class="setting-desc">Adjust background brightness</div>
                                </div>
                                <div class="setting-control">
                                    <input type="range" id="brightness-slider" min="0" max="100" value="${systemState.brightness}">
                                </div>
                            </div>
                        </div>
                        <div class="settings-section" id="system">
                            <h3>System Information</h3>
                            <div class="setting-item">
                                <div class="setting-info">
                                    <div class="setting-title">Computer Name</div>
                                    <div class="setting-desc">Change the name of this computer</div>
                                </div>
                                <div class="setting-control">
                                    <input type="text" id="computer-name" value="${systemState.computerName}">
                                    <button id="change-name">Change</button>
                                </div>
                            </div>
                            <div class="setting-item">
                                <div class="setting-info">
                                    <div class="setting-title">Memory</div>
                                    <div class="setting-desc">${systemState.memory.used} GB of ${systemState.memory.total} GB used</div>
                                </div>
                            </div>
                            <div class="setting-item">
                                <div class="setting-info">
                                    <div class="setting-title">System Type</div>
                                    <div class="setting-desc">${systemState.bits}-bit operating system</div>
                                </div>
                            </div>
                        </div>
                        <div class="settings-section" id="accounts">
                            <h3>Your Account</h3>
                            <div class="setting-item">
                                <div class="setting-info">
                                    <div class="setting-title">User Name</div>
                                    <div class="setting-desc">Change your display name</div>
                                </div>
                                <div class="setting-control">
                                    <input type="text" id="user-name-input" value="${systemState.userName}">
                                    <button id="change-username">Change</button>
                                </div>
                            </div>
                            <div class="setting-item">
                                <div class="setting-info">
                                    <div class="setting-title">Profile Picture</div>
                                    <div class="setting-desc">Set your profile picture</div>
                                </div>
                                <div class="setting-control">
                                    <input type="file" id="profile-picture-upload" accept="image/*">
                                </div>
                            </div>
                            <div class="profile-picture-upload">
                                <div class="profile-preview" id="profile-preview">${systemState.userName.charAt(0)}</div>
                                <div>Preview</div>
                            </div>
                            <div class="setting-item">
                                <div class="setting-info">
                                    <div class="setting-title">Password</div>
                                    <div class="setting-desc">Set or change your password</div>
                                </div>
                                <div class="setting-control">
                                    <input type="password" id="password-set" placeholder="New password">
                                    <button id="set-password">Set</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            `;
            
            content.innerHTML = settingsHTML;
            
            // Set profile preview if exists
            const profilePreview = content.querySelector('#profile-preview');
            if (systemState.profilePicture) {
                profilePreview.style.backgroundImage = `url(${systemState.profilePicture})`;
                profilePreview.textContent = '';
            }
            
            // Settings panel switching
            content.querySelectorAll('.settings-nav-item').forEach(item => {
                item.addEventListener('click', () => {
                    content.querySelectorAll('.settings-nav-item').forEach(i => i.classList.remove('active'));
                    item.classList.add('active');
                    // In a real implementation, you would switch the settings panel here
                });
            });
            
            // Background upload
            content.querySelector('#bg-upload').addEventListener('change', function(e) {
                const file = e.target.files[0];
                if (file) {
                    const reader = new FileReader();
                    reader.onload = function(event) {
                        desktop.style.backgroundImage = `url(${event.target.result})`;
                        systemState.background = event.target.result;
                        saveSystemState();
                    };
                    reader.readAsDataURL(file);
                }
            });
            
            // Brightness slider
            const brightnessSlider = content.querySelector('#brightness-slider');
            brightnessSlider.value = systemState.brightness;
            brightnessSlider.addEventListener('input', function() {
                systemState.brightness = this.value;
                desktop.style.filter = `brightness(${this.value}%)`;
                saveSystemState();
            });
            
            // Computer name change
            content.querySelector('#change-name').addEventListener('click', function() {
                const newName = content.querySelector('#computer-name').value;
                systemState.computerName = newName;
                saveSystemState();
                alert(`Computer name changed to ${newName}. Restart required for changes to take effect.`);
            });
            
            // Username change
            content.querySelector('#change-username').addEventListener('click', function() {
                const newName = content.querySelector('#user-name-input').value;
                systemState.userName = newName;
                userName.textContent = newName;
                loginName.textContent = newName;
                
                // Update profile preview if no picture set
                if (!systemState.profilePicture) {
                    userAvatar.textContent = newName.charAt(0);
                    loginAvatar.textContent = newName.charAt(0);
                    profilePreview.textContent = newName.charAt(0);
                }
                
                saveSystemState();
                alert('Username changed successfully.');
            });
            
            // Profile picture upload
            content.querySelector('#profile-picture-upload').addEventListener('change', function(e) {
                const file = e.target.files[0];
                if (file) {
                    const reader = new FileReader();
                    reader.onload = function(event) {
                        systemState.profilePicture = event.target.result;
                        
                        // Update all profile pictures
                        userAvatar.style.backgroundImage = `url(${event.target.result})`;
                        userAvatar.textContent = '';
                        loginAvatar.style.backgroundImage = `url(${event.target.result})`;
                        loginAvatar.textContent = '';
                        profilePreview.style.backgroundImage = `url(${event.target.result})`;
                        profilePreview.textContent = '';
                        
                        
                    };
                    reader.readAsDataURL(file);
                }
            });
            
            // Password set
            content.querySelector('#set-password').addEventListener('click', function() {
                const newPassword = content.querySelector('#password-set').value;
                systemState.password = newPassword;
                saveSystemState();
                alert('Password set successfully.');
            });
        }

        // Open Notepad app
        function openNotepad(content, title) {
            title.innerHTML = '<i class="fas fa-sticky-note"></i> Notepad';
            
            // Load saved note if exists
            let savedNote = "";
            const noteFile = systemState.files.documents.find(f => f.name === "notes.txt");
            if (noteFile) {
                savedNote = noteFile.content;
            }
            
            const notepadHTML = `
                <div class="notepad-content">
                    <textarea placeholder="Type your text here..." id="notepad-text">${savedNote}</textarea>
                    <div class="notepad-actions">
                        <button id="notepad-clear"><i class="fas fa-trash"></i> Clear</button>
                        <button id="notepad-save"><i class="fas fa-save"></i> Save</button>
                    </div>
                </div>
            `;
            
            content.innerHTML = notepadHTML;
            
            // Save functionality
            content.querySelector('#notepad-save').addEventListener('click', function() {
                const text = content.querySelector('#notepad-text').value;
                // Save to documents
                const noteIndex = systemState.files.documents.findIndex(f => f.name === "notes.txt");
                if (noteIndex !== -1) {
                    systemState.files.documents[noteIndex].content = text;
                } else {
                    systemState.files.documents.push({
                        name: "notes.txt",
                        content: text,
                        type: "text"
                    });
                }
                saveSystemState();
                alert('Note saved to Documents!');
            });
            
            // Clear functionality
            content.querySelector('#notepad-clear').addEventListener('click', function() {
                if (confirm('Are you sure you want to clear the notepad?')) {
                    content.querySelector('#notepad-text').value = '';
                }
            });
        }

        // Open File Explorer
        function openFileExplorer(content, title) {
            title.innerHTML = '<i class="fas fa-folder"></i> File Explorer';
            
            const explorerHTML = `
                <div class="file-explorer-content">
                    <div class="explorer-toolbar">
                        <button><i class="fas fa-folder-plus"></i> New Folder</button>
                        <button><i class="fas fa-copy"></i> Copy</button>
                        <button><i class="fas fa-clipboard"></i> Paste</button>
                    </div>
                    <div class="explorer-body">
                        <div class="explorer-sidebar">
                            <div class="file-item"><i class="fas fa-folder"></i> Documents</div>
                            <div class="file-item"><i class="fas fa-folder"></i> Pictures</div>
                            <div class="file-item"><i class="fas fa-folder"></i> Videos</div>
                            <div class="file-item"><i class="fas fa-folder"></i> Downloads</div>
                        </div>
                        <div class="explorer-files">
                            <h3>Documents</h3>
                            ${systemState.files.documents.map(file => `
                                <div class="file-item" data-file="${file.name}">
                                    ${file.type === 'text' ? '<i class="fas fa-file-alt"></i>' : '<i class="fas fa-file-image"></i>'} ${file.name}
                                </div>
                            `).join('')}
                        </div>
                    </div>
                </div>
            `;
            
            content.innerHTML = explorerHTML;
            
            // File click handlers
            content.querySelectorAll('.file-item').forEach(item => {
                item.addEventListener('click', function() {
                    const fileName = this.getAttribute('data-file');
                    if (fileName) {
                        const file = systemState.files.documents.find(f => f.name === fileName);
                        if (file) {
                            if (file.type === 'text') {
                                openApp('notepad');
                                // In a real implementation, you would load the file content
                            } else {
                                alert(`Opening ${file.name}`);
                            }
                        }
                    }
                });
            });
        }

        // Open Camera app
        function openCamera(content, title) {
            title.innerHTML = '<i class="fas fa-camera"></i> Camera';
            
            const cameraHTML = `
                <div class="camera-content">
                    <div id="camera-preview">
                        <i class="fas fa-camera" style="font-size: 48px;"></i>
                        <p>Camera feed would appear here</p>
                    </div>
                    <button id="capture-btn"><i class="fas fa-camera"></i> Take Photo</button>
                </div>
            `;
            
            content.innerHTML = cameraHTML;
            
            // Capture functionality
            content.querySelector('#capture-btn').addEventListener('click', function() {
                // Add to documents
                systemState.files.documents.push({
                    name: `photo-${new Date().getTime()}.png`,
                    content: "",
                    type: "image"
                });
                saveSystemState();
                alert('Photo taken and saved to Pictures!');
                // In a real implementation, this would capture from webcam and save
            });
        }

        // Open a game
        function openGame(gameName, content, title) {
            let gameTitle = '';
            let gameIcon = '';
            
            switch (gameName) {
                case 'minecraft': 
                    gameTitle = 'Minecraft';
                    gameIcon = '<i class="fas fa-cube"></i>';
                    break;
                case 'tictactoe': 
                    gameTitle = 'Tic Tac Toe';
                    gameIcon = '<i class="fas fa-times"></i>';
                    break;
                case 'snake': 
                    gameTitle = 'Snake Game';
                    gameIcon = '<i class="fas fa-worm"></i>';
                    break;
                case 'memory': 
                    gameTitle = 'Memory Game';
                    gameIcon = '<i class="fas fa-brain"></i>';
                    break;
                case 'bird': 
                    gameTitle = 'Flying Bird';
                    gameIcon = '<i class="fas fa-dove"></i>';
                    break;
            }
            title.innerHTML = `${gameIcon} ${gameTitle}`;
            
            let gameHTML = `
            <iframe class="file" src="indextex.html"></iframe>
            `;
            
            content.innerHTML = gameHTML;
            
            // Start game button
            const startBtn = content.querySelector('#start-game');
            if (startBtn) {
                startBtn.addEventListener('click', function() {
                    alert(`${gameTitle} game is do not run because kpos 12 is only run .kxp file and this file type is .exe`);
                    // In a real implementation, this would initialize the game
                });
            }
        }

        // Initialize the OS when the page loads
        window.onload = initOS;
        
        
            // Set up right-click context menu
            document.addEventListener('contextmenu', (e) => {
                e.preventDefault();
                const contextMenu = document.getElementById('context-menu');
                contextMenu.style.display = 'block';
                contextMenu.style.left = e.pageX + 'px';
                contextMenu.style.top = e.pageY + 'px';
                
                // Check if we clicked on an app icon
                if (e.target.closest('.desktop-icon')) {
                    currentContextApp = e.target.closest('.desktop-icon').getAttribute('onclick').match(/'([^']+)'/)[1];
                }
            });
            
            document.addEventListener('click', () => {
                document.getElementById('context-menu').style.display = 'none';
            });
            
    </script>
</body>
</html>
