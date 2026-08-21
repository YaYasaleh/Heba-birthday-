
<html lang="ar" dir="rtl">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Happy Birthday هبه ❤️</title>

  <style>

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, sans-serif;
      background:
        radial-gradient(circle at 50% 0%, #32194d 0%, #12091d 45%, #050308 100%);
      color: white;
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      background:
        radial-gradient(circle at 15% 25%, rgba(175, 92, 255, .12), transparent 25%),
        radial-gradient(circle at 85% 70%, rgba(255, 82, 181, .10), transparent 28%);
      z-index: -2;
    }

    /* =========================
       النجوم
    ========================= */

    .stars {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: -1;
    }

    .star {
      position: absolute;
      width: 2px;
      height: 2px;
      background: white;
      border-radius: 50%;
      opacity: .7;
      animation: twinkle 3s infinite ease-in-out;
    }

    @keyframes twinkle {
      0%, 100% {
        opacity: .2;
      }

      50% {
        opacity: 1;
      }
    }

    /* =========================
       القلوب
    ========================= */

    .hearts {
      position: fixed;
      inset: 0;
      pointer-events: none;
      overflow: hidden;
      z-index: 20;
    }

    .heart {
      position: absolute;
      bottom: -30px;
      animation: floatHeart linear forwards;
      opacity: 0;
    }

    @keyframes floatHeart {

      0% {
        transform: translateY(0) scale(.7);
        opacity: 0;
      }

      15% {
        opacity: .8;
      }

      100% {
        transform: translateY(-110vh) scale(1.15) rotate(360deg);
        opacity: 0;
      }

    }

    /* =========================
       شاشة القفل
    ========================= */

    #lockScreen {
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 30px 20px;
    }

    .lock-content {
      width: 100%;
      max-width: 850px;
      animation: fadeUp 1.5s ease;
    }

    .lock-date {
      color: #d7a9ff;
      font-size: 17px;
      letter-spacing: 5px;
      margin-bottom: 25px;
    }

    .lock-title {
      font-size: clamp(38px, 8vw, 70px);
      line-height: 1.2;
      margin-bottom: 18px;

      background:
        linear-gradient(
          90deg,
          #fff,
          #e6c5ff,
          #ff9fd6
        );

      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .lock-subtitle {
      color: #ded1e7;
      font-size: clamp(17px, 3vw, 21px);
      line-height: 2;
      margin-bottom: 35px;
    }

    /* =========================
       العد التنازلي
    ========================= */

    .countdown {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 14px;
      max-width: 750px;
      margin: 30px auto;
    }

    .time {
      padding: 25px 10px;
      background: rgba(255,255,255,.055);
      border: 1px solid rgba(220,180,255,.15);
      border-radius: 22px;
      backdrop-filter: blur(10px);
    }

    .number {
      display: block;
      font-size: clamp(32px, 7vw, 55px);
      color: #e6b8ff;
      font-weight: bold;
    }

    .label {
      display: block;
      margin-top: 8px;
      color: #bdb0c6;
      font-size: 16px;
    }

    /* =========================
       كلمة السر
    ========================= */

    .password-box {
      max-width: 500px;
      margin: 35px auto 0;
      padding: 28px 25px;

      background: rgba(255,255,255,.055);
      border: 1px solid rgba(220,180,255,.15);
      border-radius: 25px;

      backdrop-filter: blur(12px);
    }

    .password-title {
      color: #e2b7ff;
      font-size: 20px;
      margin-bottom: 18px;
    }

    .password-form {
   display: flex;
      justify-content: center;
      gap: 10px;
      flex-wrap: wrap;
      direction: ltr;
    }

    #passwordInput {
      width: 250px;
      padding: 13px 16px;

      border: 1px solid rgba(220,180,255,.25);
      border-radius: 12px;

      background: rgba(0,0,0,.3);
      color: white;

      outline: none;
      font-size: 16px;
      text-align: center;
    }

    #passwordInput::placeholder {
      color: #9f91a8;
    }

    #passwordInput:focus {
      border-color: #c98cff;
      box-shadow: 0 0 20px rgba(190,120,255,.15);
    }

    #unlockButton {
      padding: 13px 23px;

      border: none;
      border-radius: 12px;

      background: #a96be8;
      color: white;

      font-size: 16px;
      cursor: pointer;

      transition: .3s;
    }

    #unlockButton:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 25px rgba(169,107,232,.3);
    }

    #errorMessage {
      display: none;
      margin-top: 15px;
      color: #ff9fc7;
      font-size: 14px;
    }

    /* =========================
       التلميح
    ========================= */

    #hint {
      display: none;
      margin-top: 28px;

      color: #e6b8ff;
      font-size: clamp(22px, 5vw, 30px);
      letter-spacing: 3px;

      direction: ltr;

      animation: fadeUp 1s ease;
    }

    #hint.show {
      display: block;
    }

    /* =========================
       المحتوى الأصلي
    ========================= */

    #siteContent {
      display: none;
    }

    #siteContent.unlocked {
      display: block;
      animation: fadeUp 1.2s ease;
    }

    /* =========================
       البداية
    ========================= */

    .hero {
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 30px 20px;
    }

    .hero-content {
      width: 100%;
      max-width: 850px;
      animation: fadeUp 1.5s ease;
    }

    @keyframes fadeUp {

      from {
        opacity: 0;
        transform: translateY(30px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }

    }

    .date {
      color: #d7a9ff;
      font-size: 17px;
      letter-spacing: 5px;
      margin-bottom: 25px;
    }

    .hero h1 {
      font-size: clamp(45px, 10vw, 90px);
      line-height: 1.2;
      margin-bottom: 20px;

      background:
        linear-gradient(
          90deg,
          #fff,
          #e6c5ff,
          #ff9fd6
        );

      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .happy {
      font-size: clamp(26px, 5vw, 42px);
      color: #f7eafa;
      margin-bottom: 30px;
    }

    .hero-message {
      font-size: clamp(18px, 3vw, 23px);
      line-height: 2;
      color: #ded1e7;
      max-width: 700px;
      margin: auto;
    }

    .scroll {
      margin-top: 65px;
      color: #d9a9ff;
      font-size: 17px;
      animation: bounce 2s infinite;
    }

    @keyframes bounce {

      0%, 100% {
        transform: translateY(0);
      }

      50% {
        transform: translateY(10px);
      }

    }

    /* =========================
       الأقسام
    ========================= */

    section {
      width: 100%;
      max-width: 1000px;
      margin: auto;
      padding: 90px 20px;
      text-align: center;
    }

    .section-title {
      font-size: clamp(30px, 6vw, 45px);
      color: #e2b7ff;
      margin-bottom: 15px;
    }

    .section-subtitle {
      color: #bcaec6;
      font-size: 18px;
      margin-bottom: 35px;
    }

    /* =========================
       الرسالة الأولى
    ========================= */

    .letter {
      max-width: 800px;
      margin: 40px auto 0;
      padding: 45px 35px;

      background: rgba(255,255,255,.075);
      border: 1px solid rgba(220,180,255,.15);
      border-radius: 28px;

      box-shadow: 0 20px 70px rgba(0,0,0,.3);

      color: #f4eaf8;
      font-size: 20px;
      line-height: 2.3;

      text-align: right;

      backdrop-filter: blur(12px);
    }

    /* ========================= 
    الصور
    ========================= */

    .gallery {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
      max-width: 900px;
      margin: 40px auto 0;
    }

    .photo {
      aspect-ratio: 1 / 1.15;
      border-radius: 28px;
      overflow: hidden;

      background: rgba(255,255,255,.04);

      border: 2px solid rgba(220,180,255,.18);

      box-shadow: 0 15px 45px rgba(0,0,0,.35);

      transition: .4s ease;
    }

    .photo:hover {
      transform: translateY(-8px) scale(1.02);
      box-shadow: 0 20px 55px rgba(190,120,255,.25);
    }

    .photo img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
      transition: .5s ease;
    }

    .photo:hover img {
      transform: scale(1.06);
    }

    /* =========================
       الفيديو
    ========================= */

    .video-container {
      margin-top: 40px;

      border-radius: 25px;
      overflow: hidden;

      background: #09060d;

      border: 1px solid rgba(220,180,255,.15);

      box-shadow: 0 20px 70px rgba(0,0,0,.4);
    }

    .video-container video {
      width: 100%;
      display: block;
      border-radius: 25px;
    }

    /* =========================
       الموسيقى
    ========================= */

    .music-player {
      position: fixed;
      bottom: 22px;
      left: 22px;

      z-index: 100;

      display: flex;
      align-items: center;
      gap: 10px;

      padding: 10px 15px;

      border-radius: 999px;

      background: rgba(25,15,35,.90);

      border: 1px solid rgba(220,180,255,.25);

      backdrop-filter: blur(12px);
    }

    .music-player button {
      border: none;
      background: #a96be8;
      color: white;

      width: 42px;
      height: 42px;

      border-radius: 50%;

      cursor: pointer;
      font-size: 17px;
    }

    .music-player span {
      font-size: 13px;
      color: #e4d4ec;
    }

    /* =========================
       الهدية
    ========================= */

    .gift-section {
      min-height: 90vh;

      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }

    .gift {
      font-size: 125px;
      cursor: pointer;
      margin: 35px 0;

      transition: .4s;
      user-select: none;
    }

    .gift:hover {
      transform: scale(1.12) rotate(-5deg);
    }

    .final-message {
      display: none;
      max-width: 750px;
      animation: fadeUp 1s ease;
    }

    .final-message.show {
      display: block;
    }

    .final-main {
      font-size: 23px;
      line-height: 2.2;
      color: #f5dff0;
    }

    .second-letter {
      margin-top: 40px;
      padding: 35px;

      background: rgba(255,255,255,.06);

      border: 1px solid rgba(220,180,255,.15);

      border-radius: 25px;

      color: #f4eaf8;

      font-size: 19px;
      line-height: 2.3;

      text-align: right;
    }

    .last-line {
      margin-top: 35px;

      color: #d7a9ff;

      font-size: 19px;
      line-height: 2;
    }

    footer {
      padding: 50px 20px;
      text-align: center;

      color: #776a80;
      font-size: 13px;
    }

    /* =========================
       الجوال
    ========================= */

    @media (max-width: 700px) {

      .countdown {
        grid-template-columns: repeat(2, 1fr);
      }

      .gallery {
        grid-template-columns: repeat(2, 1fr);
        gap: 14px;
      }

      .photo:last-child {
        grid-column: span 1;
      }

      .letter {
        padding: 28px 22px;
        font-size: 18px;
      }

      .gift {
        font-size: 95px;
      }

      .password-form {
        flex-direction: column;
        align-items: center;
      }

      #passwordInput {
        width: 100%;
        max-width: 300px;
      }

      #unlockButton {
        width: 100%;
        max-width: 300px;
      }

    }

  </style>
</head>


<body>

  <!-- النجوم -->
  <div class="stars"></div>

  <!-- القلوب -->
  <div class="hearts"></div>


  <!-- =====================================================
  شاشة القفل
  ====================================================== -->

  <div id="lockScreen">

    <div class="lock-content">

      <div class="lock-date">
        AUGUST 22
      </div>

      <h1 class="lock-title">
        ❤️ هبة ❤️
      </h1>

      <p class="lock-subtitle">
        شيء جميل ينتظرك...
        <br>
        لكن عليك الانتظار قليلًا.
      </p>


      <!-- العد التنازلي -->

      <div class="countdown">

        <div class="time">
          <span class="number" id="days">00</span>
          <span class="label">يوم</span>
        </div>

        <div class="time">
          <span class="number" id="hours">00</span>
          <span class="label">ساعة</span>
        </div>

        <div class="time">
          <span class="number" id="minutes">00</span>
          <span class="label">دقيقة</span>
        </div>

        <div class="time">
          <span class="number" id="seconds">00</span>
          <span class="label">ثانية</span>
        </div>

      </div>


      <!-- كلمة السر -->

      <div class="password-box">

        <div class="password-title">
          🔒 كلمة السر مطلوبة
        </div>

        <div class="password-form">

          <input
            type="password"
            id="passwordInput"
            placeholder="أدخل كلمة السر"
            autocomplete="off"
          >

          <button
            id="unlockButton"
            onclick="unlockSite()"
          >
            فتح ❤️
          </button>

        </div>

        <div id="errorMessage">
          كلمة السر غير صحيحة ❤️
        </div>

      </div>


      <!-- التلميح الذي يظهر عند انتهاء العد -->

      <div id="hint">
        I …….. you
      </div>

    </div>

  </div>


  <!-- =====================================================
       الموقع الأصلي بالكامل
       مخفي إلى أن يتم إدخال كلمة السر
  ====================================================== -->

  <div id="siteContent">


    <!-- البداية -->

    <section class="hero">

      <div class="hero-content">

        <div class="date">
          AUGUST 22
        </div>

        <h1>
          Happy Birthday هبه
        </h1>

        <div class="happy">
          Happy Birthday
        </div>

        <p class="hero-message">
          إلى أجمل شخص في العالم وأعلى هدية له
        </p>

        <div class="scroll">
          اسحب للأسفل ↓
        </div>

      </div>

    </section>


    <!-- العداد -->

    <section>

      <h2 class="section-title">
        اليوم الكبير 🎂
      </h2>

      <p class="section-subtitle">
        المتبقي على 22 أغسطس
      </p>

      <div class="countdown">

        <div class="time">
          <span class="number" id="siteDays">00</span>
          <span class="label">يوم</span>
        </div>

        <div class="time">
          <span class="number" id="siteHours">00</span>
          <span class="label">ساعة</span>
        </div>

        <div class="time">
          <span class="number" id="siteMinutes">00</span>
          <span class="label">دقيقة</span>
        </div>

        <div class="time">
          <span class="number" id="siteSeconds">00</span>
          <span class="label">ثانية</span>
        </div>

      </div>

    </section>


    <!-- الرسالة الأولى -->

    <section>

      <h2 class="section-title">
        رسالة لأجمل شخص في الدنيا 💌
      </h2>

      <div class="letter">

        <p>
          في يوم مثل هذا قبل سنوات ولدت أجمل إنسانة في الدنيا
        </p>

        <br>

        <p>
          فرح وسعادة وهبه لكل شخص حولها
        </p>

        <br>

        <p>
          كل عام وأنتِ بخير هبوشي، وأتمنى تكون سنواتك الجاية كلها سعادة وفرح وتحققي كل أهدافك
        </p>

      </div>

    </section>


    <!-- الصور -->

    <section>

      <h2 class="section-title">
        أجمل بنوتة في الدنيا 📸
      </h2>

      <div class="gallery">

        <div class="photo">
          <img
            src="IMG_20260811_113036_757.jpg"
            alt="هبه"
          >
        </div>

        <div class="photo">
          <img
            src="IMG_20260811_113036_724.jpg"
            alt="هبه"
          >
        </div>

        <div class="photo">
          <img
            src="IMG_20260811_113035_807.jpg"
            alt="هبه"
          >
        </div>

        <div class="photo">
          <img
            src="IMG_20260811_113036_518.jpg"
            alt="هبه"
          >
        </div>

        <div class="photo">
          <img
            src="IMG_20260811_113035_857.jpg"
            alt="هبه"
          >
        </div>

      </div>

    </section>


    <!-- الفيديو -->

    <section>

      <h2 class="section-title">
        for my baby
      </h2>

      <div class="video-container">

        <video controls playsinline>

          <source
            src="4_5778680816603241723.MP4"
            type="video/mp4"
          >

          المتصفح لا يدعم تشغيل الفيديو.

        </video>

      </div>

    </section>


    <!-- الهدية -->

    <section class="gift-section">

      <h2 class="section-title">
        One Last Thing...
      </h2>

      <div
        class="gift"
        onclick="openGift()"
        title="اضغط على الهدية"
      >
        🎁
      </div>

      <div
        id="finalMessage"
        class="final-message"
      >

        <div class="final-main">

          <p>
            كل عام وأنتِ بخير يا هبة.
          </p>

          <br>

          <p>
            أتمنى أن تكون هذه السنة أجمل من كل السنوات اللي قبلها،
            وأن تبقى ابتسامتك موجودة للأبد.
          </p>

        </div>


        <!-- الرسالة الثانية -->

        <div class="second-letter">

          <p>
            أحبك
          </p>

          <br>

          <p>
            أحبك أكثر من كل شيء، أنتِ أجمل شخص دخل حياتي.
          </p>

          <br>

          <p>
            من يوم تعرفت عليكِ وأنا حاس بالتغيير اللي صار في حياتي.
          </p>

          <br>

          <p>
            كل يوم وكل لحظة أقضيها معك تملأني فرح،
            وأتمنى دائمًا إن اللحظات ذي تدوم وأقدر أكون معك لآخر يوم.
          </p>

          <br>

          <p>
            أنتِ هبتي وأغلى شيء عندي.
          </p>

          <br>

          <p>
            مرة أحبك. ❤️
          </p>

        </div>


        <div class="last-line">
          وهذه هدية صغيرة ما هي إلا طريقة بسيطة أقول لك إنك شخص مميز.
        </div>

      </div>

    </section>


    <footer>
      ❤️
    </footer>


    <!-- الموسيقى -->

    <div class="music-player">

      <button
        onclick="toggleMusic()"
        id="musicButton"
      >
        ▶
      </button>

      <span>
        Heaven Can Wait
      </span>

      <audio
        id="backgroundMusic"
        loop
      >

        <source
          src="Michael-Jackson-Heaven-Can-Wait-Official-Audio-128Kbps-44KHz%20%281%29.mp3"
          type="audio/mpeg"
        >

      </audio>

    </div>

  </div>


  <!-- =====================================================
       JAVASCRIPT
  ====================================================== -->

  <script>


    /* =====================================================
       النجوم
    ===================================================== */

    const stars =
      document.querySelector(".stars");

    for (let i = 0; i < 100; i++) {

      const star =
        document.createElement("div");

      star.className =
        "star";

      star.style.left =
        Math.random() * 100 + "%";

      star.style.top =
        Math.random() * 100 + "%";

      star.style.animationDelay =
        Math.random() * 3 + "s";

      stars.appendChild(star);

    }


    /* =====================================================
       إعدادات القفل
    ===================================================== */

    /*
       22 أغسطس 2026
       الساعة 12:00 صباحًا
       بتوقيت تركيا UTC+3
    */

    const birthday =
      new Date(
        "2026-08-22T00:00:00+03:00"
      ).getTime();


    /*
       كلمة السر
    */

    const correctPassword =
      "I love you";


    /* =====================================================
       العد التنازلي لشاشة القفل
    ===================================================== */
function updateLockCountdown() {

      const now =
        new Date().getTime();

      const distance =
        birthday - now;


      /*
         إذا انتهى العد
      */

      if (distance <= 0) {

        document.getElementById("days").textContent =
          "00";

        document.getElementById("hours").textContent =
          "00";

        document.getElementById("minutes").textContent =
          "00";

        document.getElementById("seconds").textContent =
          "00";


        /*
           إظهار التلميح
        */

        document
          .getElementById("hint")
          .classList.add("show");


        return;

      }


      const days =
        Math.floor(
          distance /
          (1000 * 60 * 60 * 24)
        );


      const hours =
        Math.floor(
          (distance /
          (1000 * 60 * 60)) % 24
        );


      const minutes =
        Math.floor(
          (distance /
          (1000 * 60)) % 60
        );


      const seconds =
        Math.floor(
          (distance /
          1000) % 60
        );


      document.getElementById("days").textContent =
        String(days).padStart(2, "0");

      document.getElementById("hours").textContent =
        String(hours).padStart(2, "0");

      document.getElementById("minutes").textContent =
        String(minutes).padStart(2, "0");

      document.getElementById("seconds").textContent =
        String(seconds).padStart(2, "0");

    }


    /* =====================================================
       فتح الموقع بكلمة السر
    ===================================================== */

    function unlockSite() {

      const passwordInput =
        document.getElementById(
          "passwordInput"
        );

      const errorMessage =
        document.getElementById(
          "errorMessage"
        );

      const enteredPassword =
        passwordInput.value;


      /*
         التحقق من كلمة السر
      */

      if (
        enteredPassword ===
        correctPassword
      ) {

        /*
           إخفاء شاشة القفل
        */

        document.getElementById(
          "lockScreen"
        ).style.display = "none";


        /*
           إظهار الموقع الأصلي
        */

        document.getElementById(
          "siteContent"
        ).classList.add("unlocked");


        /*
           تشغيل قلوب الموقع
        */

        startHearts();

      } else {

        /*
           كلمة السر خاطئة
        */

        errorMessage.style.display =
          "block";

        passwordInput.value = "";

      }

    }


    /* =====================================================
       Enter لفتح الموقع
    ===================================================== */

    document
      .getElementById("passwordInput")
      .addEventListener(
        "keydown",
        function(event) {

          if (event.key === "Enter") {

            unlockSite();

          }

        }
      );


    /* =====================================================
       العد التنازلي داخل الموقع الأصلي
    ===================================================== */

    function updateSiteCountdown() {

      const now =
        new Date().getTime();

      const distance =
        birthday - now;


      if (distance <= 0) {

        document.getElementById(
          "siteDays"
        ).textContent = "00";

        document.getElementById(
          "siteHours"
        ).textContent = "00";

        document.getElementById(
          "siteMinutes"
        ).textContent = "00";

        document.getElementById(
          "siteSeconds"
        ).textContent = "00";

        return;

      }


      const days =
        Math.floor(
          distance /
          (1000 * 60 * 60 * 24)
        );


      const hours =
        Math.floor(
          (distance /
          (1000 * 60 * 60)) % 24
        );


      const minutes =
        Math.floor(
          (distance /
          (1000 * 60)) % 60
        );


      const seconds =
        Math.floor(
          (distance /
          1000) % 60
        );


      document.getElementById(
      "siteDays"
      ).textContent =
        String(days).padStart(2, "0");


      document.getElementById(
        "siteHours"
      ).textContent =
        String(hours).padStart(2, "0");


      document.getElementById(
        "siteMinutes"
      ).textContent =
        String(minutes).padStart(2, "0");


      document.getElementById(
        "siteSeconds"
      ).textContent =
        String(seconds).padStart(2, "0");

    }


    /* =====================================================
       تشغيل العدادات
    ===================================================== */

    updateLockCountdown();
    updateSiteCountdown();


    setInterval(
      updateLockCountdown,
      1000
    );


    setInterval(
      updateSiteCountdown,
      1000
    );


    /* =====================================================
       الهدية
    ===================================================== */

    function openGift() {

      document
        .getElementById("finalMessage")
        .classList.add("show");


      for (let i = 0; i < 25; i++) {

        setTimeout(
          createHeart,
          i * 70
        );

      }

    }


    /* =====================================================
       القلوب
    ===================================================== */

    function createHeart() {

      const heart =
        document.createElement("div");

      heart.className =
        "heart";

      heart.textContent =
        Math.random() > .5
          ? "❤️"
          : "💜";


      heart.style.left =
        Math.random() * 100 + "vw";


      heart.style.fontSize =
        (14 + Math.random() * 18) + "px";


      heart.style.animationDuration =
        (5 + Math.random() * 5) + "s";


      document
        .querySelector(".hearts")
        .appendChild(heart);


      setTimeout(
        () => heart.remove(),
        10000
      );

    }


    /*
       تشغيل القلوب فقط بعد فتح الموقع
    */

    let heartInterval = null;


    function startHearts() {

      if (heartInterval !== null) {
        return;
      }

      heartInterval =
        setInterval(
          createHeart,
          1200
        );

    }


    /* =====================================================
       الموسيقى
    ===================================================== */

    function toggleMusic() {

      const music =
        document.getElementById(
          "backgroundMusic"
        );

      const button =
        document.getElementById(
          "musicButton"
        );


      if (music.paused) {

        music.play()
          .then(() => {

            button.textContent =
              "❚❚";

          })
          .catch(() => {

            alert(
              "اضغط مرة ثانية لتشغيل الموسيقى."
            );

          });

      } else {

        music.pause();

        button.textContent =
          "▶";

      }

    }

  </script>

</body>

</html>
