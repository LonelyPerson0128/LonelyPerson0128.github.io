<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My GitHub Website</title>
    <link rel="icon" type="image/x-xicon" href="/images/favicon.ico">
    <script src="https://cdn.tailwindcss.com"></script>
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
    </style>
</head>
<body>
    <div class="w-full max-w-4xl rounded-xl shadow-lg overflow-hidden bg-opacity-90 main-content-area">
        <header class="p-6 text-white text-center rounded-t-xl custom-banner">
            <h1 class="text-4xl font-bold mb-2">Hii welcome people :D!</h1>
            <p class="text-lg">A page That still is in a (WIP :P).</p>
        </header>

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
            <div id="home" class="tab-content active">
                <h2 class="text-3xl font-semibold mb-4">Welcome Lovelys to a page I'm trying to fix X_X!</h2>
                <p class="leading-relaxed mb-4">
                    This website will be Ig silly pics of me, Silly blogs, and also my music interest :P
                </p>
                <p class="leading-relaxed">
                    Use the tabs above to navigate through my page!:D
                </p>
                <img src="https://i.ibb.co/9mvrbK41/puG6st9.jpg" width="300" height="200"/> 
            </div>

            <div id="about" class="tab-content">
                <h2 class="text-3xl font-semibold mb-4" style="background-color:firebrick; color:white; padding: 0.5rem; border-radius: 0.5rem;">Some pictures and what they are about :)! I love to edit and make art!</h2>
                <p class="leading-relaxed mb-4">Photoshop is LIFE!</p>
                
                <div class="image-gallery grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-8">
                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center">
                        <a href="https://i.ibb.co/39wBVBbc/Picsart-25-07-02-19-44-17-326.png" target="_blank" class="block">
                            <img src="https://i.ibb.co/39wBVBbc/Picsart-25-07-02-19-44-17-326.png" alt="SICK EDIT! Made it because I got into 50's music lolz XP!" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">SICK EDIT! Made it because I got into 50's music lolz XP!</p>
                    </div>

                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center">
                        <a href="https://i.ibb.co/jZjZxGjw/Picsart-25-06-20-00-52-08-352.jpg" target="_blank" class="block">
                            <img src="https://i.ibb.co/jZjZxGjw/Picsart-25-06-20-00-52-08-352.jpg" alt="IM IN A COMPUTER 0O0 OMGG!!!" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">IM IN A COMPUTER 0O0 OMGG!!!</p>
                    </div>

                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center">
                        <a href="https://i.ibb.co/yBh41rd7/IMG20250610143513.jpg" target="_blank" class="block">
                            <img src="https://i.ibb.co/yBh41rd7/IMG20250610143513.jpg" alt="Self portrait I drew of myself. I love to draw myself A lot lolz XD!" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Self portrait I drew of myself. I love to draw myself A lot lolz XD!</p>
                    </div>

                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center">
                        <a href="https://i.ibb.co/xSmy656y/IMG20250608180014.jpg" target="_blank" class="block">
                            <img src="https://i.ibb.co/xSmy656y/IMG20250608180014.jpg" alt="Me and my friend in a GoodwillXD! We were taking dumb pics with the suits XD!" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Me and my friend in a GoodwillXD! We were taking dumb pics with the suits XD!</p>
                    </div>
                </div>
            </div>

            <div id="community-art" class="tab-content">
                <h2 class="text-3xl font-semibold mb-4" style="background-color:darkgreen; color:white; padding: 0.5rem; border-radius: 0.5rem;">Awesome Art from Other Creators!</h2>
                <p class="leading-relaxed mb-4">
                    Here's a space dedicated to cool art, photos, or creations from friends, artists I admire, or anyone who wants to share! If you'd like your art featured, let me know on my socials!
                </p>
                
                <div class="image-gallery grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-8">
                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center">
                        <a href="YOUR_COMMUNITY_ART_IMAGE_URL_HERE.jpg" target="_blank" class="block">
                            <img src="YOUR_COMMUNITY_ART_IMAGE_URL_HERE.jpg" alt="Description of Community Art" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Description of this awesome community art. Give credit here!</p>
                    </div>

                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center">
                        <a href="https://i.ibb.co/jZmZxGjw/example-community-art-2.jpg" target="_blank" class="block">
                            <img src="https://i.ibb.co/jZmZxGjw/example-community-art-2.jpg" alt="Cool abstract piece by [Artist Name]" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Nothing yet</p>
                    </div>
                    
                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center">
                        <a href="https://i.ibb.co/jZmZxGjw/example-community-art-3.jpg" target="_blank" class="block">
                            <img src="https://i.ibb.co/jZmZxGjw/example-community-art-3.jpg" alt="A lovely photo by [Photographer Name]" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Nothing yet</p>
                    </div>

                </div>
            </div>

            <div id="music" class="tab-content">
                <h3 class="text-3xl font-semibold mb-4" style="background-color:firebrick; color:white; padding: 0.5rem; border-radius: 0.5rem;">Just all the music I Love!! heheer</h3>
                <p class="leading-relaxed mb-4">Bands: Green day (for life XD), Ultra Q, Misfits,My chemical romance, studio Killers, Three days grace, and panic at the disco! Artist: Demi lovato, Billie joe armstrong, Britany spears, 6arelyhuman, lady gaga, darren styles, jeffree star, but I dont remember right now XD. Heres a few albums That describe me in the moment!</p>
                
                <div class="spotify-grid grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-8">
                    <div class="bg-gray-800 p-4 rounded-lg shadow-md">
                        <h4 class="text-xl font-semibold mb-2 text-center">My Current Mood Playlist</h4>
                        <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/56Xxj4tGzN9smTgEkKdVqI?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                        <p class="text-sm text-gray-300 mt-2 text-center">I Like to dance!.</p>
                    </div>

                    <div class="bg-gray-800 p-4 rounded-lg shadow-md">
                        <h4 class="text-xl font-semibold mb-2 text-center">Favorite Album Right Now</h4>
                        <iframe style="border-radius:12px" src="https://open.spotify.com/embed/album/71rrqHKVkUFx2CSVfxrrLs?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                        <p class="text-sm text-gray-300 mt-2 text-center">Lokey 1 of Green days best albums! with dirty and dancey lyrics!</p>
                    </div>

                    <div class="bg-gray-800 p-4 rounded-lg shadow-md">
                        <h4 class="text-xl font-semibold mb-2 text-center">Song on Repeat</h4>
                       <iframe style="border-radius:12px" src="https://open.spotify.com/embed/track/4A96t6zxkRfmFd1ky7Orkv?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                        <p class="text-sm text-gray-300 mt-2 text-center">Honstely this song is sad... but one of the best to me personaly by 6arelyhuman!.</p>
                    </div>

                    </div>
            </div>

            <div id="contact" class="tab-content">
                <h2 class="text-3xl font-semibold mb-4">Where to follow me at!</h2>
                <p class="leading-relaxed mb-4">
                    Y'all can message me if y'all want! These places are where my art and post are! :D
                </p>
                <ul class="space-y-2">
                    <li><strong>Instagram:</strong> <a href="https://www.instagram.com/lonelyperson0128/" class="text-blue-400 hover:underline">https://www.instagram.com/lonelyperson0128/</a></li>
                    <li><strong>Youtube:</strong> <a href="https://www.youtube.com/channel/UC-your-youtube-channel-id" target="_blank" class="text-blue-400 hover:underline">https://www.youtube.com/channel/UC-your-youtube-channel-id</a></li>
                    <li><strong>Spacehey:</strong> <a href="https://spacehey.com/greendaysnumber1fanxp" target="_blank" class="text-blue-400 hover:underline">https://spacehey.com/greendaysnumber1fanxp</a></li>
                </ul>
            </div>
        </div>
    </div>

    <footer>
        <p>Author: Lonelyperson</p>
        <p><a href="https://spacehey.com/lonelyperson">Spacehey!-Lonelyperson</a></p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const tabButtons = document.querySelectorAll('.tab-button');
            const tabContents = document.querySelectorAll('.tab-content');
            const backgroundMusic = document.getElementById('background-music');
            const musicToggleButton = document.getElementById('music-toggle-button');

            // Function to show a specific tab
            const showTab = (tabId) => {
                // Remove 'active' class from all content sections and buttons
                tabContents.forEach(content => content.classList.remove('active'));
                tabButtons.forEach(button => button.classList.remove('active'));

                // Add 'active' class to the selected content section
                document.getElementById(tabId).classList.add('active');

                // Add 'active' class to the clicked button
                document.querySelector(`.tab-button[data-tab="${tabId}"]`).classList.add('active');
            };

            // Add click event listeners to all tab buttons
            tabButtons.forEach(button => {
                button.addEventListener('click', () => {
                    const tabId = button.dataset.tab; // Get the tab ID from the data-tab attribute
                    showTab(tabId);
                });
            });

            // Music player logic
            musicToggleButton.addEventListener('click', () => {
                if (backgroundMusic.paused) {
                    backgroundMusic.play();
                    musicToggleButton.textContent = 'Pause Music';
                } else {
                    backgroundMusic.pause();
                    musicToggleButton.textContent = 'Play Music';
                }
                // Also unmute if it was muted for autoplay
                backgroundMusic.muted = false;
            });

            // Handle autoplay with mute for better browser compatibility
            // Try to play when the page loads, but muted
            backgroundMusic.play().catch(error => {
                // Autoplay failed (e.g., user didn't interact) - no big deal, button still works
                console.log('Autoplay was prevented, user can click play button.', error);
            });


            // Initially show the 'home' tab when the page loads
            showTab('home');
        });
    </script>
</body>
</html>


