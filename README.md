<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Professional Writing Portfolio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: #f4f4f4;
            color: #333;
        }
        header {
            background: #222;
            color: #fff;
            padding: 20px;
            text-align: center;
        }
        .container {
            width: 80%;
            margin: auto;
            overflow: hidden;
            padding: 20px;
            background: #fff;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
        }
        .writing-sample {
            border-bottom: 1px solid #ddd;
            padding: 15px 0;
        }
        .writing-sample h2 {
            margin: 0;
            color: #444;
        }
        .writing-sample p {
            font-size: 14px;
            color: #666;
        }
        .btn {
            display: inline-block;
            margin-top: 10px;
            padding: 10px 15px;
            background: #007BFF;
            color: white;
            text-decoration: none;
            border-radius: 5px;
        }
        .btn:hover {
            background: #0056b3;
        }
        footer {
            text-align: center;
            padding: 10px;
            background: #222;
            color: white;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>
        <h1>My Writing Portfolio</h1>
        <p>Showcasing my best work</p>
    </header>
    <div class="container" id="portfolio">
        <!-- Writing samples will be added dynamically -->
    </div>
    <footer>
        <p>&copy; 2025 Your Name | All Rights Reserved</p>
    </footer>
    <script>
        const samples = [
            { title: "The Art of Storytelling", description: "An in-depth analysis of storytelling techniques.", link: "#" },
            { title: "Writing for Impact", description: "How to create powerful and engaging narratives.", link: "#" },
            { title: "Screenwriting Essentials", description: "A guide to crafting compelling scripts.", link: "#" }
        ];

        const portfolioDiv = document.getElementById("portfolio");
        
        samples.forEach(sample => {
            const sampleDiv = document.createElement("div");
            sampleDiv.classList.add("writing-sample");
            sampleDiv.innerHTML = `
                <h2>${sample.title}</h2>
                <p>${sample.description}</p>
                <a href="${sample.link}" class="btn">Read More</a>
            `;
            portfolioDiv.appendChild(sampleDiv);
        });
    </script>
</body>
</html>
