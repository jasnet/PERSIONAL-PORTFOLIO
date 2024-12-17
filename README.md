<!-- # Personal Portfolio -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Portfolio Website</title>
    <link rel="stylesheet" href="style2.css">
    <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
    <style>
        :root {
            --main-color: #0ef;
            --bg-color: #1f242d;
            --text-color: #fff;
            --hover-color: rgba(0, 238, 255, .2);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background: var(--bg-color);
            color: var(--text-color);
        }

        .header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            padding: 20px 10%;
            background: transparent;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 100;
        }

        .logo {
            font-size: 25px;
            color: var(--text-color);
            text-decoration: none;
            font-weight: 600;
            cursor: default;
            opacity: 0;
            animation: slideRight 1s ease forwards;
        }

        .navbar a {
            display: inline-block;
            font-size: 18px;
            color: var(--text-color);
            text-decoration: none;
            font-weight: 500;
            margin-left: 35px;
            transition: .3s;
            opacity: 0;
            animation: slideTop .5s ease forwards;
            animation-delay: calc(.2s * var(--i));
        }

        .navbar a:hover,
        .navbar a.active {
            color: var(--main-color);
        }

        .home {
            position: relative;
            width: 100%;
            height: 100vh;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 70px 10% 0;
        }

        .home-content {
            max-width: 600px;
        }

        .home-content h1 {
            font-size: 56px;
            font-weight: 700;
            margin: -3px 0;
            opacity: 0;
            animation: slideBottom 1s ease forwards;
            animation-delay: .7s;
        }

        .home-content h3 {
            font-size: 32px;
            font-weight: 700;
            opacity: 0;
            animation: slideBottom 1s ease forwards;
            animation-delay: .7s;
        }

        .home-content p {
            font-size: 16px;
            margin: 20px 0 40px;
            opacity: 0;
            animation: slideLeft 1s ease forwards;
            animation-delay: 1s;
        }

        .btn-box {
            display: flex;
            justify-content: space-between;
            width: 345px;
            height: 50px;
        }

        .btn-box a {
            position: relative;
            display: inline-flex;
            justify-content: center;
            align-items: center;
            width: 150px;
            height: 100%;
            background: var(--main-color);
            border: 2px solid var(--main-color);
            border-radius: 8px;
            font-size: 19px;
            color: var(--bg-color);
            text-decoration: none;
            font-weight: 600;
            letter-spacing: 1px;
            z-index: 1;
            overflow: hidden;
            transition: .5s;
            opacity: 0;
            animation: slideTop 1s ease forwards;
            animation-delay: 2s;
        }

        .btn-box a:hover {
            color: var(--main-color);
        }

        .btn-box a:nth-child(2) {
            background: transparent;
            color: var(--main-color);
        }

        .btn-box a:nth-child(2):hover {
            color: var(--bg-color);
        }

        .btn-box a:nth-child(2)::before {
            background: var(--main-color);
        }

        .btn-box a::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 100%;
            background: var(--bg-color);
            z-index: -1;
            transition: .5s;
        }

        .btn-box a:hover::before {
            width: 100%;
        }

        .home-sci {
            position: absolute;
            bottom: 40px;
            width: 170px;
            display: flex;
            justify-content: space-between;
        }

        .home-sci a {
            position: relative;
            display: inline-flex;
            justify-content: center;
            align-items: center;
            width: 40px;
            height: 40px;
            background: transparent;
            border: 2px solid var(--main-color);
            border-radius: 50%;
            font-size: 20px;
            color: var(--main-color);
            text-decoration: none;
            z-index: 1;
            overflow: hidden;
            transition: .5s;
            opacity: 0;
            animation: slideLeft 1s ease forwards;
            animation-delay: calc(.2s * var(--i));
        }

        .home-sci a:hover {
            color: var(--bg-color);
        }

        .home-sci a::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 100%;
            background: var(--main-color);
            z-index: -1;
            transition: .5s;
        }

        .home-sci a:hover::before {
            width: 100%;
        }

        .home-imgHover {
            position: absolute;
            top: 0;
            right: 30px;
            width: 500px;
            height: 100%;
            background: transparent;
            transition: 3s;
            animation: manipActiveHover .1s forwards;
            animation-delay: 4s;
            pointer-events: none;
        }

        .home-imgHover:hover {
            background: var(--bg-color);
            opacity: .8;
        }

        @keyframes slideRight {
            0% {
                transform: translateX(-100px);
                opacity: 0;
            }
            100% {
                transform: translateX(0);
                opacity: 1;
            }
        }

        @keyframes slideTop {
            0% {
                transform: translateY(100px);
                opacity: 0;
            }
            100% {
                transform: translateY(0);
                opacity: 1;
            }
        }

        @keyframes slideBottom {
            0% {
                transform: translateY(-100px);
                opacity: 0;
            }
            100% {
                transform: translateY(0);
                opacity: 1;
            }
        }

        @keyframes slideLeft {
            0% {
                transform: translateX(100px);
                opacity: 0;
            }
            100% {
                transform: translateX(0);
                opacity: 1;
            }
        }

        @keyframes manipActiveHover {
            100% {
                pointer-events: auto;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <a href="#" class="logo">Jasss.</a>

        <nav class="navbar">
            <a href="#" class="active" style="--i:1;">Home</a>
            <a href="#" style="--i:2;">About</a>
            <a href="#" style="--i:3;">Services</a>
            <a href="#" style="--i:4;">Portfolio</a>
            <a href="#" style="--i:5;">Contact</a>
        </nav>
    </header>

    <section class="home">
        <div class="home-content">
            <h1>Hi, I'm Jasneet Singh</h1>
            <h3>Frontend Developer</h3>
            <p>Front end developers are pivotal in web development. They are entrusted with the critical task of shaping websites' and web applications' user experience and interface. Their roles and responsibilities revolve around creating visually appealing, user-friendly, and responsive front end components.</p>
            <div class="btn-box">
                <label for="resume-upload" style="cursor: pointer;">
                    <a href="#" onclick="document.getElementById('resume-upload').click();">Hire Me</a>
                </label>
                <input type="file" id="resume-upload" style="display: none;" accept=".pdf,.doc,.docx">
                <a href="#">Let's Talk</a>
            </div>
        </div>
        <div class="home-sci">
            <a href="https://facebook.com/yourusername" style="--i:6;"><i class='bx bxl-facebook'></i></a>
            <a href="https://twitter.com/yourusername" style="--i:7;"><i class='bx bxl-twitter'></i></a>
            <a href="https://linkedin.com/in/yourusername" style="--i:8;"><i class='bx bxl-linkedin'></i></a>
            <a href="https://github.com/yourusername" style="--i:9;"><i class='bx bxl-github'></i></a>
        </div>
        <span class="home-imgHover"></span>
    </section>
</body>
</html>
