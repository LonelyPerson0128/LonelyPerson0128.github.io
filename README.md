<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My GitHub Website</title>
    <link rel="icon" type="image/x-xicon" href="/images/favicon.ico">
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Creepster&display=swap" rel="stylesheet">
    <style>
        /* Custom styles for the Creepster font and basic body styling */
        body {
            font-family: "Creepster", system-ui;
            /* User's background image */
            background-image: url('https://i.pinimg.com/originals/2e/c8/1e/2ec81e1517a75592dd347207fa748d78.gif');
            background-size: cover; /* Ensure the image covers the entire background */
            background-attachment: fixed; /* Keep the background image fixed when scrolling */
            background-position: center; /* Center the background image */
            display: flex;
            flex-direction: column; /* Arrange header, main content, and footer vertically */
            justify-content: flex-start;
            align-items: center; /* Center content horizontally */
            min-height: 100vh;
            padding: 2rem; /* Add some padding around the content */
            box-sizing: border-box; /* Include padding in the element's total width and height */
            transition: background-color 0.3s ease; /* Smooth transition for dark mode */
        }

        /* --- Dark Mode Styles --- */
        body.dark-mode {
            background-color: #1a1a1a; /* Darker background for dark mode */
            background-image: none; /* Remove GIF background in dark mode for less distraction/performance */
            color: #e0e0e0; /* Lighter text for dark mode */
        }

        .dark-mode .main-content-area {
            background-color: #2c2c2c; /* Darker main content area */
            color: #e0e0e0;
        }

        .dark-mode .tab-button {
            background-color: #3a3a3a; /* Darker buttons */
            color: #e0e0e0;
        }

        .dark-mode .tab-button.active {
            background-color: #00cc14; /* Keep vibrant green for active tab */
            color: black;
        }

        .dark-mode .tab-button:hover {
            background-color: #4a4a4a; /* Darker hover */
        }

        .dark-mode footer {
            color: #e0e0e0;
        }

        .dark-mode footer a {
            color: #add8e6; /* Lighter blue for links in dark mode */
        }

        /* Hide content sections by default */
        .tab-content {
            display: none;
        }
        /* Show the active content section */
        .tab-content.active {
            display: block;
        }
        /* Style for active tab button */
        .tab-button.active {
            background-color: #00ff1a; /* This is a vibrant green */
            color: black;
        }
        /* Style for the footer to ensure visibility and proper placement */
        footer {
            margin-top: auto; /* Pushes the footer to the bottom */
            padding-top: 2rem;
            text-align: center;
            color: white; /* Ensure footer text is visible on the dark background */
        }
        footer a {
            color: #93c5fd; /* Light blue for links in the footer */
            text-decoration: underline;
        }

        /* Custom styles for black background on buttons and main content */
        .tab-button {
            background-color: black;
            color: white; /* Ensure text is visible on black background */
        }

        .tab-button:hover {
            background-color: #333; /* Slightly lighter black on hover */
        }

        .main-content-area {
            background-color: black;
            color: white; /* Ensure text is visible on black background */
            position: relative; /* Needed for positioning the music player */
        }

        /* Styles for the customizable banner */
        .custom-banner {
            background-image: url('https://i.pinimg.com/736x/f6/c1/05/f6c10582e6996bd489ed67852b00ec71.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
        }

        /* Styles for the music player */
        .music-player {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background-color: rgba(0, 0, 0, 0.7); /* Semi-transparent black */
            padding: 0.5rem 1rem;
            border-radius: 0.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            z-index: 10; /* Ensure it stays on top of other content */
        }
        .music-player button {
            background-color: #00ff1a;
            color: black;
            padding: 0.25rem 0.75rem;
            border-radius: 0.25rem;
            font-size: 0.875rem;
            cursor: pointer;
            transition: background-color 0.2s;
        }
        .music-player button:hover {
            background-color: #00cc14;
        }

        /* --- Back to Top Button Styles --- */
        #back-to-top {
            display: none; /* Hidden by default */
            position: fixed; /* Fixed position */
            bottom: 20px; /* Place at the bottom */
            right: 20px; /* Place at the right */
            z-index: 99; /* High z-index to be on top */
            font-size: 24px; /* Large icon */
            background-color: #00ff1a; /* Green background */
            color: black; /* Black text/icon */
            border: none; /* No border */
            border-radius: 50%; /* Circular shape */
            width: 50px;
            height: 50px;
            cursor: pointer; /* Pointer cursor on hover */
            display: flex;
            justify-content: center;
            align-items: center;
            transition: opacity 0.3s, transform 0.3s;
            opacity: 0; /* Start hidden */
            transform: translateY(20px); /* Start slightly off screen */
        }

        #back-to-top.show {
            opacity: 1;
            transform: translateY(0);
        }

        #back-to-top:hover {
            background-color: #00cc14; /* Darker green on hover */
        }

        /* --- Dark Mode Toggle Button Styles --- */
        #dark-mode-toggle {
            position: absolute;
            top: 1rem;
            left: 1rem;
            background-color: rgba(0, 0, 0, 0.7); /* Semi-transparent black */
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 0.5rem;
            border: none;
            cursor: pointer;
            z-index: 10;
            transition: background-color 0.2s, color 0.2s;
        }

        .dark-mode #dark-mode-toggle {
            background-color: rgba(255, 255, 255, 0.2); /* Lighter background in dark mode */
            color: #00ff1a; /* Green icon in dark mode */
        }

        #dark-mode-toggle:hover {
            background-color: rgba(0, 0, 0, 0.9);
        }

        .dark-mode #dark-mode-toggle:hover {
             background-color: rgba(255, 255, 255, 0.4);
        }

        /* --- Animations on Scroll --- */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        .fade-in.appear {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- Lightbox Styles --- */
        .lightbox-overlay {
            display: none; /* Hidden by default */
            position: fixed; /* Stay in place */
            z-index: 100; /* Sit on top */
            left: 0;
            top: 0;
            width: 100%; /* Full width */
            height: 100%; /* Full height */
            overflow: auto; /* Enable scroll if needed */
            background-color: rgba(0, 0, 0, 0.9); /* Black w/ opacity */
            align-items: center;
            justify-content: center;
        }

        .lightbox-overlay.active {
            display: flex;
        }

        .lightbox-content {
            margin: auto;
            display: block;
            max-width: 90%;
            max-height: 90%;
            object-fit: contain; /* Ensure image fits without cropping */
        }

        .lightbox-caption {
            margin: auto;
            display: block;
            width: 80%;
            max-width: 700px;
            text-align: center;
            color: #ccc;
            padding: 10px 0;
            height: 150px;
        }

        .lightbox-close {
            position: absolute;
            top: 15px;
            right: 35px;
            color: #f1f1f1;
            font-size: 40px;
            font-weight: bold;
            transition: 0.3s;
            cursor: pointer;
        }

        .lightbox-close:hover,
        .lightbox-close:focus {
            color: #bbb;
            text-decoration: none;
            cursor: pointer;
        }
        /* --- Simple Particle Effect --- */
        .particles-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none; /* Allows clicks to pass through */
            z-index: -1; /* Behind other content */
            overflow: hidden;
        }
        .particle {
            position: absolute;
            background-color: rgba(255, 255, 255, 0.5);
            border-radius: 50%;
            animation: floatAndFade 10s infinite ease-in-out;
        }

        @keyframes floatAndFade {
            0% {
                transform: translateY(0) translateX(0) scale(1);
                opacity: 0.5;
            }
            50% {
                transform: translateY(-50vh) translateX(20vw) scale(0.8);
                opacity: 0.2;
            }
            100% {
                transform: translateY(-100vh) translateX(-10vw) scale(0.5);
                opacity: 0;
            }
        }
        .dark-mode .particles-container {
            display: none; /* Hide particles in dark mode for cleaner look */
        }


    </style>
</head>
<body>
    <div class="particles-container" id="particles-container"></div>

    <div class="w-full max-w-4xl rounded-xl shadow-lg overflow-hidden bg-opacity-90 main-content-area">
        <header class="p-6 text-white text-center rounded-t-xl custom-banner">
            <h1 class="text-4xl font-bold mb-2">Hii welcome people :D!</h1>
            <p class="text-lg">A page That still is in a (WIP :P).</p>
        </header>

        <button id="dark-mode-toggle" aria-label="Toggle dark mode">🌙 Dark Mode</button>

        <div class="music-player">
            <audio id="background-music" src="YOUR_MUSIC_FILE_URL_HERE.mp3" loop muted></audio>
            <button id="music-toggle-button">Play Music</button>
        </div>

        <nav class="flex justify-center p-4 border-b border-gray-300">
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium transition-colors duration-200 focus:outline-none" data-tab="home">Home</button>
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium transition-colors duration-200 focus:outline-none" data-tab="about">My Art</button>
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium transition-colors duration-200 focus:outline-none" data-tab="community-art">Community Art</button>
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium transition-colors duration-200 focus:outline-none" data-tab="music">My Music</button>
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium transition-colors duration-200 focus:outline-none" data-tab="contact">Socials</button>
        </nav>

        <div class="p-8">
            <div id="home" class="tab-content active fade-in">
                <h2 class="text-3xl font-semibold mb-4">Welcome Lovelys to a page I'm trying to fix X_X!</h2>
                <p class="leading-relaxed mb-4">
                    This website will be Ig silly pics of me, Silly blogs, and also my music interest :P
                </p>
                <p class="leading-relaxed">
                    Use the tabs above to navigate through my page!:D
                </p>
                <img src="https://i.ibb.co/9mvrbK41/puG6st9.jpg" width="300" height="200" class="mt-4 rounded-lg shadow-lg fade-in"/>
            </div>

            <div id="about" class="tab-content fade-in">
                <h2 class="text-3xl font-semibold mb-4" style="background-color:firebrick; color:white; padding: 0.5rem; border-radius: 0.5rem;">Some pictures and what they are about :)! I love to edit and make art!</h2>
                <p class="leading-relaxed mb-4">Photoshop is LIFE!</p>

                <div class="image-gallery grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-8">
                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center fade-in">
                        <a href="#" class="image-link block" data-img-src="https://i.ibb.co/39wBVBbc/Picsart-25-07-02-19-44-17-326.png" data-caption="SICK EDIT! Made it because I got into 50's music lolz XP!">
                            <img src="https://i.ibb.co/39wBVBbc/Picsart-25-07-02-19-44-17-326.png" alt="SICK EDIT! Made it because I got into 50's music lolz XP!" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">SICK EDIT! Made it because I got into 50's music lolz XP!</p>
                    </div>

                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center fade-in">
                        <a href="#" class="image-link block" data-img-src="https://i.ibb.co/jZjZxGjw/Picsart-25-06-20-00-52-08-352.jpg" data-caption="IM IN A COMPUTER 0O0 OMGG!!!">
                            <img src="https://i.ibb.co/jZjZxGjw/Picsart-25-06-20-00-52-08-352.jpg" alt="IM IN A COMPUTER 0O0 OMGG!!!" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">IM IN A COMPUTER 0O0 OMGG!!!</p>
                    </div>

                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center fade-in">
                        <a href="#" class="image-link block" data-img-src="https://i.ibb.co/yBh41rd7/IMG20250610143513.jpg" data-caption="Self portrait I drew of myself. I love to draw myself A lot lolz XD!">
                            <img src="https://i.ibb.co/yBh41rd7/IMG20250610143513.jpg" alt="Self portrait I drew of myself. I love to draw myself A lot lolz XD!" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Self portrait I drew of myself. I love to draw myself A lot lolz XD!</p>
                    </div>

                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center fade-in">
                        <a href="#" class="image-link block" data-img-src="https://i.ibb.co/xSmy656y/IMG20250608180014.jpg" data-caption="Me and my friend in a GoodwillXD! We were taking dumb pics with the suits XD!">
                            <img src="https://i.ibb.co/xSmy656y/IMG20250608180014.jpg" alt="Me and my friend in a GoodwillXD! We were taking dumb pics with the suits XD!" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Me and my friend in a GoodwillXD! We were taking dumb pics with the suits XD!</p>
                    </div>
                </div>
            </div>

            <div id="community-art" class="tab-content fade-in">
                <h2 class="text-3xl font-semibold mb-4" style="background-color:darkgreen; color:white; padding: 0.5rem; border-radius: 0.5rem;">Awesome Art from Other Creators!</h2>
                <p class="leading-relaxed mb-4">
                    Here's a space dedicated to cool art, photos, or creations from friends, artists I admire, or anyone who wants to share! If you'd like your art featured, let me know on my socials!
                </p>

                <div class="image-gallery grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-8">
                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center fade-in">
                        <a href="#" class="image-link block" data-img-src="https://i.ibb.co/cXFWdf3V/6832750-2172237-mrkha-you-can-relax-my-friend-65ddcfadc76ac366cdc48539236bf75d.webp" data-caption="Kewl pixel art from musical fan art : You can relax my friend! By:MrKha">
                            <img src="https://i.ibb.co/cXFWdf3V/6832750-2172237-mrkha-you-can-relax-my-friend-65ddcfadc76ac366cdc48539236bf75d.webp" alt="Description of Community Art" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Kewl pixel art from musical fan art : You can relax my friend! By:MrKha </p>
                    </div>

                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center fade-in">
                        <a href="#" class="image-link block" data-img-src="https://via.placeholder.com/600x400/333/eee?text=Placeholder+Art+2" data-caption="Cool abstract piece by [Artist Name]">
                            <img src="https://via.placeholder.com/600x400/333/eee?text=Placeholder+Art+2" alt="Cool abstract piece by [Artist Name]" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Nothing yet</p>
                    </div>

                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center fade-in">
                        <a href="#" class="image-link block" data-img-src="https://via.placeholder.com/600x400/555/fff?text=Placeholder+Art+3" data-caption="A lovely photo by [Photographer Name]">
                            <img src="https://via.placeholder.com/600x400/555/fff?text=Placeholder+Art+3" alt="A lovely photo by [Photographer Name]" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Nothing yet</p>
                    </div>

                </div>
            </div>

            <div id="music" class="tab-content fade-in">
                <h3 class="text-3xl font-semibold mb-4" style="background-color:firebrick; color:white; padding: 0.5rem; border-radius: 0.5rem;">Just all the music I Love!! heheer</h3>
                <p class="leading-relaxed mb-4">Bands: Green day (for life XD), Ultra Q, Misfits,My chemical romance, studio Killers, Three days grace, and panic at the disco! Artist: Demi lovato, Billie joe armstrong, Britany spears, 6arelyhuman, lady gaga, darren styles, jeffree star, but I dont remember right now XD. Heres a few albums That describe me in the moment!</p>

                <div class="spotify-grid grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-8">
                    <div class="bg-gray-800 p-4 rounded-lg shadow-md fade-in">
                        <h4 class="text-xl font-semibold mb-2 text-center">My Current Mood Playlist</h4>
                        <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/37i9dQZF1EIfW21nLgM9bV?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                        <p class="text-sm text-gray-300 mt-2 text-center">I Like to dance!.</p>
                    </div>

                    <div class="bg-gray-800 p-4 rounded-lg shadow-md fade-in">
                        <h4 class="text-xl font-semibold mb-2 text-center">Favorite Album Right Now</h4>
                        <iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/0zQ0y4Wd0p0LzYw8K6f0gQ?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                        <p class="text-sm text-gray-300 mt-2 text-center">Lokey 1 of Green days best albums! with dirty and dancey lyrics!</p>
                    </div>

                    <div class="bg-gray-800 p-4 rounded-lg shadow-md fade-in">
                        <h4 class="text-xl font-semibold mb-2 text-center">Song on Repeat</h4>
                       <iframe style="border-radius:12px" src="https://open.spotify.com/embed/track/2S5kQ2C28eXw9y6S09Ff0t?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                        <p class="text-sm text-gray-300 mt-2 text-center">Honstely this song is sad... but one of the best to me personaly by 6arelyhuman!.</p>
                    </div>

                    </div>
            </div>

            <div id="contact" class="tab-content fade-in">
                <h2 class="text-3xl font-semibold mb-4">Where to follow me at!</h2>
                <p class="leading-relaxed mb-4">
                    Y'all can message me if y'all want! These places are where my art and post are! :D
                </p>
                <ul class="space-y-2">
                    <li><strong>Instagram:</strong> <a href="https://www.instagram.com/lonelyperson0128/" class="text-blue-400 hover:underline">https://www.instagram.com/lonelyperson0128/</a></li>
                    <li><strong>Youtube:</strong> <a href="https://www.youtube.com/channel/UCy7Q8E7qM8oP2Y0J7N0q9wA" target="_blank" class="text-blue-400 hover:underline">https://www.youtube.com/channel/UCy7Q8E7qM8oP2Y0J7N0q9wA</a></li>
                    <li><strong>Spacehey:</strong> <a href="https://spacehey.com/greendaysnumber1fanxp" target="_blank" class="text-blue-400 hover:underline">https://spacehey.com/greendaysnumber1fanxp</a></li>
                </ul>
            </div>
        </div>
    </div>

    <footer>
        <p>Author: Lonelyperson</p>
        <p><a href="https://spacehey.com/lonelyperson">Spacehey!-Lonelyperson</a></p>
    </footer>

    <button id="back-to-top" title="Go to top">↑</button>

    <div id="lightbox-overlay" class="lightbox-overlay">
        <span class="lightbox-close">&times;</span>
        <img class="lightbox-content" id="lightbox-img">
        <div id="lightbox-caption" class="lightbox-caption"></div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const tabButtons = document.querySelectorAll('.tab-button');
            const tabContents = document.querySelectorAll('.tab-content');
            const backgroundMusic = document.getElementById('background-music');
            const musicToggleButton = document.getElementById('music-toggle-button');
            const backToTopButton = document.getElementById('back-to-top');
            const darkModeToggle = document.getElementById('dark-mode-toggle');
            const imageLinks = document.querySelectorAll('.image-link');
            const lightboxOverlay = document.getElementById('lightbox-overlay');
            const lightboxImg = document.getElementById('lightbox-img');
            const lightboxCaption = document.getElementById('lightbox-caption');
            const lightboxClose = document.querySelector('.lightbox-close');
            const particlesContainer = document.getElementById('particles-container');


            // --- Tab Switching Logic (Existing) ---
            const showTab = (tabId) => {
                tabContents.forEach(content => content.classList.remove('active'));
                tabButtons.forEach(button => button.classList.remove('active'));
                document.getElementById(tabId).classList.add('active');
                document.querySelector(`.tab-button[data-tab="${tabId}"]`).classList.add('active');

                // Re-trigger fade-in for content when tab changes
                const activeTabContent = document.getElementById(tabId);
                activeTabContent.classList.remove('appear');
                void activeTabContent.offsetWidth; // Trigger reflow
                activeTabContent.classList.add('appear');

                // Trigger fade-in for child elements within the active tab
                const childrenToAnimate = activeTabContent.querySelectorAll('.fade-in');
                childrenToAnimate.forEach(el => {
                    el.classList.remove('appear');
                    void el.offsetWidth; // Trigger reflow
                    el.classList.add('appear');
                });
            };

            tabButtons.forEach(button => {
                button.addEventListener('click', () => {
                    const tabId = button.dataset.tab;
                    showTab(tabId);
                });
            });

            // Initially show the 'home' tab and apply fade-in
            showTab('home');

            // --- Music Player Logic (Existing) ---
            musicToggleButton.addEventListener('click', () => {
                if (backgroundMusic.paused) {
                    backgroundMusic.play();
                    musicToggleButton.textContent = 'Pause Music';
                } else {
                    backgroundMusic.pause();
                    musicToggleButton.textContent = 'Play Music';
                }
                backgroundMusic.muted = false;
            });

            backgroundMusic.play().catch(error => {
                console.log('Autoplay was prevented, user can click play button.', error);
            });

            // --- Back to Top Button Logic ---
            window.addEventListener('scroll', () => {
                if (window.scrollY > 300) { // Show button after scrolling 300px
                    backToTopButton.classList.add('show');
                } else {
                    backToTopButton.classList.remove('show');
                }
            });

            backToTopButton.addEventListener('click', () => {
                window.scrollTo({
                    top: 0,
                    behavior: 'smooth' // Smooth scroll
                });
            });

            // --- Dark Mode Toggle Logic ---
            const isDarkMode = localStorage.getItem('darkMode') === 'true';

            // Apply dark mode on load if previously enabled
            if (isDarkMode) {
                document.body.classList.add('dark-mode');
                darkModeToggle.textContent = '☀️ Light Mode';
            }

            darkModeToggle.addEventListener('click', () => {
                document.body.classList.toggle('dark-mode');
                const isNowDarkMode = document.body.classList.contains('dark-mode');
                localStorage.setItem('darkMode', isNowDarkMode); // Save preference

                if (isNowDarkMode) {
                    darkModeToggle.textContent = '☀️ Light Mode';
                    particlesContainer.style.display = 'none'; // Hide particles in dark mode
                } else {
                    darkModeToggle.textContent = '🌙 Dark Mode';
                    particlesContainer.style.display = 'block'; // Show particles in light mode
                }
            });


            // --- Animations on Scroll (Intersection Observer) ---
            const faders = document.querySelectorAll('.fade-in');

            const appearOptions = {
                threshold: 0.1, // Element is 10% visible
                rootMargin: "0px 0px -50px 0px" // Start appearing 50px before it hits the bottom of viewport
            };

            const appearOnScroll = new IntersectionObserver(function(entries, appearOnScroll) {
                entries.forEach(entry => {
                    if (!entry.isIntersecting) {
                        return;
                    } else {
                        entry.target.classList.add('appear');
                        appearOnScroll.unobserve(entry.target); // Stop observing once it has appeared
                    }
                });
            }, appearOptions);

            faders.forEach(fader => {
                appearOnScroll.observe(fader);
            });


            // --- Lightbox Logic ---
            imageLinks.forEach(link => {
                link.addEventListener('click', (e) => {
                    e.preventDefault(); // Prevent default link behavior
                    const imgSrc = link.dataset.imgSrc;
                    const imgCaption = link.dataset.caption;

                    lightboxImg.src = imgSrc;
                    lightboxCaption.textContent = imgCaption;
                    lightboxOverlay.classList.add('active');
                });
            });

            lightboxClose.addEventListener('click', () => {
                lightboxOverlay.classList.remove('active');
            });

            // Close lightbox if clicking outside the image
            lightboxOverlay.addEventListener('click', (e) => {
                if (e.target === lightboxOverlay) {
                    lightboxOverlay.classList.remove('active');
                }
            });

            // Close lightbox with ESC key
            document.addEventListener('keydown', (e) => {
                if (e.key === 'Escape' && lightboxOverlay.classList.contains('active')) {
                    lightboxOverlay.classList.remove('active');
                }
            });

            // --- Simple Particle Effect Logic ---
            const createParticle = () => {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                particlesContainer.appendChild(particle);

                const size = Math.random() * 5 + 2 + 'px'; // 2px to 7px
                particle.style.width = size;
                particle.style.height = size;

                const startX = Math.random() * 100 + 'vw';
                const startY = Math.random() * 100 + 'vh';
                particle.style.left = startX;
                particle.style.top = startY;

                // Randomize animation duration and delay
                particle.style.animationDuration = Math.random() * 8 + 6 + 's'; // 6s to 14s
                particle.style.animationDelay = Math.random() * 5 + 's'; // 0s to 5s

                // Remove particle after animation
                particle.addEventListener('animationend', () => {
                    particle.remove();
                });
            };

            // Generate a continuous stream of particles
            const particleInterval = setInterval(() => {
                if (!document.body.classList.contains('dark-mode')) { // Only create particles if not in dark mode
                     createParticle();
                }
            }, 500); // Create a new particle every 0.5 seconds

            // Initial particles on load
            for (let i = 0; i < 30; i++) {
                if (!document.body.classList.contains('dark-mode')) {
                    createParticle();
                }
            }
        });
    </script>
</body>
</html>
