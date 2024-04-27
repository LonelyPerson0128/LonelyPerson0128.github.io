<h1 style="background-color:firebrick;">Welcome to my page!</h1> 
<DOCTYPE html>
<html>
<head>
<link rel="icon" type="image/x-icon" href="/images/favicon.ico">
</head>
<body>

<h2 style="background-color:firebrick;">About me!</h2> 
<p style="color:white;">I Like to listen to music ofc! Eat food ;-; Yes im guilty of it! also love to post on insa and kinda code on spacehey!!</p>


<h3 style="background-color:firebrick;">Type of music I love!</h3>
<p style="color:white;">Bands: Green day (for life XD), Ultra Q, Misfits, And My chemical romance
  Artist: Demi lovato, Billie joe armstrong, Britany spears, 6arelyhuman, and Britany manson
  Theres probaly more, but I dont remember right now XD, but if u want to listen to my music! Heres the playlist!
</p>

<iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/2Oeyrt4oIYWmsTG3YZkkuc?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>

</body>
<!-- This is a comment -->
<style>
  Body{
  Background-image: url('https://i.pinimg.com/564x/3e/26/5f/3e265f3b290a7e8615a5bb7194cabe78.jpg');
     
  }
  </style>
<!-- The background of my page! change it here! -->






<footer>
  <p style="color:white;">Author: Lonelyperson</p>
  <p><a href="https://spacehey.com/lonelyperson">Spacehey!-Lonelyperson</a></p>
</footer>







</html>

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Music Player</title>
    <style>
        .tab {
            display: none;
        }
    </style>
</head>

<body>
    <button id="tab1Button" onclick="openTab('tab1')">Favorite Music</button>
    <button id="tab2Button" onclick="openTab('tab2')">Add Music</button>

    <div id="tab1" class="tab" >
        <!-- Add favorite music and album art here -->
        <img src="album_art.jpg" alt="Album Art">
        <p>Artist: Artist Name</p>
        <p>Song: Song Title</p>
    </div>

    <div id="tab2" class="tab">
        <!-- Code to add new music or edit existing music -->
        <!-- Example: -->
        <input type="text" placeholder="Artist Name">
        <input type="text" placeholder="Song Title">
        <input type="file">
    </div>

    <script>
        function openTab(tabName) {
            var tabs = document.getElementsByClassName('tab');
            for (var i = 0; i < tabs.length; i++) {
                tabs[i].style.display = 'none';
            }
            document.getElementById(tabName).style.display = 'block';
        }
    </script>
</body>

</html>


