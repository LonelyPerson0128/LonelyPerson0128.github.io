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
<html>
<head>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/5.1.0/css/bootstrap.min.css">
    <style>
        .tab_content {
            display: none;
        }

        .image-container {
            position: relative;
            display: inline-block;
        }

        .image-zoom {
            display: none;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 999;
        }

        .image-container:hover .image-zoom {
            display: block;
        }
    </style>
</head>
<body>

<div class="container">
    <button id="addMusicButton" class="btn btn-primary">Add Music</button>
    <br><br>

    <div class="row">
        <div class="col-md-3">
            <ul class="nav nav-tabs">
                <li class="nav-item">
                    <a class="nav-link active" data-bs-toggle="tab" href="#music1">Music 1</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" data-bs-toggle="tab" href="#music2">Music 2</a>
                </li>
            </ul>
        </div>
        <div class="col-md-9">
            <div class="tab-content">
                <div id="music1" class="tab-pane active tab_content">
                    <!-- Here you can add content for Music 1 -->
                </div>
                <div id="music2" class="tab-pane tab_content">
                    <!-- Here you can add content for Music 2 -->
                </div>
            </div>
        </div>
    </div>
</div>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.0/dist/js/bootstrap.bundle.min.js"></script>
<script>
    $(document).ready(function() {
        $('#addMusicButton').click(function() {
            var artist = prompt('Enter Artist Name:');
            var music = prompt('Enter Music Name:');
            var albumArt = prompt('Enter Album Art URL:');

            var content = '<div class="image-container">' +
                          '<img src="' + albumArt + '" alt="Album Art">' +
                          '<div class="image-zoom">' +
                          '<h4>' + artist + '</h4>' +
                          '<p>' + music + '</p>' +
                          '</div>' +
                          '</div>';

            $('.tab_content').append(content);
        });

        $('.nav-link').click(function() {
            $('.tab_content').hide();
            $($(this).attr('href')).show();
        });
    });
</script>

</body>
</html>
