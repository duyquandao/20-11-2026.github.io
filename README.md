# 20-11-2026.github.io

<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy 20/11 - Khoa Tin học</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: "Trebuchet MS", Arial, sans-serif;
    overflow: hidden;
    background: #ffe8f1;
}

#video {
    width: 100%;
    height: 100vh;
    height: 100dvh;
    position: relative;
    overflow: hidden;
    background: linear-gradient(
        135deg,
        #ffd6e7,
        #fff0b8,
        #d5f4ff,
        #efd9ff
    );
}

/* Ánh sáng nền */
#video::before {
    content: "";
    position: absolute;
    inset: 0;
    background:
        radial-gradient(circle at 20% 20%, #fff 0 3%, transparent 25%),
        radial-gradient(circle at 80% 70%, #fff 0 2%, transparent 25%);
    opacity: .6;
}

/* Các cảnh */
.scene {
    position: absolute;
    inset: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
    opacity: 0;
    visibility: hidden;
    transition: opacity 1s ease;
    z-index: 3;
}

.scene.active {
    opacity: 1;
    visibility: visible;
}

.scene h1 {
    font-size: clamp(30px, 7vw, 65px);
    line-height: 1.4;
    color: #e83e86;
    text-shadow: 3px 4px 0 #fff, 0 0 20px #fff;
    animation: bounce 1.5s ease;
}

.scene p {
    margin-top: 22px;
    max-width: 700px;
    color: #7b3d87;
    font-size: clamp(16px, 3vw, 23px);
    line-height: 1.7;
    animation: pop 1.5s ease;
}

.scene .sub {
    font-size: 16px;
    font-weight: bold;
    letter-spacing: 3px;
    color: #f28a27;
    margin-bottom: 22px;
}

@keyframes bounce {
    0% { transform: scale(.5); opacity: 0; }
    60% { transform: scale(1.1); opacity: 1; }
    100% { transform: scale(1); }
}

@keyframes pop {
    from { transform: translateY(25px); opacity: 0; }
    to { transform: translateY(0); opacity: 1; }
}

/* Hoa bay */
.flower {
    position: absolute;
    top: -70px;
    z-index: 2;
    pointer-events: none;
    animation: fall linear infinite;
    user-select: none;
}

@keyframes fall {
    0% {
        transform: translateY(-70px) rotate(0deg);
        opacity: 0;
    }
    10% { opacity: 1; }
    50% { transform: translateY(50vh) rotate(180deg) translateX(40px); }
    100% {
        transform: translateY(110vh) rotate(600deg) translateX(-40px);
        opacity: .8;
    }
}

/* Hoa trang trí bốn góc */
.corner {
    position: absolute;
    font-size: clamp(40px, 9vw, 85px);
    animation: wiggle 3s infinite ease-in-out;
    z-index: 4;
    pointer-events: none;
}

.c1 { top: 12px; left: 12px; }
.c2 { top: 12px; right: 12px; animation-delay: .5s; }
.c3 { bottom: 90px; left: 12px; animation-delay: 1s; }
.c4 { bottom: 90px; right: 12px; animation-delay: 1.5s; }

@keyframes wiggle {
    0%, 100% { transform: rotate(-12deg) scale(1); }
    50% { transform: rotate(12deg) scale(1.2); }
}

/* Tim và ngôi sao */
.sparkle {
    position: absolute;
    pointer-events: none;
    z-index: 2;
    animation: sparkle 3s ease-in-out infinite;
}

@keyframes sparkle {
    0%, 100% { opacity: .3; transform: scale(.7) rotate(0deg); }
    50% { opacity: 1; transform: scale(1.3) rotate(30deg); }
}

/* Nút điều khiển */
#controls {
    position: absolute;
    bottom: 22px;
    width: 100%;
    display: flex;
    justify-content: center;
    gap: 10px;
    z-index: 10;
    flex-wrap: wrap;
    padding: 0 10px;
}

button {
    border: none;
    background: linear-gradient(135deg, #ff65a3, #a66bff);
    color: white;
    padding: 12px 20px;
    border-radius: 30px;
    font-weight: bold;
    cursor: pointer;
    box-shadow: 0 5px 15px #e78bb7;
}

button:hover {
    transform: scale(1.08);
}

#timer {
    position: absolute;
    top: 15px;
    right: 15px;
    color: #b53b80;
    font-weight: bold;
    z-index: 10;
}

#progress {
    position: absolute;
    bottom: 0;
    left: 0;
    height: 5px;
    width: 0;
    background: #ff3f91;
    z-index: 11;
}

@media(max-width:480px) {
    .scene { padding: 18px; }
    .scene .sub { font-size: 12px; }
    button { padding: 10px 13px; font-size: 12px; }
}
</style>
</head>

<body>

<div id="video">

    <div class="corner c1">🌸</div>
    <div class="corner c2">🌻</div>
    <div class="corner c3">🌷</div>
    <div class="corner c4">🌺</div>

    <div id="timer">00:00 / 01:00</div>

    <!-- CẢNH 1 -->
    <section class="scene active">
        <div class="sub">🌷 THÁNG 11 ĐÃ VỀ 🌷</div>
        <h1>HAPPY<br>20 - 11! 💗</h1>
        <p>Ngập tràn yêu thương gửi đến những người lái đò đáng kính! 🌸</p>
    </section>

    <!-- CẢNH 2 -->
    <section class="scene">
        <div class="sub">🌼 GỬI NGƯỜI THẦY, NGƯỜI CÔ 🌼</div>
        <h1>NHỮNG BÔNG HOA<br>ĐẸP NHẤT 🌺</h1>
        <p>Có những người âm thầm gieo hạt giống tri thức, để hôm nay chúng em tự tin nở hoa trên hành trình của mình.</p>
    </section>

    <!-- CẢNH 3 -->
    <section class="scene">
        <div class="sub">💻 KHOA TIN HỌC – ĐHSP HUẾ 💻</div>
        <h1>CODE CÓ THỂ<br>CÓ BUG... 😆</h1>
        <p>Nhưng tình cảm và lòng biết ơn của chúng em dành cho thầy cô thì luôn chạy đúng chương trình! 💗</p>
    </section>

    <!-- CẢNH 4 -->
    <section class="scene">
        <div class="sub">🌻 NHỮNG NGƯỜI TRUYỀN CẢM HỨNG 🌻</div>
        <h1>CẢM ƠN<br>THẦY CÔ! 💐</h1>
        <p>Cảm ơn vì những bài giảng, những lời động viên, sự kiên nhẫn và cả những lần tận tình chỉ bảo chúng em.</p>
    </section>

    <!-- CẢNH 5 -->
    <section class="scene">
        <div class="sub">💖 MỘT CHÚT YÊU THƯƠNG 💖</div>
        <h1>CHÚC THẦY CÔ<br>LUÔN RẠNG RỠ! 🌷</h1>
        <p>Luôn mạnh khỏe, hạnh phúc, bình an và mãi giữ nụ cười trên bục giảng!</p>
    </section>

    <!-- CẢNH 6 -->
    <section class="scene">
        <div class="sub">🌸 TRI ÂN NGÀY 20/11 🌸</div>
        <h1>CHÚC MỪNG<br>NGÀY NHÀ GIÁO<br>VIỆT NAM! 🎉</h1>
        <p>Kính tặng quý thầy cô Khoa Tin học – Trường Đại học Sư phạm, Đại học Huế.</p>
        <p>💐 Yêu thương và biết ơn! 💐</p>
    </section>

    <div id="controls">
        <button id="playBtn">▶ PHÁT VIDEO</button>
        <button id="pauseBtn">Ⅱ TẠM DỪNG</button>
        <button id="restartBtn">↻ XEM LẠI</button>
    </div>

    <div id="progress"></div>
</div>

<audio id="music" loop>
    <source src="music.mp3" type="audio/mpeg">
</audio>

<script>
(function() {
    "use strict";

    const scenes = document.querySelectorAll(".scene");
    const music = document.getElementById("music");
    const timer = document.getElementById("timer");
    const progress = document.getElementById("progress");

    const playBtn = document.getElementById("playBtn");
    const pauseBtn = document.getElementById("pauseBtn");
    const restartBtn = document.getElementById("restartBtn");

    const flowers = [
        "🌸", "🌺", "🌷", "🌻", "🌼",
        "💐", "🌹", "💮", "🪷", "🌼"
    ];

    const starts = [0, 8, 20, 32, 43, 52];
    const total = 60;

    let elapsed = 0;
    let playing = false;
    let animationId = null;
    let startTime = 0;
    let lastScene = -1;

    // Tạo nhiều hoa bay
    const video = document.getElementById("video");

    for (let i = 0; i < 55; i++) {
        const flower = document.createElement("div");

        flower.className = "flower";
        flower.textContent =
            flowers[Math.floor(Math.random() * flowers.length)];

        flower.style.left = Math.random() * 100 + "%";
        flower.style.fontSize = (16 + Math.random() * 25) + "px";
        flower.style.animationDuration = (6 + Math.random() * 10) + "s";
        flower.style.animationDelay = (-Math.random() * 15) + "s";

        video.appendChild(flower);
    }

    // Tạo sao và trái tim
    const decorations = ["✨", "💖", "⭐", "💕", "🌟"];

    for (let i = 0; i < 25; i++) {
        const item = document.createElement("div");

        item.className = "sparkle";
        item.textContent =
            decorations[Math.floor(Math.random() * decorations.length)];

        item.style.left = Math.random() * 100 + "%";
        item.style.top = Math.random() * 100 + "%";
        item.style.fontSize = (12 + Math.random() * 20) + "px";
        item.style.animationDelay = Math.random() * 4 + "s";

        video.appendChild(item);
    }

    function showScene(index) {
        if (index === lastScene) return;

        scenes.forEach(function(scene) {
            scene.classList.remove("active");
        });

        scenes[index].classList.add("active");
        lastScene = index;
    }

    function getScene(seconds) {
        let index = 0;

        for (let i = 0; i < starts.length; i++) {
            if (seconds >= starts[i]) {
                index = i;
            }
        }

        return index;
    }

    function updateUI() {
        const seconds = Math.floor(elapsed);
        const minute = Math.floor(seconds / 60);
        const second = seconds % 60;

        timer.textContent =
            String(minute).padStart(2, "0") + ":" +
            String(second).padStart(2, "0") + " / 01:00";

        progress.style.width = (elapsed / total * 100) + "%";
    }

    function animate() {
        if (!playing) return;

        elapsed = Math.min(
            (Date.now() - startTime) / 1000,
            total
        );

        showScene(getScene(elapsed));
        updateUI();

        if (elapsed >= total) {
            finish();
            return;
        }

        animationId = requestAnimationFrame(animate);
    }

    function play() {
        if (playing) return;

        if (elapsed >= total) {
            elapsed = 0;
            lastScene = -1;
        }

        playing = true;
        startTime = Date.now() - elapsed * 1000;

        music.play().catch(function(error) {
            console.log("Không phát được nhạc:", error);
        });

        playBtn.textContent = "▶ ĐANG PHÁT";

        animationId = requestAnimationFrame(animate);
    }

    function pause() {
        playing = false;

        if (animationId !== null) {
            cancelAnimationFrame(animationId);
            animationId = null;
        }

        music.pause();
        playBtn.textContent = "▶ TIẾP TỤC";
    }

    function finish() {
        pause();

        elapsed = total;
        showScene(5);
        updateUI();

        playBtn.textContent = "▶ PHÁT LẠI";
    }

    function restart() {
        pause();

        elapsed = 0;
        lastScene = -1;

        music.currentTime = 0;

        showScene(0);
        updateUI();

        play();
    }

    playBtn.addEventListener("click", play);
    pauseBtn.addEventListener("click", pause);
    restartBtn.addEventListener("click", restart);

    updateUI();

})();
</script>

</body>
</html>
