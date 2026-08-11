# Heba-birthday-
A special birthday website for me baby 
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Happy Birthday Heba ❤️</title>

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
      background: #0b0710;
      color: white;
      overflow-x: hidden;
    }

    /* خلفية */

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      background:
        radial-gradient(circle at 20% 20%, rgba(255, 75, 170, 0.18), transparent 30%),
        radial-gradient(circle at 80% 70%, rgba(150, 70, 255, 0.16), transparent 30%);
      pointer-events: none;
      z-index: -1;
    }

    /* قلوب */

    .hearts {
      position: fixed;
      inset: 0;
      pointer-events: none;
      overflow: hidden;
      z-index: 10;
    }

    .heart {
      position: absolute;
      bottom: -40px;
      animation: floatHeart linear forwards;
      opacity: 0;
    }

    @keyframes floatHeart {
      0% {
        transform: translateY(0) scale(0.7) rotate(0deg);
        opacity: 0;
      }

      15% {
        opacity: 0.8;
      }

      100% {
        transform: translateY(-110vh) scale(1.2) rotate(360deg);
        opacity: 0;
      }
    }

    /* الصفحة الرئيسية */

    .hero {
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 30px 20px;
      position: relative;
    }

    .hero-content {
      max-width: 800px;
      animation: appear 1.5s ease;
    }

    @keyframes appear {
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
      color: #ff9dcc;
      font-size: 18px;
      letter-spacing: 3px;
      margin-bottom: 25px;
    }

    h1 {
      font-size: clamp(55px, 13vw, 120px);
      font-weight: 800;
      background: linear-gradient(
        90deg,
        #ffffff,
        #ffb1db,
        #ff65b4
      );
      -webkit-background-clip: text;
      color: transparent;
      margin-bottom: 15px;
    }

    .birthday {
      font-size: clamp(25px, 5vw, 42px);
      margin-bottom: 25px;
    }

    .intro {
      color: #d9c6d5;
      font-size: 20px;
      line-height: 1.9;
      max-width: 600px;
      margin: auto;
    }

    .scroll {
      margin-top: 60px;
      color: #ff9dcc;
      font-size: 15px;
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

    /* العد التنازلي */

    .countdown-section {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 60px 20px;
      text-align: center;
    }

    .section-title {
      font-size: 36px;
      color: #ffabd8;
      margin-bottom: 15px;
    }

    .section-text {
      color: #cdbdca;
      font-size: 18px;
      margin-bottom: 35px;
    }

    .countdown {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 15px;
      width: min(700px, 100%);
    }

    .time {
      padding: 25px 10px;
      border-radius: 22px;
      background: rgba(255,255,255,0.06);
      border: 1px solid rgba(255,255,255,0.1);
      backdrop-filter: blur(10px);
    }

    .time-number {
      display: block;
      font-size: clamp(32px, 7vw, 55px);
      font-weight: bold;
      color: #ff8ec7;
    }

    .time-label {
      color: #bcaeb9;
      margin-top: 8px;
      display: block;
    }

    /* الرسالة */

    .letter-section {
      padding: 100px 20px;
      max-width: 900px;
      margin: auto;
    }

    .letter {
      margin-top: 35px;
      background: #fff9fc;
      color: #3a2634;
      padding: 45px 35px;
      border-radius: 8px;
      box-shadow: 0 20px 60px rgba(0,0,0,0.3);
      line-height: 2.3;
      font-size: 19px;
      text-align: right;
      transform: rotate(-0.5deg);
    }

    .letter-title {
      color: #c54283;
      font-size: 28px;
      margin-bottom: 25px;
    }

    .signature {
      margin-top: 30px;
      text-align: left;
      color: #c54283;
      font-size: 22px;
    }

    /* الصور */

    .gallery-section {
      padding: 100px 20px;
      max-width: 1000px;
      margin: auto;
      text-align: center;
    }

    .gallery-placeholder {
      margin-top: 35px;
      min-height: 300px;
      border: 2px dashed rgba(255,160,210,0.3);
      border-radius: 25px;
      display: flex;
      justify-content: center;
      align-items: center;
      color: #bcaeb9;
      font-size: 18px;
      padding: 30px;
    }

    /* الفيديو */

    .video-section {
      padding: 100px 20px;
      max-width: 900px;
      margin: auto;
      text-align: center;
    }

    .video-placeholder {
      margin-top: 35px;
      aspect-ratio: 16 / 9;
      border-radius: 25px;
      border: 2px dashed rgba(255,160,210,0.3);
      display: flex;
      justify-content: center;
      align-items: center;
      color: #bcaeb9;
      overflow: hidden;
    }

    /* الهدية */

    .gift-section {
      min-height: 80vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 60px 20px;
    }

    .gift {
      font-size: 120px;
      cursor: pointer;
      transition: 0.4s;
      margin: 30px 0;
    }

    .gift:hover {
      transform: scale(1.1) rotate(-5deg);
    }

    .final-message {
      display: none;
      max-width: 650px;
      font-size: 23px;
      line-height: 2;
      color: #ffd1e9;
      animation: appear 1s ease;
    }

    .final-message.show {
      display: block;
    }

    /* الفوتر */

    footer {
      text-align: center;
      padding: 40px 20px;
      color: #746775;
      font-size: 14px;
    }

    /* الجوال */

    @media (max-width: 600px) {

      .countdown {
        grid-template-columns: repeat(2, 1fr);
      }

      .letter {
        padding: 30px 22px;
        font-size: 17px;
      }

      .gift {
        font-size: 90px;
      }

    }

  </style>
</head>


<body>

  <div class="hearts"></div>


  <!-- البداية -->

  <section class="hero">

    <div class="hero-content">

      <div class="date">
        AUGUST 22
      </div>

      <h1>هبة</h1>

      <div class="birthday">
        Happy Birthday ❤️
      </div>

      <p class="intro">
        إلى الشخص اللي يستحق يوم كامل من الفرح،
        والكثير من الكلام الحلو،
        وهذه المساحة الصغيرة كلها لكِ.
      </p>

      <div class="scroll">
        ↓ اسحبي لتحت ↓
      </div>

    </div>

  </section>


  <!-- العد التنازلي -->

  <section class="countdown-section">

    <h2 class="section-title">
      يومك الكبير يقترب 🎂
    </h2>

    <p class="section-text">
      باقي على 22 أغسطس...
    </p>

    <div class="countdown">

      <div class="time">
        <span class="time-number" id="days">00</span>
        <span class="time-label">يوم</span>
      </div>

      <div class="time">
        <span class="time-number" id="hours">00</span>
        <span class="time-label">ساعة</span>
      </div>

      <div class="time">
        <span class="time-number" id="minutes">00</span>
        <span class="time-label">دقيقة</span>
      </div>

      <div class="time">
        <span class="time-number" id="seconds">00</span>
        <span class="time-label">ثانية</span>
      </div>

    </div>

  </section>


  <!-- الرسالة -->

  <section class="letter-section">

    <h2 class="section-title">
      رسالة لكِ 💌
    </h2>

    <div class="letter">

      <div class="letter-title">
        إلى هبة...
      </div>

      <p>
        في يوم مثل هذا، قبل سنوات، جاء شخص إلى العالم
        وصار وجوده بعد ذلك سببًا للكثير من اللحظات الجميلة.
      </p>

      <br>

      <p>
        أتمنى أن تكون سنتك الجديدة مليئة بالأيام التي
        تجعلك تبتسمين، وبالأشياء التي تتمنينها وتتحقق.
      </p>

      <br>

      <p>
      وهذا الموقع مجرد بداية...
        لأن عندي لكِ أشياء كثيرة لسه ما شفتيها ❤️
      </p>

      <div class="signature">
        لكِ دائمًا ❤️
      </div>

    </div>

  </section>


  <!-- الصور -->

  <section class="gallery-section">

    <h2 class="section-title">
      ذكرياتنا 📸
    </h2>

    <p class="section-text">
      هنا راح تكون صورنا الخمس.
    </p>

    <div class="gallery-placeholder">
      صور هبة راح تنضاف هنا لاحقًا ❤️
    </div>

  </section>


  <!-- الفيديو -->

  <section class="video-section">

    <h2 class="section-title">
      شيء أريدك أن تشاهديه 🎥
    </h2>

    <p class="section-text">
      فيديو التهنئة راح يكون هنا.
    </p>

    <div class="video-placeholder">
      فيديو التهنئة راح ينضاف هنا ❤️
    </div>

  </section>


  <!-- الهدية -->

  <section class="gift-section">

    <h2 class="section-title">
      One Last Thing...
    </h2>

    <p class="section-text">
      باقي شيء واحد فقط.
    </p>

    <div
      class="gift"
      onclick="openGift()"
      title="اضغطي على الهدية"
    >
      🎁
    </div>

    <div id="finalMessage" class="final-message">

      <p>
        كل عام وأنتِ بخير يا هبة ❤️
      </p>

      <br>

      <p>
        أتمنى أن تكون هذه السنة أجمل من كل السنوات
        اللي قبلها، وأن تبقى ابتسامتك موجودة دائمًا.
      </p>

      <br>

      <p>
        وهذه الهدية الصغيرة ما هي إلا طريقة بسيطة
        أقول لك فيها إنك شخص مميز جدًا. ✨
      </p>

    </div>

  </section>


  <footer>
    Made with love ❤️ for Heba
  </footer>


  <script>

    /*
      العد التنازلي
      22 أغسطس 2026 الساعة 12:00 AM
    */

    const birthday = new Date(
      "2026-08-22T00:00:00"
    ).getTime();


    function updateCountdown() {

      const now = new Date().getTime();

      const distance = birthday - now;

      if (distance <= 0) {

        document.getElementById("days").textContent = "00";
        document.getElementById("hours").textContent = "00";
        document.getElementById("minutes").textContent = "00";
        document.getElementById("seconds").textContent = "00";

        return;
      }


      const days = Math.floor(
        distance / (1000 * 60 * 60 * 24)
      );

      const hours = Math.floor(
        (distance / (1000 * 60 * 60)) % 24
      );

      const minutes = Math.floor(
        (distance / (1000 * 60)) % 60
      );

      const seconds = Math.floor(
        (distance / 1000) % 60
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


    updateCountdown();

    setInterval(updateCountdown, 1000);


    /*
      فتح الهدية
    */

    function openGift() {

      document
        .getElementById("finalMessage")
        .classList.add("show");

      for (let i = 0; i < 25; i++) {

        setTimeout(() => {
          createHeart();
        }, i * 80);

      }

    }


    /*
      القلوب المتحركة
    */

    function createHeart() {

      const heart =
        document.createElement("div");

      heart.className = "heart";

      heart.textContent =
        Math.random() > 0.5 ? "❤️" : "💕";

      heart.style.left =
        Math.random() * 100 + "vw";

      heart.style.fontSize =
        (14 + Math.random() * 18) + "px";

      heart.style.animationDuration =
        (5 + Math.random() * 5) + "s";

      document
        .querySelector(".hearts")
        .appendChild(heart);


      setTimeout(() => {
        heart.remove();
      }, 10000);

    }


    setInterval(createHeart, 1200);

  </script>

</body>
</html>
