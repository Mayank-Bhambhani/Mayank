<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Introduction - Screenplay</title>
    <style>
        body {
            font-family: "Courier New", Courier, monospace;
            background: #fff;
            color: #000;
            padding: 40px;
            line-height: 1.8;
            opacity: 0;
            animation: fadeIn 1s forwards;
        }

        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        @keyframes fadeOut { from { opacity: 1; } to { opacity: 0; } }
        .fade-out { animation: fadeOut 0.5s forwards; }

        .nav-links { position: absolute; top: 20px; right: 20px; }
        .nav-links a { color: #000; text-decoration: none; margin-left: 15px; font-weight: bold; }

        .scene-heading { font-weight: bold; text-transform: uppercase; margin-top: 30px; }
        .character { font-weight: bold; text-transform: uppercase; margin-top: 25px; }
        .dialogue { margin-left: 50px; max-width: 80%; }
        .action { margin-left: 30px; font-style: italic; }
    </style>
</head>
<body>
    <div class="nav-links">
        <a href="index.html" class="page-link">Title</a>
        <a href="portfolio.html" class="page-link">Portfolio</a>
        <a href="contact.html" class="page-link">Contact</a>
    </div>

    <p class="scene-heading">INT. A CAFE - NIGHT</p>
    <p class="action">A lone writer sits by the window, watching the city buzz around him. A notebook lies open, filled with ideas.</p>

    <p class="character">MAYANK BHAMBHANI</p>
    <p class="dialogue">"Stories are everywhere. In the silence of an empty street. In the laughter of strangers. In the chaos of a deadline. And in me."</p>

    <p class="scene-heading">INTRODUCTION</p>
    <p class="dialogue">A writer, a storyteller, a thinker. With a background in English literature and experience in digital marketing, filmmaking, and poetry, Mayank crafts narratives that inform, engage, and inspire.</p>

    <script>
        document.querySelectorAll('.page-link').forEach(link => {
            link.addEventListener('click', function(event) {
                event.preventDefault();
                let destination = this.getAttribute('href');
                document.body.classList.add('fade-out');
                setTimeout(() => { window.location.href = destination; }, 500);
            });
        });
    </script>
</body>
</html>
