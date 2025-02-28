<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mayank Bhambhani - Screenplay</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Courier+Prime&display=swap">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Courier Prime', 'Courier New', Courier, monospace;
            background: #fff;
            color: #000;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            text-align: center;
            opacity: 0;
            animation: fadeIn 1s forwards;
            padding: 20px;
        }

        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        @keyframes fadeOut { from { opacity: 1; } to { opacity: 0; } }
        .fade-out { animation: fadeOut 0.5s forwards; }

        .title { font-size: 36px; font-weight: bold; }
        .subtitle { font-size: 22px; margin-top: 10px; }

        .links {
            margin-top: 30px;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
        }

        .links a {
            font-size: 18px;
            font-weight: bold;
            color: #000;
            text-decoration: none;
            padding: 10px 20px;
            border: 2px solid #000;
            border-radius: 5px;
            transition: 0.3s;
            width: 180px;
            text-align: center;
        }

        .links a:hover {
            background: #000;
            color: #fff;
        }

        .arrow {
            font-size: 28px;
            position: absolute;
            bottom: 30px;
            right: 30px;
            transform: rotate(45deg);
            cursor: pointer;
        }

        @media (max-width: 768px) {
            .title { font-size: 28px; }
            .subtitle { font-size: 18px; }
            .links a { width: 150px; font-size: 16px; }
        }

    </style>
</head>
<body>
    <div class="title">MAYANK BHAMBHANI</div>
    <div class="subtitle">WRITER</div>

    <div class="links">
        <a href="about.html" class="page-link">Introduction</a>
        <a href="portfolio.html" class="page-link">Portfolio</a>
        <a href="contact.html" class="page-link">Contact</a>
    </div>

    <div class="arrow">↓</div>

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
