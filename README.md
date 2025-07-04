<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My GitHub Website</title>
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom styles for the Inter font and basic body styling */
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
        }

        /* Styles for the customizable banner */
        .custom-banner {
            background-color: purple; /* Default purple background */
            /* You can uncomment and modify the lines below to use an image instead */
            /* background-image: url('YOUR_IMAGE_URL_HERE'); */
            /* background-size: cover; */
            /* background-position: center; */
            /* background-repeat: no-repeat; */
        }
    </style>
</head>
<body>
    <div class="w-full max-w-4xl rounded-xl shadow-lg overflow-hidden bg-opacity-90 main-content-area">
        <header class="p-6 text-white text-center rounded-t-xl custom-banner">
            <h1 class="text-4xl font-bold mb-2">Hii welcome people :D!</h1>
            <p class="text-lg">A page That still is in a (WIP :P).</p>
        </header>

        <nav class="flex justify-center p-4 border-b border-gray-300">
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium transition-colors duration-200 focus:outline-none" data-tab="home">Home</button>
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium transition-colors duration-200 focus:outline-none" data-tab="about">About Me</button>
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium transition-colors duration-200 focus:outline-none" data-tab="music">My Music</button>
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium transition-colors duration-200 focus:outline-none" data-tab="contact">Contact</button>
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
                <h2 class="text-3xl font-semibold mb-4" style="background-color:firebrick; color:white; padding: 0.5rem; border-radius: 0.5rem;">About me!</h2>
                <p class="leading-relaxed mb-4">I Like to listen to music ofc! Eat food ;-; Yes im guilty of it! also love to post on insa and kinda code on spacehey!!</p>
                
                <div class="image-gallery grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-8">
                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center">
                        <a href="https://via.placeholder.com/600x400/FF0000/FFFFFF?text=My+First+Post" target="_blank" class="block">
                            <img src="https://via.placeholder.com/300x200/FF0000/FFFFFF?text=My+First+Post" alt="Description of my first post" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">This is my very first post! Exploring new things. Click the image to see it bigger!</p>
                    </div>
                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center">
                        <a href="https://via.placeholder.com/600x400/00FF00/000000?text=Nature+Walk" target="_blank" class="block">
                            <img src="https://via.placeholder.com/300x200/00FF00/000000?text=Nature+Walk" alt="Picture from a nature walk" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Enjoyed a peaceful nature walk today. So refreshing!</p>
                    </div>
                    <div class="image-item bg-gray-800 p-4 rounded-lg shadow-md text-center">
                        <a href="https://via.placeholder.com/600x400/0000FF/FFFFFF?text=Coding+Time" target="_blank" class="block">
                            <img src="https://via.placeholder.com/300x200/0000FF/FFFFFF?text=Coding+Time" alt="Screenshot of coding" class="w-full h-auto rounded-lg mb-3 cursor-pointer object-cover">
                        </a>
                        <p class="text-sm text-gray-300">Late night coding session. Making progress on my website! :)</p>
                    </div>
                    </div>
            </div>

            <div id="music" class="tab-content">
                <h3 class="text-3xl font-semibold mb-4" style="background-color:firebrick; color:white; padding: 0.5rem; border-radius: 0.5rem;">Type of music I love!</h3>
                <p class="leading-relaxed mb-4">Bands: Green day (for life XD), Ultra Q, Misfits, And My chemical romance Artist: Demi lovato, Billie joe armstrong, Britany spears, 6arelyhuman, and Britany manson Theres probaly more, but I dont remember right now XD, but if u want to listen to my music! Heres the playlist!</p>
                <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/2Oeyrt4oIYWmsTG3YZkkuc?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
            </div>

            <div id="contact" class="tab-content">
                <h2 class="text-3xl font-semibold mb-4">📧 Get in Touch!</h2>
                <p class="leading-relaxed mb-4">
                    I'm always open to new opportunities and collaborations. Feel free to reach out to me via email or connect on social media.
                </p>
                <ul class="space-y-2">
                    <li><strong>Email:</strong> <a href="mailto:your.email@example.com" class="text-blue-400 hover:underline">your.email@example.com</a></li>
                    <li><strong>LinkedIn:</strong> <a href="https://linkedin.com/in/yourprofile" target="_blank" class="text-blue-400 hover:underline">linkedin.com/in/yourprofile</a></li>
                    <li><strong>GitHub:</strong> <a href="https://github.com/yourusername" target="_blank" class="text-blue-400 hover:underline">github.com/yourusername</a></li>
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

            // Initially show the 'home' tab when the page loads
            showTab('home');
        });
    </script>
</body>
</html>


