<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Bhuvanesh | Developer</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link
    href="https://fonts.googleapis.com/css2?family=Google+Sans+Flex:opsz,wght@6..144,1..1000&family=Google+Sans:ital,opsz,wght,GRAD@0,17..18,400..700,-50;1,17..18,400..700,-50&display=swap"
    rel="stylesheet"
  >

  <style>
    html,
    body {
      margin: 0;
      padding: 0;
      width: 100%;
      min-height: 100%;
    }

    body {
      background-color: #000;

      /* BLACK GRID + WHITE LINES */
      background-image:
        linear-gradient(
          rgba(255, 255, 255, 0.12) 1px,
          transparent 1px
        ),
        linear-gradient(
          90deg,
          rgba(255, 255, 255, 0.12) 1px,
          transparent 1px
        );

      background-size: 32px 32px;
      background-position: center top;

      color: #fff;
      font-family: 'Google Sans', sans-serif;

      text-align: center;
    }

    .content {
      width: 100%;
      padding: 40px 20px;
    }

    .typing img {
      max-width: 100%;
      height: auto;
    }

    .section-title {
      font-family: 'Google Sans Flex', sans-serif;
      font-weight: 600;
      color: #fff;
      letter-spacing: 1px;
      margin-top: 30px;
    }

    .tech-stack {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
      gap: 18px;
      margin-top: 20px;
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
  </style>
</head>

<body>

  <div class="content">

    <!-- TYPING ANIMATION -->

    <div class="typing">

      <img
        src="https://readme-typing-svg.herokuapp.com?font=Google+Sans&size=38&duration=3000&pause=1000&color=FFFFFF&center=true&vCenter=true&width=500&lines=Hello+World!_;I+am+Bhuvanesh!_;Developer!_;"
        alt="Typing Animation"
      >

    </div>


    <!-- TECH STACK -->

    <h2 class="section-title">
      Tech Stack
    </h2>

    <div class="tech-stack">

      <img
        src="https://skillicons.dev/icons?i=java"
        height="55"
        alt="Java"
      >

      <img
        src="https://skillicons.dev/icons?i=html"
        height="55"
        alt="HTML"
      >

      <img
        src="https://skillicons.dev/icons?i=css"
        height="55"
        alt="CSS"
      >

      <img
        src="https://skillicons.dev/icons?i=js"
        height="55"
        alt="JavaScript"
      >

      <img
        src="https://skillicons.dev/icons?i=python"
        height="55"
        alt="Python"
      >

      <img
        src="https://skillicons.dev/icons?i=nodejs"
        height="55"
        alt="Node.js"
      >

      <img
        src="https://skillicons.dev/icons?i=mysql"
        height="55"
        alt="MySQL"
      >

      <img
        src="https://skillicons.dev/icons?i=flutter"
        height="55"
        alt="Flutter"
      >

      <img
        src="https://skillicons.dev/icons?i=git"
        height="55"
        alt="Git"
      >

    </div>


    <!-- SUPPORT MY WORK -->

    <div class="support">

      <h2 class="section-title">
        Support My Work
      </h2>

      <a
        href="https://buymeacoffee.com/bhuvaneshh"
        target="_blank"
        rel="noopener noreferrer"
      >

        <img
          src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png"
          alt="Buy Me A Coffee"
          style="
            height:60px !important;
            width:217px !important;
            border-radius:12px !important;
          "
        >

      </a>

    </div>

  </div>

</body>
</html>
