<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NITHIN VINCENT - Game Developer</title>
    <!-- Imports a clean, modern font -->
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap');

        /* --- Global Styles --- */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #121212;
            color: #e0e0e0;
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }

        .container {
            max-width: 900px;
            margin: 40px auto;
            padding: 20px;
        }

        /* --- Header --- */
        header {
            text-align: center;
            border-bottom: 2px solid #333;
            padding-bottom: 20px;
            margin-bottom: 40px;
        }

        header h1 {
            color: #ffffff;
            font-size: 2.5em;
            margin: 0;
        }

        header p {
            color: #bb86fc; /* A nice accent color */
            font-size: 1.2em;
        }

        /* --- Sections --- */
        h2 {
            color: #ffffff;
            border-bottom: 1px solid #bb86fc;
            padding-bottom: 5px;
            margin-top: 40px;
        }

        p {
            font-size: 1.1em;
        }

        a {
            color: #03dac6; /* Another accent color */
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
        }

        /* --- Project Grid --- */
        .project-grid {
            display: grid;
            /* This creates a responsive grid. It will stack on mobile. */
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .project-card {
            background-color: #1e1e1e;
            border: 1px solid #333;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
            transition: transform 0.2s;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-card h3 {
            color: #bb86fc;
            margin-top: 0;
        }

        /* --- Project Image Style --- */
        .project-card img {
            width: 100%; /* Make image fill the card width */
            border-radius: 4px; /* Slightly rounded corners for the image */
            margin-bottom: 15px; /* Space below the image */
            border: 1px solid #444; /* A subtle border for the image */
            aspect-ratio: 16 / 10; /* Keep a consistent shape */
            object-fit: cover; /* Ensure image covers the space */
        }
        
        .project-card b {
            color: #03dac6;
        }

        /* --- Project Links (itch.io, Video) --- */
        .project-links {
            margin-top: 20px;
            display: flex;
            flex-wrap: wrap; /* Allow links to wrap on small screens */
            gap: 15px; /* Space between links */
        }

        .project-links a {
            background-color: #bb86fc;
            color: #121212; /* Dark text on light button */
            padding: 8px 12px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 700;
            transition: background-color 0.2s;
            cursor: pointer; /* So it looks clickable */
        }

        .project-links a:hover {
            background-color: #e0e0e0;
            text-decoration: none;
        }

        /* Secondary link style (e.g., for video) */
        .project-links a.secondary {
            background-color: transparent;
            color: #03dac6;
            border: 1px solid #03dac6;
            padding: 7px 11px; /* Adjust padding for border */
        }

        .project-links a.secondary:hover {
            background-color: rgba(3, 218, 198, 0.1); /* Faint background on hover */
            text-decoration: none;
        }
        
        /* --- Footer --- */
        footer {
            text-align: center;
            margin-top: 50px;
            border-top: 1px solid #333;
            padding-top: 20px;
            color: #888;
        }

        /* --- NEW: Video Modal Styles --- */
        .modal {
            display: none; /* Hidden by default */
            position: fixed; /* Stay in place */
            z-index: 1000; /* Sit on top */
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto; /* Enable scroll if needed */
            background-color: rgba(0,0,0,0.85); /* Black w/ opacity */
        }

        .modal-content {
            position: relative;
            margin: 5% auto; /* 5% from the top and centered */
            padding: 20px;
            width: 80%;
            max-width: 800px;
        }

        /* The Close Button */
        .close {
            color: #aaa;
            position: absolute;
            top: -10px;
            right: 15px;
            font-size: 40px;
            font-weight: bold;
        }

        .close:hover,
        .close:focus {
            color: white;
            text-decoration: none;
            cursor: pointer;
        }
        
        /* Responsive Iframe for video */
        .video-container {
            position: relative;
            padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
            height: 0;
            overflow: hidden;
            max-width: 100%;
            background: #000;
        }
        
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
    </style>
</head>
<body>

    <div class="container">
        
        <header>
            <h1>NITHIN VINCENT</h1>
            <p>Game Developer & Designer</p>
        </header>

        <main>
            <section id="about">
                <h2>About Me</h2>
                <p>
                    Hello! I'm a passionate game developer specializing in Unity and C#. I love creating engaging
                    and tactical game experiences. Below are some of the projects I've worked on.
                </p>
            </section>

            <section id="projects">
                <h2>My Projects</h2>

                <div class="project-grid">

                    <!-- PROJECT 1: Tower Tactics -->
                    <div class="project-card">
                        <h3>Tower Tactics</h3>
                        
                        <!-- 
                          This image loads from your repository. 
                          Make sure you have uploaded "tower-tactics.jpg"
                        -->
                        <img src="tower-tactics.jpg" alt="Tower Tactics Gameplay Screenshot">

                        <p>
                            A strategic defense game where players must defend their base against waves of 
                            incoming enemies by strategically placing and upgrading towers.
                        </p>
                        <p>
                            <b>Challenge Faced:</b> The biggest challenge was balancing the game's difficulty. 
                            It required constant playtesting to ensure enemy waves felt challenging but not 
                            impossible, making sure every tower choice felt useful and tactical.
                        </p>
                        <p>
                            <b>Technologies:</b> Unity, C#, Wwise (for audio integration)
                        </p>
                        
                        <!-- 
                          EDIT THIS LINK SECTION:
                          1. Replace "#" with your real itch.io link.
                          2. Replace "YOUTUBE_ID_HERE" with your YouTube video ID.
                        -->
                        <div class="project-links">
                            <a href="#" target="_blank">Play on itch.io</a>
                            <a class="secondary" onclick="openModal('YOUTUBE_ID_HERE')">Watch Video</a>
                        </div>
                    </div>

                    <!-- PROJECT 2: Memory Puzzle -->
                    <div class="project-card">
                        <h3>Memory Puzzle Game</h3>

                        <!-- 
                          EDIT THIS PART: 
                          Upload your screenshot (e.g., "memory-puzzle.png") 
                          and change the src="..." to your image name.
                        -->
                        <img src="memory-puzzle.jpg" alt="Memory Puzzle Gameplay Screenshot">

                        <p>
                            A classic card-matching memory game with a 4x4 grid. The game features
                            flip animations, a timer, and a limited number of attempts.
                        </p>
                        <p>
                            <b>Challenge Faced:</b> Implementing the animation state machine in Unity
                            to smoothly handle all card states (idle, flip, shake, unflip) 
                            without logic conflicts was a key challenge.
                        </p>
                        <p>
                            <b>Technologies:</b> Unity, C#
                        </p>

                        <!-- 
                          EDIT THIS LINK SECTION:
                          1. Replace "#" with your real itch.io link.
                          2. Replace "YOUTUBE_ID_HERE" with your YouTube video ID.
                        -->
                        <div class="project-links">
                            <a href="#" target="_blank">Play on itch.io</a>
                            <a class="secondary" onclick="openModal('YOUTUBE_ID_HERE')">Watch Video</a>
                        </div>
                    </div>

                </div>
            </section>
        </main>

        <footer>
            <!-- 
              EDIT THIS PART: 
              Change the email address to your own.
            -->
            <p>Get in touch! <a href="mailto:youremail@example.com">youremail@example.com</a></p>
        </footer>

    </div>
    
    <!-- NEW: Video Modal HTML -->
    <div id="videoModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <div class="video-container">
                <iframe id="videoPlayer" src="" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>
        </div>
    </div>

    <!-- NEW: JavaScript for Modal -->
    <script>
        // Get the modal
        var modal = document.getElementById("videoModal");
        var videoPlayer = document.getElementById("videoPlayer");

        // Function to open the modal and play the video
        function openModal(videoId) {
            videoPlayer.src = "https://www.youtube.com/embed/" + videoId + "?autoplay=1";
            modal.style.display = "block";
        }

        // Function to close the modal and stop the video
        function closeModal() {
            modal.style.display = "none";
            videoPlayer.src = ""; // Stop the video
        }

        // When the user clicks anywhere outside of the modal, close it
        window.onclick = function(event) {
            if (event.target == modal) {
                closeModal();
            }
        }
    </script>
    
</body>
</html>
