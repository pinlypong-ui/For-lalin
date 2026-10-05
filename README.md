# For-lalin
Index.html
<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>คำอวยพร 💜</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Itim&family=Mitr:wght@400;500&display=swap');

* {
    box-sizing: border-box;
}

body {
    margin: 0;
    min-height: 100vh;
    overflow: hidden;
    font-family: 'Mitr', sans-serif;
    background: linear-gradient(135deg, #faf7ff, #eee2ff, #ffffff);
    color: #5b3b7d;
    display: flex;
    justify-content: center;
    align-items: center;
}

/* กล่องหลัก */
.container {
    position: relative;
    width: min(90%, 430px);
    min-height: 620px;
    padding: 45px 25px;
    border: 3px solid rgba(150, 105, 200, .35);
    border-radius: 28px;
    background: rgba(255,255,255,.78);
    box-shadow:
        0 15px 50px rgba(120, 75, 170, .18),
        inset 0 0 30px rgba(180,140,230,.12);
    backdrop-filter: blur(8px);
    overflow: hidden;
    text-align: center;
}

/* วิ้งพื้นหลัง */
.sparkle {
    position: absolute;
    color: #b994e8;
    font-size: 18px;
    opacity: .65;
    animation: floatSparkle linear infinite;
    pointer-events: none;
}

@keyframes floatSparkle {
    0% {
        transform: translateY(110vh) rotate(0deg);
        opacity: 0;
    }

    15% {
        opacity: .7;
    }

    85% {
        opacity: .7;
    }

    100% {
        transform: translateY(-120vh) rotate(360deg);
        opacity: 0;
    }
}

/* ไม้คฑาลอย */
.wand {
    position: absolute;
    font-size: 35px;
    opacity: .55;
    animation: wandFloat 5s ease-in-out infinite;
    pointer-events: none;
}

@keyframes wandFloat {
    0%,100% {
        transform: translateY(0) rotate(-12deg);
    }

    50% {
        transform: translateY(-25px) rotate(12deg);
    }
}

h1 {
    margin: 10px 0 5px;
    font-family: 'Itim', cursive;
    font-size: 38px;
    color: #70449a;
}

.subtitle {
    font-size: 14px;
    opacity: .65;
    margin-bottom: 35px;
}

/* ปุ่ม */
button {
    font-family: 'Mitr', sans-serif;
    border: none;
    cursor: pointer;
}

.receive {
    padding: 18px 28px;
    border-radius: 18px;
    background: linear-gradient(135deg, #9d6ed0, #75449e);
    color: white;
    font-size: 20px;
    font-weight: 500;
    box-shadow: 0 8px 25px rgba(117,68,158,.25);
    animation: pulseButton 1.5s ease-in-out infinite;
    transition: .25s;
}

.receive:hover {
    transform: scale(1.06);
}

@keyframes pulseButton {
    0%,100% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.08);
    }
}

/* ปุ่มไม่กด */
.nope {
    position: relative;
    margin-top: 35px;
    padding: 12px 20px;
    border-radius: 15px;
    background: #eee4f8;
    color: #74538e;
    transition: .2s;
}

/* พื้นที่คำอวยพร */
.message-area {
    margin-top: 35px;
    min-height: 230px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.message-box {
    display: none;
    position: relative;
    width: 100%;
    padding: 22px 18px;
    border: 2px solid #b994dc;
    border-radius: 20px;
    background: rgba(255,255,255,.85);
    box-shadow: 0 8px 25px rgba(130,90,170,.12);
    animation: messageAppear .65s ease;
    line-height: 1.8;
    font-size: 16px;
}

@keyframes messageAppear {
    0% {
        transform: scale(.5) translateY(20px);
        opacity: 0;
    }

    70% {
        transform: scale(1.08);
    }

    100% {
        transform: scale(1);
        opacity: 1;
    }
}

.message-wand {
    font-size: 48px;
    margin-bottom: 10px;
    animation: wandMagic .7s ease;
}

@keyframes wandMagic {
    0% {
        transform: translateY(30px) rotate(-30deg);
        opacity: 0;
    }

    60% {
        transform: translateY(-8px) rotate(15deg);
    }

    100% {
        transform: translateY(0) rotate(0);
        opacity: 1;
    }
}

/* ประกายตอนกด */
.magic {
    position: fixed;
    pointer-events: none;
    font-size: 25px;
    z-index: 999;
    animation: magicBurst .8s ease-out forwards;
}

@keyframes magicBurst {
    0% {
        transform: translate(0,0) scale(.2) rotate(0);
        opacity: 1;
    }

    100% {
        transform:
            translate(
                calc((var(--x) - .5) * 250px),
                calc((var(--y) - .5) * 250px)
            )
            scale(1.3)
            rotate(180deg);
        opacity: 0;
    }
}

/* GIF */
.gif-area {
    display: none;
    animation: gifAppear .8s ease;
}

.gif-area img {
    width: 100%;
    max-width: 330px;
    border-radius: 20px;
    box-shadow: 0 10px 30px rgba(100,60,130,.2);
}

@keyframes gifAppear {
    from {
        opacity: 0;
        transform: scale(.6);
    }

    to {
        opacity: 1;
        transform: scale(1);
    }
}

.hidden {
    display: none !important;
}
</style>
</head>

<body>

<div class="container">

    <!-- ของตกแต่งพื้นหลัง -->
    <div class="wand" style="left:8%; top:12%;">🪄</div>
    <div class="wand" style="right:8%; top:30%; animation-delay:1s;">🪄</div>
    <div class="wand" style="left:5%; bottom:15%; animation-delay:2s;">🪄</div>
    <div class="wand" style="right:7%; bottom:8%; animation-delay:3s;">🪄</div>

    <div class="sparkle" style="left:15%; animation-duration:7s;">✦</div>
    <div class="sparkle" style="left:35%; animation-duration:9s; animation-delay:2s;">✧</div>
    <div class="sparkle" style="left:60%; animation-duration:8s; animation-delay:1s;">⋆</div>
    <div class="sparkle" style="left:80%; animation-duration:10s; animation-delay:3s;">✦</div>
    <div class="sparkle" style="left:90%; animation-duration:6s; animation-delay:4s;">✧</div>

    <div id="intro">

        <h1>มีอะไรจะให้ 💜</h1>

        <div class="subtitle">
            กดดูสิ... ไม่กัดหรอก
        </div>

        <button class="receive" id="receiveBtn">
            กดเพื่อรับคำอวยพร
        </button>

        <br>

        <button class="nope" id="nopeBtn">
            ไม่กดหรอก ! ไม่อยากได้ !
        </button>

    </div>

    <div class="message-area">

        <div id="messageBox" class="message-box">
            <div id="wandIcon" class="message-wand">🪄</div>
            <div id="messageText"></div>
        </div>

        <div id="gifArea" class="gif-area">

            <!-- ใส่ลิงก์ GIF ตรง src="..." -->
            <img
                id="finalGif"
                src="ใส่ลิงก์ GIF ตรงนี้"
                alt="GIF"
            >

        </div>

    </div>

</div>


<script>

const receiveBtn = document.getElementById("receiveBtn");
const nopeBtn = document.getElementById("nopeBtn");
const messageBox = document.getElementById("messageBox");
const messageText = document.getElementById("messageText");
const wandIcon = document.getElementById("wandIcon");
const intro = document.getElementById("intro");
const gifArea = document.getElementById("gifArea");

let clickCount = 0;

const messages = [
    "ขอให้ทุกอย่างราบรื่น",

    "ทุกอย่างจะผ่านไปได้ด้วยดี<br>ขอให้มั่นใจ 👊🏻",

    "รักเด็กนะเว้ย เพราะงั้น<br>ขอให้ทุกอย่างโอเค<br>ขอให้เธอไม่กลัวเกินไป<br>ขอให้ปลอดภัย<br>ขอให้เธอไม่เจ็บมากเท่าที่ควรนะ !"
];


/* ปุ่มไม่กดจะหนี */
nopeBtn.addEventListener("mouseover", moveNope);
nopeBtn.addEventListener("touchstart", moveNope);

function moveNope(e) {

    e.preventDefault();

    const container = document.querySelector(".container");

    const maxX = container.clientWidth - nopeBtn.offsetWidth - 20;
    const maxY = container.clientHeight - nopeBtn.offsetHeight - 20;

    const x = Math.random() * maxX - container.clientWidth / 2 + 40;
    const y = Math.random() * maxY - container.clientHeight / 2 + 40;

    nopeBtn.style.transform =
        `translate(${x}px, ${y}px)`;
}


/* กดรับคำอวยพร */
receiveBtn.addEventListener("click", function(e) {

    createMagic(e.clientX, e.clientY);

    if (clickCount < messages.length) {

        messageText.innerHTML = messages[clickCount];

        messageBox.style.display = "block";

        /* รีเซ็ต animation */
        messageBox.style.animation = "none";
        wandIcon.style.animation = "none";

        void messageBox.offsetWidth;
        void wandIcon.offsetWidth;

        messageBox.style.animation =
            "messageAppear .65s ease";

        wandIcon.style.animation =
            "wandMagic .7s ease";

        clickCount++;

    } else {

        /* กดครั้งที่ 4 → GIF */
        createMagic(e.clientX, e.clientY);

        messageBox.style.display = "none";
        intro.classList.add("hidden");

        gifArea.style.display = "block";
    }

});


/* เอฟเฟกต์ประกาย */
function createMagic(x, y) {

    const symbols = ["✦","✧","⋆","✨","💫"];

    for(let i = 0; i < 14; i++) {

        const magic = document.createElement("span");

        magic.className = "magic";

        magic.innerText =
            symbols[Math.floor(Math.random() * symbols.length)];

        magic.style.left = x + "px";
        magic.style.top = y + "px";

        magic.style.setProperty(
            "--x",
            Math.random()
        );

        magic.style.setProperty(
            "--y",
            Math.random()
        );

        document.body.appendChild(magic);

        setTimeout(() => {
            magic.remove();
        }, 800);
    }
}

</script>

</body>
</html>
