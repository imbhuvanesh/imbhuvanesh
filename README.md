<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link
    href="https://fonts.googleapis.com/css2?family=Google+Sans+Flex:opsz,wght@6..144,1..1000&family=Google+Sans:ital,opsz,wght,GRAD@0,17..18,400..700,-50;1,17..18,400..700,-50&family=Nabla&family=Quicksand:wght@300..700&display=swap"
    rel="stylesheet"
  >

  <style>

    /* =====================================
       RESET
    ====================================== */

    * {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      min-height: 100vh;

      overflow-x: hidden;

      background: #000;

      color: #fff;

      font-family: "Google Sans", sans-serif;
    }


    /* =====================================
       HYPER VELOCITY BACKGROUND
    ====================================== */

    .velocity-bg {
      position: fixed;

      inset: 0;

      z-index: 0;

      overflow: hidden;

      background: #000;

      pointer-events: none;
    }


    /* =====================================
       SMOOTH MOVING GRID
    ====================================== */

    .grid {
      position: absolute;

      width: 300%;
      height: 300%;

      left: -100%;
      top: -100%;

      background-image:
        linear-gradient(
          rgba(255,255,255,0.16) 1px,
          transparent 1px
        ),
        linear-gradient(
          90deg,
          rgba(255,255,255,0.16) 1px,
          transparent 1px
        );

      background-size: 45px 45px;

      transform:
        perspective(700px)
        rotateX(62deg)
        scale(1.5);

      animation:
        hyperVelocity 5s linear infinite;

      will-change: transform;
    }


    @keyframes hyperVelocity {

      0% {

        transform:
          perspective(700px)
          rotateX(62deg)
          scale(1.5)
          translate3d(0, 0, 0);

      }

      100% {

        transform:
          perspective(700px)
          rotateX(62deg)
          scale(1.5)
          translate3d(0, 45px, 0);

      }

    }


    /* =====================================
       GRID FADE
    ====================================== */

    .velocity-overlay {

      position: absolute;

      inset: 0;

      background:
        radial-gradient(
          ellipse at center,
          transparent 0%,
          rgba(0,0,0,0.08) 35%,
          rgba(0,0,0,0.35) 65%,
          rgba(0,0,0,0.78) 100%
        );

    }


    /* =====================================
       CONTENT
    ====================================== */

    .content {

      position: relative;

      z-index: 2;

      width: 100%;

      min-height: 100vh;

      padding:
        70px
        20px
        100px;

      text-align: center;

    }


    /* =====================================
       TYPING
    ====================================== */

    .typing {

      font-family:
        "Google Sans Flex",
        sans-serif;

      font-size:
        clamp(34px, 6vw, 64px);

      font-weight: 650;

      letter-spacing: -1px;

      color: #fff;

      margin-bottom: 60px;

      min-height: 75px;

      text-shadow:
        0 0 20px
        rgba(255,255,255,0.12);

    }


    .cursor {

      display: inline-block;

      width: 3px;

      height: 0.9em;

      margin-left: 6px;

      background: #fff;

      vertical-align: middle;

      animation:
        blink 0.8s infinite;

    }


    @keyframes blink {

      50% {
        opacity: 0;
      }

    }


    /* =====================================
       SECTION TITLE
    ====================================== */

    .section-title {

      font-family:
        "Google Sans Flex",
        sans-serif;

      font-size: 25px;

      font-weight: 600;

      letter-spacing: 0.5px;

      color: #fff;

      margin:
        0 0 30px;

      text-shadow:
        0 0 15px
        rgba(255,255,255,0.12);

    }


    /* =====================================
       TECH STACK
    ====================================== */

    .tech-stack {

      display: flex;

      justify-content: center;

      align-items: center;

      flex-wrap: wrap;

      gap: 28px;

      max-width: 950px;

      margin: 0 auto;

    }


    /* =====================================
       ICON HOLDER
       NO BORDER
       NO OUTLINE
       NO BACKGROUND
    ====================================== */

    .tech-icon {

      position: relative;

      width: 75px;

      height: 75px;

      display: flex;

      align-items: center;

      justify-content: center;

      background: transparent;

      border: none;

      outline: none;

      box-shadow: none;

      cursor: pointer;

      user-select: none;

      transition:
        transform 0.25s ease;

    }


    .tech-icon:hover {

      transform:
        translateY(-7px)
        scale(1.08);

    }


    /* =====================================
       TECH IMAGE
    ====================================== */

    .tech-icon img {

      width: 55px;

      height: 55px;

      object-fit: contain;

      pointer-events: none;

      user-select: none;

      will-change:
        transform,
        opacity;

    }


    /* =====================================
       HIDDEN ICON
    ====================================== */

    .tech-icon.icon-hidden {

      pointer-events: none;

      transform: none;

    }


    .tech-icon.icon-hidden img {

      visibility: hidden;

      opacity: 0;

    }


    /* =====================================
       BURST PARTICLES
    ====================================== */

    .burst-particle {

      position: fixed;

      pointer-events: none;

      z-index: 9999;

      border-radius: 2px;

      background: #fff;

      box-shadow:
        0 0 8px
        rgba(255,255,255,0.9);

      will-change:
        transform,
        opacity;

    }


    /* =====================================
       BURST FLASH
    ====================================== */

    .burst-flash {

      position: fixed;

      pointer-events: none;

      z-index: 9998;

      width: 18px;

      height: 18px;

      border-radius: 50%;

      background: #fff;

      transform:
        translate(-50%, -50%)
        scale(0);

      box-shadow:
        0 0 20px #fff,
        0 0 50px
        rgba(255,255,255,0.8);

      animation:
        flashBurst 350ms
        ease-out
        forwards;

    }


    @keyframes flashBurst {

      0% {

        opacity: 1;

        transform:
          translate(-50%, -50%)
          scale(0.2);

      }

      30% {

        opacity: 0.9;

        transform:
          translate(-50%, -50%)
          scale(1);

      }

      100% {

        opacity: 0;

        transform:
          translate(-50%, -50%)
          scale(4);

      }

    }


    /* =====================================
       ICON REAPPEAR
    ====================================== */

    .icon-reappear {

      animation:
        iconReappear
        900ms
        cubic-bezier(.16,.8,.25,1);

    }


    @keyframes iconReappear {

      0% {

        opacity: 0;

        transform:
          scale(0.1)
          rotate(-25deg);

      }

      45% {

        opacity: 1;

        transform:
          scale(1.25)
          rotate(8deg);

      }

      75% {

        transform:
          scale(0.92)
          rotate(-3deg);

      }

      100% {

        opacity: 1;

        transform:
          scale(1)
          rotate(0);

      }

    }


    /* =====================================
       SUPPORT MY WORK
    ====================================== */

    .support {

      margin-top: 70px;

    }


    .support-title {

      font-family:
        "Quicksand",
        sans-serif;

      font-size: 25px;

      font-weight: 600;

      letter-spacing: 0.3px;

      color: #fff;

      margin-bottom: 22px;

      text-shadow:
        0 0 15px
        rgba(255,255,255,0.12);

    }


    /* =====================================
       BUY ME A COFFEE
    ====================================== */

    .coffee-button img {

      width: 217px;

      height: 60px;

      border-radius: 12px;

      transition:
        transform 0.25s ease,
        filter 0.25s ease;

    }


    .coffee-button:hover img {

      transform:
        translateY(-5px)
        scale(1.05);

      filter:
        brightness(1.08)
        drop-shadow(
          0 10px 25px
          rgba(255,255,255,0.15)
        );

    }


    /* =====================================
       MOBILE
    ====================================== */

    @media (max-width: 600px) {

      .content {

        padding:
          45px
          15px
          80px;

      }


      .tech-stack {

        gap: 18px;

      }


      .tech-icon {

        width: 65px;

        height: 65px;

      }


      .tech-icon img {

        width: 46px;

        height: 46px;

      }

    }

  </style>
</head>


<body>


  <!-- =====================================
       HYPER VELOCITY GRID
  ====================================== -->

  <div class="velocity-bg">

    <div class="grid"></div>

    <div class="velocity-overlay"></div>

  </div>


  <!-- =====================================
       MAIN CONTENT
  ====================================== -->

  <main class="content">


    <!-- ===================================
         TYPING
    ==================================== -->

    <div class="typing">

      <span id="typingText"></span>

      <span class="cursor"></span>

    </div>


    <!-- ===================================
         TECH STACK
    ==================================== -->

    <h2 class="section-title">
      Tech Stack
    </h2>


    <div class="tech-stack">


      <!-- Java -->

      <div class="tech-icon">

        <img
          src="https://skillicons.dev/icons?i=java"
          alt="Java"
        >

      </div>


      <!-- HTML -->

      <div class="tech-icon">

        <img
          src="https://skillicons.dev/icons?i=html"
          alt="HTML"
        >

      </div>


      <!-- CSS -->

      <div class="tech-icon">

        <img
          src="https://skillicons.dev/icons?i=css"
          alt="CSS"
        >

      </div>


      <!-- JavaScript -->

      <div class="tech-icon">

        <img
          src="https://skillicons.dev/icons?i=js"
          alt="JavaScript"
        >

      </div>


      <!-- Python -->

      <div class="tech-icon">

        <img
          src="https://skillicons.dev/icons?i=python"
          alt="Python"
        >

      </div>


      <!-- Node.js -->

      <div class="tech-icon">

        <img
          src="https://skillicons.dev/icons?i=nodejs"
          alt="Node.js"
        >

      </div>


      <!-- SQL -->

      <div class="tech-icon">

        <img
          src="https://skillicons.dev/icons?i=mysql"
          alt="SQL"
        >

      </div>


      <!-- Flutter -->

      <div class="tech-icon">

        <img
          src="https://skillicons.dev/icons?i=flutter"
          alt="Flutter"
        >

      </div>


      <!-- Git -->

      <div class="tech-icon">

        <img
          src="https://skillicons.dev/icons?i=git"
          alt="Git"
        >

      </div>


    </div>


    <!-- ===================================
         SUPPORT MY WORK
    ==================================== -->

    <div class="support">

      <h2 class="support-title">
        Support My Work
      </h2>


      <a
        class="coffee-button"
        href="https://buymeacoffee.com/bhuvaneshh"
        target="_blank"
        rel="noopener noreferrer"
      >

        <img
          src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png"
          alt="Buy Me A Coffee"
        >

      </a>

    </div>


  </main>


  <script>

    /* =====================================
       TYPING ANIMATION
    ====================================== */

    const typingText =
      document.getElementById(
        "typingText"
      );


    const phrases = [

      "Hello World!",

      "I am Bhuvanesh!",

      "Developer!"

    ];


    let phraseIndex = 0;

    let characterIndex = 0;

    let deleting = false;


    function typeEffect() {

      const phrase =
        phrases[phraseIndex];


      if (!deleting) {

        typingText.textContent =
          phrase.substring(
            0,
            characterIndex + 1
          );

        characterIndex++;


        if (
          characterIndex ===
          phrase.length
        ) {

          deleting = true;

          setTimeout(
            typeEffect,
            1600
          );

          return;

        }

      } else {

        typingText.textContent =
          phrase.substring(
            0,
            characterIndex - 1
          );

        characterIndex--;


        if (
          characterIndex === 0
        ) {

          deleting = false;

          phraseIndex =
            (phraseIndex + 1)
            % phrases.length;

        }

      }


      setTimeout(
        typeEffect,
        deleting ? 45 : 85
      );

    }


    typeEffect();


    /* =====================================
       ICON BURST SYSTEM
    ====================================== */

    const icons =
      document.querySelectorAll(
        ".tech-icon"
      );


    icons.forEach(icon => {

      let bursting = false;


      icon.addEventListener(
        "mouseenter",
        () => {

          if (bursting) return;


          bursting = true;


          const image =
            icon.querySelector(
              "img"
            );


          const rect =
            image.getBoundingClientRect();


          const centerX =
            rect.left +
            rect.width / 2;


          const centerY =
            rect.top +
            rect.height / 2;


          /* =================================
             FLASH
          ================================== */

          const flash =
            document.createElement(
              "div"
            );


          flash.className =
            "burst-flash";


          flash.style.left =
            `${centerX}px`;


          flash.style.top =
            `${centerY}px`;


          document.body.appendChild(
            flash
          );


          flash.addEventListener(
            "animationend",
            () => flash.remove()
          );


          /* =================================
             ICON BURST
          ================================== */

          image.animate(

            [

              {
                transform:
                  "scale(1)",

                opacity: 1

              },

              {
                transform:
                  "scale(1.5)",

                opacity: 1

              },

              {
                transform:
                  "scale(2)",

                opacity: 0

              }

            ],

            {

              duration: 180,

              easing:
                "cubic-bezier(.2,.8,.2,1)",

              fill: "forwards"

            }

          );


          /* =================================
             PARTICLES
          ================================== */

          const particleCount = 40;


          for (
            let i = 0;
            i < particleCount;
            i++
          ) {

            const particle =
              document.createElement(
                "div"
              );


            particle.className =
              "burst-particle";


            const size =
              3 +
              Math.random() * 6;


            particle.style.width =
              `${size}px`;


            particle.style.height =
              `${size}px`;


            particle.style.left =
              `${centerX}px`;


            particle.style.top =
              `${centerY}px`;


            document.body.appendChild(
              particle
            );


            const angle =
              Math.random() *
              Math.PI *
              2;


            const distance =
              60 +
              Math.random() *
              150;


            const x =
              Math.cos(angle) *
              distance;


            const y =
              Math.sin(angle) *
              distance;


            const rotation =
              Math.random() *
              720 -
              360;


            const scale =
              0.2 +
              Math.random() *
              1.4;


            const animation =
              particle.animate(

                [

                  {
                    transform:
                      "translate(-50%, -50%) scale(1) rotate(0deg)",

                    opacity: 1

                  },

                  {
                    transform:
                      `translate(
                        calc(-50% + ${x}px),
                        calc(-50% + ${y}px)
                      )
                      scale(${scale})
                      rotate(${rotation}deg)`,

                    opacity: 0

                  }

                ],

                {

                  duration:
                    450 +
                    Math.random() * 450,

                  easing:
                    "cubic-bezier(.12,.75,.25,1)",

                  fill: "forwards"

                }

              );


            animation.onfinish =
              () => {

                particle.remove();

              };

          }


          /* =================================
             HIDE ICON
          ================================== */

          setTimeout(
            () => {

              icon.classList.add(
                "icon-hidden"
              );


              image.style.opacity =
                "0";


              image.style.visibility =
                "hidden";

            },

            250
          );


          /* =================================
             REAPPEAR AFTER 15 SECONDS
          ================================== */

          setTimeout(
            () => {

              icon.classList.remove(
                "icon-hidden"
              );


              image.style.visibility =
                "visible";


              image.style.opacity =
                "0";


              image.classList.add(
                "icon-reappear"
              );


              image.addEventListener(

                "animationend",

                () => {

                  image.classList.remove(
                    "icon-reappear"
                  );


                  image.style.opacity =
                    "1";


                  image.style.transform =
                    "scale(1)";


                  bursting =
                    false;

                },

                {
                  once: true
                }

              );


            },

            15000
          );

        }

      );

    });

  </script>

</body>
</html>
