# yessine-allemand
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>KUMAYA SPORT</title>
<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #0f172a;
    color: white;
    text-align: center;
}

header {
    padding: 50px;
    background: linear-gradient(90deg, #0ea5e9, #22c55e);
}

section {
    padding: 40px;
}

h1, h2 {
    margin-bottom: 20px;
}

.card {
    background: #1e293b;
    margin: 10px;
    padding: 20px;
    border-radius: 15px;
}

button {
    padding: 15px 25px;
    margin: 10px;
    border: none;
    border-radius: 10px;
    font-size: 16px;
    cursor: pointer;
}

.yes { background: #22c55e; }
.no { background: #ef4444; }

#overlay {
    position: fixed;
    top:0; left:0;
    width:100%;
    height:100%;
    display:none;
    align-items:center;
    justify-content:center;
    font-size:30px;
    text-align:center;
    z-index:999;
}

.glitch {
    animation: glitch 0.2s infinite;
}

@keyframes glitch {
    0% { transform: translate(2px, -2px); }
    25% { transform: translate(-2px, 2px); }
    50% { transform: translate(2px, 2px); }
    75% { transform: translate(-2px, -2px); }
    100% { transform: translate(0); }
}
</style>
</head>

<body>

<header>
<h1>KUMAYA SPORT</h1>
<p>Freundschaft • Sport • Spaß</p>
</header>

<section>
<h2>Über uns</h2>
<p>KUMAYA kommt von KUSS, MAAMARI und KHAYAT.</p>
<p>Ein Verein aus Freundschaft und Liebe zum Sport.</p>
<p>Hauptquartier: Vatican</p>
</section>

<section>
<h2>Städte</h2>
<div class="card">Strasbourg, Berlin, Paris, Damas, Tunis</div>
</section>

<section>
<h2>Team</h2>
<div class="card">Präsident: Baptiste</div>
<div class="card">Vizepräsident: Yessine</div>
<div class="card">Praktikum: Louis</div>
</section>

<section>
<h2>Trainer & Helfer</h2>
<p>Didier Deschamps • Jose Mourinho • Patrick Sébastien</p>
<p>Mit Hilfe von Cristiano Ronaldo & Lionel Messi</p>
</section>

<section>
<h2>Ziele</h2>
<p>Kinder helfen • Sport fördern • Teamarbeit • Respekt • Spaß</p>
</section>

<section>
<h2>Sponsoren</h2>
<p>Nike • MYM • Pampers • Vodka</p>
</section>

<section>
<h2>Maskottchen</h2>
<p>🐯 Ein sportlicher Tiger</p>
</section>

<section>
<h2>Schirmherr</h2>
<p>Khabib Nurmagomedov</p>
</section>

<section>
<h2>Avez-vous aimé le site ?</h2>
<button class="yes" onclick="likeSite()">Oui</button>
<button class="no" onclick="dislikeStep1()">Non</button>
</section>

<div id="overlay"></div>

<script>
function likeSite() {
    const o = document.getElementById("overlay");
    o.style.display = "flex";
    o.style.background = "black";
    o.innerHTML = "🎆 SUPER ! 🎆";
}

function dislikeStep1() {
    const o = document.getElementById("overlay");
    o.style.display = "flex";
    o.style.background = "black";
    o.classList.add("glitch");

    setTimeout(() => {
        o.classList.remove("glitch");
        o.innerHTML = `
        Bist du sicher, dass du es nicht mochtest?<br><br>
        <button onclick="blackScreen()">Ja</button>
        <button onclick="likeSite()">Nein 😄</button>
        `;
    }, 1500);
}

function blackScreen() {
    const o = document.getElementById("overlay");
    o.style.background = "black";
    o.innerHTML = "";
}
</script>

</body>
</html>
