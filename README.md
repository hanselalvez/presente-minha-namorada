
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#39206b">

<title>Para minha Milena 💙❤️</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    min-height: 100vh;
    font-family: "Trebuchet MS", Arial, sans-serif;
    color: white;
    text-align: center;
    overflow-x: hidden;

    background:
        linear-gradient(
            135deg,
            rgba(15, 70, 200, 0.82),
            rgba(190, 15, 65, 0.80),
            rgba(75, 20, 160, 0.84)
        ),
        url("https://scontent.fmvf1-1.fna.fbcdn.net/v/t1.15752-9/862818627_2326334318142164_3173047491829448641_n.png?_nc_cat=101&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=9f807c&_nc_ohc=MjKFgF66anwQ7kNvwH4kwPA&_nc_oc=AdpQP27mD2a2l7cp3rMeFHgFoAZbGD5xO2pMH-eNfDr6pNmmR4qa4nw4vPJLAKcrlwuueTXAWY_ePUY2S4k5aNEy&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent.fmvf1-1.fna&_nc_ss=7a22e&oh=03_Q7cD6gFjyBH9obEc7WRhipZHrAewUj3Pw-s7Cu3qkEWlLwtboA&oe=6B044B04");

    background-size: auto, 180px;
    background-repeat: no-repeat, repeat;
    background-attachment: fixed;
}

.container {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 24px 15px;
}

.card {
    position: relative;
    z-index: 1;
    width: 100%;
    max-width: 520px;
    padding: 30px 22px;

    border: 2px solid rgba(255,255,255,0.6);
    border-radius: 28px;
    background: rgba(25, 15, 65, 0.88);
    box-shadow: 0 0 35px rgba(255, 70, 160, 0.45);
    backdrop-filter: blur(8px);

    animation: aparecer 1s ease;
}

h1 {
    font-size: clamp(28px, 7vw, 42px);
    margin-bottom: 10px;
}

p {
    font-size: 17px;
    line-height: 1.7;
}

.heart {
    font-size: 55px;
    display: inline-block;
    animation: pulsar 1.3s infinite;
}

.question {
    font-size: clamp(22px, 5.5vw, 30px);
    font-weight: bold;
    line-height: 1.5;
    margin: 25px 0;
}

button {
    border: none;
    border-radius: 30px;
    padding: 15px 22px;
    margin: 8px;
    font-size: 16px;
    font-weight: bold;
    font-family: inherit;
    cursor: pointer;
    touch-action: manipulation;
}

button:active {
    transform: scale(0.96);
}

.yes {
    color: white;
    background: linear-gradient(135deg, #ff3c83, #e00048);
    box-shadow: 0 4px 15px #ff3c8370;
    transition: transform 0.2s;
}

.think {
    color: #35204f;
    background: white;
    transform-origin: center;
    transition:
        transform 0.35s ease,
        opacity 0.35s ease,
        padding 0.35s ease,
        margin 0.35s ease;
}

.think:hover {
    background: #ffe1ed;
}

.music {
    color: white;
    background: linear-gradient(135deg, #147bff, #6545e8);
}

#answer {
    display: none;
    margin-top: 25px;
    padding: 18px;
    border-radius: 18px;
    background: rgba(255,255,255,0.12);
    animation: aparecer 0.8s ease;
}

.floating-heart {
    position: fixed;
    bottom: -45px;
    pointer-events: none;
    z-index: 0;
    animation: subir linear forwards;
}

footer {
    font-size: 13px;
    opacity: 0.9;
    margin-top: 25px;
}

@keyframes pulsar {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.18); }
}

@keyframes aparecer {
    from {
        opacity: 0;
        transform: translateY(15px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes subir {
    to {
        transform: translateY(-115vh) rotate(360deg);
        opacity: 0;
    }
}

@media (max-width: 400px) {
    .card {
        padding: 25px 15px;
    }

    button {
        max-width: 100%;
    }
}

@media (prefers-reduced-motion: reduce) {
    .heart {
        animation: none;
    }

    .floating-heart {
        animation-duration: 0.01ms !important;
    }
}
</style>
</head>

<body>

<div class="container">
    <main class="card">

        <div class="heart">💙❤️</div>

        <h1>Para minha Milena</h1>

        <p>
            Nesse mundo tem uma pessoa muito especial
	        Uma pessoa que faz meu coração bater mais forte
	        Alguém que faz meus dias terem mais cores.
        </p>

        <p> Essa pessoa é você, Miñly! 💖</p>

        <p>
            Se eu pudesse escolher alguém para acompanhar
            minhas histórias, minhas loucuras, meus sonhos
            e até os dias difíceis...
            Eu escolheria você.
            Hoje, amanhã e sempre.
        </p>

        </p>

        <div class="question">
            Milena, você aceita passar o resto da sua vida
            comigo? 💍
        </div>

        <button class="yes" onclick="responderSim()">
            SIM, MEU AMOR! 💖
        </button>

        <br>

        <button
            class="think"
            id="botaoPensar"
            onclick="diminuirBotao()"
        >
            Quero pensar, amor 🥺
        </button>

        <div id="answer" aria-live="polite"></div>

        <hr style="border-color:#ffffff40; margin:25px 0;">

        <p>🎵 Uma música para nós dois</p>

        <button class="music" onclick="tocarMusica()">
            ▶ Ouvir música que eu te dediquei
        </button>

        <p style="font-size:14px;">
            Escolhido com muito amor, especialmente para você.
        </p>

        <footer>
            Você é meu pedacinho favorito do universo. 🪐💗
        </footer>

    </main>
</div>

<script>
let cliquesPensar = 0;

function diminuirBotao() {
    const botao = document.getElementById("botaoPensar");

    cliquesPensar++;

    const escala = Math.max(0, 1 - cliquesPensar * 0.20);

    botao.style.transform = `scale(${escala})`;
    botao.style.opacity = escala;
    botao.style.pointerEvents = "none";

    if (cliquesPensar >= 5) {
        botao.style.display = "none";
    } else {
  
        setTimeout(() => {
            if (botao.style.display !== "none") {
                botao.style.pointerEvents = "auto";
            }
        }, 360);
    }
}

function responderSim() {
    const answer = document.getElementById("answer");

    answer.style.display = "block";

    answer.innerHTML = `
        <div style="font-size:42px">💍💖😭</div>
        <h2>EU TE AMO, MILENA!</h2>
        <p>VOCÊ DISSE SIM! ❤️💙</p>
        <p>
            Quero contar tantas histórias para você, tantas que
            sua mente iria se perder em meio as páginas delas.
        </p>
        <p>
            Obrigado por existir, meu amor.
            Quero continuar sendo a pessoa que você
            sempre escolherá hoje e sempre. 🪐
        </p>
        <div style="font-size:30px">
            💙❤️💗💕💖
        </div>
    `;

    criarChuvaDeCoracoes(55);

    answer.scrollIntoView({
        behavior: "smooth",
        block: "nearest"
    });
}

function tocarMusica() {
    window.open(
        "https://music.youtube.com/watch?v=gset79KMmt0&si=9b0pf1CX2lQzyYn3",
        "_blank"
    );
}

function criarChuvaDeCoracoes(quantidade) {
    const simbolos = ["❤️", "💙", "💖", "💕", "💗", "💘"];

    for (let i = 0; i < quantidade; i++) {
        setTimeout(() => {
            const heart = document.createElement("div");

            heart.className = "floating-heart";
            heart.textContent =
                simbolos[Math.floor(Math.random() * simbolos.length)];

            heart.style.left = Math.random() * 100 + "vw";
            heart.style.fontSize =
                (18 + Math.random() * 25) + "px";
            heart.style.animationDuration =
                (3 + Math.random() * 4) + "s";

            document.body.appendChild(heart);

            setTimeout(() => heart.remove(), 7500);
        }, i * 70);
    }
}

setInterval(() => {
    const heart = document.createElement("div");
    const simbolos = ["❤️", "💙", "💕", "💗"];

    heart.className = "floating-heart";
    heart.textContent =
        simbolos[Math.floor(Math.random() * simbolos.length)];

    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize =
        (16 + Math.random() * 20) + "px";
    heart.style.animationDuration =
        (5 + Math.random() * 4) + "s";

    document.body.appendChild(heart);

    setTimeout(() => heart.remove(), 10000);
}, 650);
</script>

</body>
</html>
