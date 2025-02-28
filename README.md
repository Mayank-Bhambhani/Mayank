<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mayank Bhambhani - Screenplay</title>
    <style>
        /* Ensuring "Courier New" works across all browsers */
        @font-face {
            font-family: 'CourierCustom';
            src: local('Courier New'), local('Courier'), local('monospace');
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'CourierCustom', 'Courier New', Courier, monospace;
            background: #fff;
            color: #000;
            text-align: center;
            padding-top: 200px;
            opacity: 0;
            animation: fadeIn 1s forwards;
            position: relative;
            min-height: 100vh;
            overflow: hidden;
        }

        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        @keyframes fadeOut { from { opacity: 1; } to { opacity: 0; } }
        .fade-out { animation: fadeOut 0.5s forwards; }

        .title {
            font-size: 32px;
            font-weight: bold;
        }

        .subtitle {
            font-size: 20px;
            margin-top: 10px;
        }

        .links {
            position: absolute;
            top: 20px;
            right: 20px;
            text-align: right;
        }

        .links a {
            display: block;
            margin-top: 10px;
            font-weight: bold;
            color: #000;
            text-decoration: none;
            font-size: 18px;
            transition: 0.3s;
        }

        .links a:hover {
            color: gray;
        }

        .arrow {
            font-size: 24px;
            position: absolute;
            bottom: 50px;
            right: 50px;
            transform: rotate(45deg);
            cursor: pointer;
        }

        /* Responsive Adjustments */
        @media (max-width: 768px) {
            body {
                padding-top: 150px;
            }

            .title {
                font-size: 28px;
            }

            .subtitle {
                font-size: 18px;
            }

            .links {
                top: 10px;
                right: 10px;
            }

            .links a {
                font-size: 16px;
            }

            .arrow {
                bottom: 20px;
                right: 20px;
            }
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

    <div class="arrow">lol</div>

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
