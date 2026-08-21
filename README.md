<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Bhuvanesh | Developer</title>

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link
    href="https://fonts.googleapis.com/css2?family=Google+Sans+Flex:opsz,wght@6..144,1..1000&family=Google+Sans:ital,opsz,wght,GRAD@0,17..18,400..700,-50;1,17..18,400..700,-50&family=Nabla&family=Quicksand:wght@300..700&display=swap"
    rel="stylesheet"
  >

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      padding: 30px;
      background: #000;
      font-family: 'Google Sans', sans-serif;
      color: #fff;
    }

    .profile-container {
      max-width: 1000px;
      margin: auto;
      padding: 40px 25px;
      border-radius: 18px;

      /* ONLINE BLACK GRID IMAGE */
      background-image:
        url("https://background-patterns.co/templates/minimalistic-black-grid-pattern-with-thin-white-lines");

      background-color: #000;
      background-size: 32px 32px;
      background-position: center;
      background-repeat: repeat;

      border: 1px solid rgba(255,255,255,0.15);
    }

    .typing {
      margin: 0;
    }

    .typing img {
      max-width: 100%;
      height: auto;
    }

    .section-title {
      font-family: 'Google Sans Flex', sans-serif;
      font-size: 26px;
      font-weight: 600;
      letter-spacing: 1px;
      margin: 30px 0 20px;
    }

    .tech-stack {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      gap: 18px;
      max-width: 650px;
      margin: auto;
    }

    .tech-stack img {
      width: 55px;
      height: 55px;
      object-fit: contain;
    }

    .support {
      margin-top: 45px;
    }

    .coffee-button img {
      height: 60px !important;
      width: 217px !important;
      border-radius: 12px !important;
    }

    @media (max-width: 600px) {

      body {
        padding: 10px;
      }

      .profile-container {
        padding: 30px 15px;
      }

      .typing img {
        width: 100%;
      }

      .tech-stack {
        gap: 12px;
      }

      .tech-stack img {
        width: 45px;
        height: 45px;
      }

      .section-title {
        font-size: 22px;
      }
    }
  </style>
</head>

<body>

  <div class="profile-container" align="center">

    <!-- TYPING ANIMATION -->

    <h1 class="typing">
      <img
        src="https://readme-typing-svg.herokuapp.com?font=Google+Sans&size=38&duration=3000&pause=1000&color=FFFFFF&center=true&vCenter=true&width=500&lines=Hello+World!_;I+am+Bhuvanesh!_;Developer!_;"
        alt="Typing Animation"
      >
    </h1>


    <!-- TECH STACK -->

    <h2 class="section-title">
      Tech Stack
    </h2>

    <div class="tech-stack">

      <img
        src="https://skillicons.dev/icons?i=java"
        alt="Java"
      >

      <img
        src="https://skillicons.dev/icons?i=html"
        alt="HTML"
      >

      <img
        src="https://skillicons.dev/icons?i=css"
        alt="CSS"
      >

      <img
        src="https://skillicons.dev/icons?i=js"
        alt="JavaScript"
      >

      <img
        src="https://skillicons.dev/icons?i=python"
        alt="Python"
      >

      <img
        src="https://skillicons.dev/icons?i=nodejs"
        alt="Node.js"
      >

      <img
        src="https://skillicons.dev/icons?i=mysql"
        alt="MySQL"
      >

      <img
        src="https://skillicons.dev/icons?i=flutter"
        alt="Flutter"
      >

      <img
        src="https://skillicons.dev/icons?i=git"
        alt="Git"
      >

    </div>


    <!-- SUPPORT -->

    <div class="support">

      <h2 class="section-title">
        Support My Work
      </h2>

      <a
        href="https://buymeacoffee.com/bhuvaneshh"
        target="_blank"
        rel="noopener noreferrer"
        class="coffee-button"
      >

        <img
          src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png"
          alt="Buy Me A Coffee"
        >

      </a>

    </div>

  </div>

</body>
</html>
