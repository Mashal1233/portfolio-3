<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio - Mashal Roghani</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: 'Poppins', sans-serif;
            background: #1f242d;
            color: #fff;
        }
        .navbar {
            position: fixed; top: 0; width: 100%;
            padding: 20px 8%;
            display: flex; justify-content: space-between; align-items: center;
            background: #1f242d; z-index: 1000;
        }
        .navbar .logo { font-size: 28px; font-weight: 700; color: #fff; }
        .navbar ul { display: flex; list-style: none; }
        .navbar ul li { margin-left: 30px; }
        .navbar ul li a {
            text-decoration: none; color: #fff; font-size: 18px; transition: 0.3s;
        }
        .navbar ul li a:hover, .navbar ul li a.active { color: #7cf03d; }

        .home {
            display: flex; align-items: center; justify-content: space-between;
            padding: 100px 8% 0; min-height: 100vh; flex-wrap: wrap;
        }
        .home-text { max-width: 500px; animation: fadeIn 1.5s ease-in-out; }
        .home-text h1 { font-size: 48px; font-weight: 700; }
        .home-text h3 {
            font-size: 24px; font-weight: 500; margin-top: 10px;
        }
        .home-text h3 span {
            color: #7cf03d; position: relative; display: inline-block;
            transition: all 0.3s ease-in-out;
            cursor: pointer;
        }
        .home-text h3 span:hover {
            color: #fff;
            text-shadow: 0 0 10px #7cf03d, 0 0 20px #7cf03d;
            transform: scale(1.05);
        }
        .home-text p {
            margin-top: 20px; line-height: 1.6; color: #ccc;
        }

        .btn {
            display: inline-block; margin-top: 20px; padding: 12px 28px;
            background: #7cf03d; color: #1f242d; border-radius: 6px;
            font-weight: bold; text-decoration: none; transition: 0.3s;
            box-shadow: 0 0 15px #7cf03d, 0 0 30px #7cf03d;
        }
        .btn:hover {
            background: #5bbf2e;
            box-shadow: 0 0 20px #7cf03d, 0 0 40px #7cf03d;
        }

        .social-icons { margin-top: 20px; }
        .social-icons a {
            display: inline-block; margin-right: 15px; font-size: 20px;
            color: #7cf03d; transition: 0.3s;
        }
        .social-icons a:hover { color: #fff; }

        .home-img { position: relative; animation: fadeIn 2s ease-in-out; }
        .circle-border {
            width: 300px; height: 300px;
            border: 4px solid transparent; border-radius: 50%;
            border-top-color: #7cf03d; border-right-color: #7cf03d;
            position: absolute; top: 0; left: 0;
            animation: rotateCircle 5s linear infinite;
        }
        .circle-img {
            width: 260px; height: 260px; border-radius: 50%;
            object-fit: cover; position: relative; z-index: 1;
            margin: 20px;
        }

        @keyframes rotateCircle {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @media (max-width: 900px) {
            .home { flex-direction: column; text-align: center; padding-top: 140px; }
            .home-text { max-width: 100%; }
            .home-text h1 { font-size: 36px; }
            .home-text h3 { font-size: 20px; }
            .home-img { margin-top: 30px; }
            .circle-border { width: 250px; height: 250px; }
            .circle-img { width: 210px; height: 210px; margin: 20px; }
            .navbar ul { display: none; }
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <div class="logo">Portfolio.</div>
        <ul>
            <li><a href="#" class="active">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Portfolio</a></li>
            <li><a href="#">Service</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <section class="home">
        <div class="home-text">
            <h1>Mashal Roghani</h1>
            <h3>I'm a <span id="roleText">Frontend Developer</span></h3>
            <p>
                As a passionate freelance UI/UX designer and frontend developer, I craft visually stunning and intuitive digital experiences.
                My expertise blends creative design with clean, responsive code to ensure every project is both beautiful and user-friendly.
            </p>
            <a href="mashal resume.pptx" class="btn">Download CV</a>
            <div class="social-icons">
                <a href="https://facebook.com" target="_blank"><i class="fab fa-facebook"></i></a>
                <a href="https://instagram.com" target="_blank"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="linkdin/mashal"></i></a>
                <a href="#"><i class=""></i></a>
            </div>
        </div>

        <div class="home-img">
            <div class="circle-border"></div>
            <img src="mashal portfolio.jpg" alt="Profile Picture" class="circle-img">
        </div>
    </section>

    <script>
        const roleText = document.getElementById("roleText");
        let isFrontend = true;

        roleText.addEventListener("click", () => {
            roleText.textContent = isFrontend ? "UI/UX Designer" : "Frontend Developer";
            isFrontend = !isFrontend;
        });
    </script>
</body>
</html>
