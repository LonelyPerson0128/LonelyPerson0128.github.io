<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My GitHub Website</title>
    <!-- User's favicon -->
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
    <!-- Tailwind CSS CDN for easy styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom styles for the Inter font and basic body styling */
        body {
            font-family: 'Inter', sans-serif;
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
            background-color: #4f46e5; /* Indigo 600 */
            color: white;
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
    </style>
</head>
<body>
    <div class="w-full max-w-4xl bg-white rounded-xl shadow-lg overflow-hidden bg-opacity-90">
        <!-- Header Section - Modified to user's content and style -->
        <header class="bg-gradient-to-r from-indigo-500 to-purple-600 p-6 text-white text-center rounded-t-xl">
            <h1 class="text-4xl font-bold mb-2" style="background-color:firebrick;">Hii welcome people :D!</h1>
            <p class="text-lg">A page That still is in a (WIP :P).</p>
        </header>

        <!-- Tab Navigation -->
        <nav class="flex justify-center bg-gray-200 p-4 border-b border-gray-300">
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium text-gray-700 hover:bg-gray-300 transition-colors duration-200 focus:outline-none" data-tab="home">Home</button>
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium text-gray-700 hover:bg-gray-300 transition-colors duration-200 focus:outline-none" data-tab="about">About Me</button>
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium text-gray-700 hover:bg-gray-300 transition-colors duration-200 focus:outline-none" data-tab="music">My Music</button>
            <button class="tab-button px-6 py-3 mx-2 rounded-lg text-lg font-medium text-gray-700 hover:bg-gray-300 transition-colors duration-200 focus:outline-none" data-tab="contact">Contact</button>
        </nav>

        <!-- Tab Content Areas -->
        <div class="p-8">
            <!-- Home Content -->
            <div id="home" class="tab-content active">
                <h2 class="text-3xl font-semibold text-gray-800 mb-4">Welcome Lovelys to a page I'm trying to fix X_X!</h2>
                <p class="text-gray-600 leading-relaxed mb-4">
                    This website will be Ig silly pics of me, Silly blogs, and also my music interest :P
                </p>
                <p class="text-gray-600 leading-relaxed">
                    Use the tabs above to navigate through my page!:D
                </p>
                <img src="https://i.ibb.co/9mvrbK41/puG6st9.jpg" width="300" height="200"/> 
            </div>

            <!-- About Me Content - User's "About me!" content -->
            <div id="about" class="tab-content">
                <h2 class="text-3xl font-semibold mb-4" style="background-color:firebrick; color:white; padding: 0.5rem; border-radius: 0.5rem;">About me!</h2>
                <p class="leading-relaxed mb-4" style="color:white;">I Like to listen to music ofc! Eat food ;-; Yes im guilty of it! also love to post on insa and kinda code on spacehey!!</p>
                <img src="https://placehold.co/600x300/ffe0e7/e54f46?text=About+Me+Image" alt="About Me Placeholder" class="w-full h-auto rounded-lg mt-6 shadow-md">
            </div>

            <!-- My Music Content - User's "Type of music I love!" content -->
            <div id="music" class="tab-content">
                <h3 class="text-3xl font-semibold mb-4" style="background-color:firebrick; color:white; padding: 0.5rem; border-radius: 0.5rem;">Type of music I love!</h3>
                <p class="leading-relaxed mb-4" style="color:white;">Bands: Green day (for life XD), Ultra Q, Misfits, And My chemical romance Artist: Demi lovato, Billie joe armstrong, Britany spears, 6arelyhuman, and Britany manson Theres probaly more, but I dont remember right now XD, but if u want to listen to my music! Heres the playlist!</p>
                <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/2Oeyrt4oIYWmsTG3YZkkuc?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
            </div>

            <!-- Contact Content - Placeholder, you can fill this in -->
            <div id="contact" class="tab-content">
                <h2 class="text-3xl font-semibold text-gray-800 mb-4">📧 Get in Touch!</h2>
                <p class="text-gray-600 leading-relaxed mb-4">
                    I'm always open to new opportunities and collaborations. Feel free to reach out to me via email or connect on social media.
                </p>
                <ul class="text-gray-700 space-y-2">
                    <li><strong>Email:</strong> <a href="mailto:your.email@example.com" class="text-blue-600 hover:underline">your.email@example.com</a></li>
                    <li><strong>LinkedIn:</strong> <a href="https://linkedin.com/in/yourprofile" target="_blank" class="text-blue-600 hover:underline">linkedin.com/in/yourprofile</a></li>
                    <li><strong>GitHub:</strong> <a href="https://github.com/yourusername" target="_blank" class="text-blue-600 hover:underline">github.com/yourusername</a></li>
                </ul>
            </div>
        </div>
    </div>

    <!-- User's Footer -->
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


