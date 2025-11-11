<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Max.Studium2025</title>

<!-- Fuente moderna -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">

<!-- Íconos Font Awesome -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
  body {
    font-family: 'Poppins', sans-serif;
    background-color: #0e0e0e;
    color: #fff;
    margin: 0;
    padding: 0;
    overflow-x: hidden;
    transition: background 0.3s ease;
  }

  header {
    text-align: center;
    font-size: 22px;
    font-weight: 700;
    color: #ff4545;
    background-color: #141414;
    padding: 16px 0;
    box-shadow: 0 2px 8px rgba(0,0,0,0.5);
    letter-spacing: 1px;
  }

  /* --- Galería de cómics --- */
  main {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 14px;
    padding: 16px;
    transition: opacity 0.3s ease;
  }

  .comic {
    background-color: #181818;
    border-radius: 14px;
    overflow: hidden;
    box-shadow: 0 0 15px rgba(255,255,255,0.05);
    position: relative;
    cursor: pointer;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .comic:hover {
    transform: translateY(-4px);
    box-shadow: 0 4px 20px rgba(255,255,255,0.1);
  }

  .comic img {
    width: 100%;
    height: 220px;
    object-fit: cover;
  }

  .comic-number {
    position: absolute;
    top: 8px;
    left: 8px;
    background-color: rgba(255,255,255,0.2);
    padding: 4px 8px;
    border-radius: 8px;
    font-size: 12px;
  }

  .heart {
    position: absolute;
    top: 8px;
    right: 10px;
    font-size: 18px;
    color: #888;
    cursor: pointer;
    transition: color 0.3s;
  }

  .heart.liked {
    color: #ff4545;
  }

  .info {
    padding: 8px 10px 14px;
  }

  .info h3 {
    margin: 0;
    font-size: 15px;
    font-weight: 600;
  }

  .info p {
    margin: 2px 0 0;
    font-size: 13px;
    color: #aaa;
  }

  /* --- Lector de cómics --- */
  #reader {
    display: none;
    padding: 20px;
    animation: fadeIn 0.5s ease;
  }

  #reader img {
    width: 100%;
    margin-bottom: 16px;
    border-radius: 10px;
  }

  #backBtn {
    position: fixed;
    top: 16px;
    left: 16px;
    background: #ff4545;
    color: white;
    border: none;
    padding: 10px 14px;
    border-radius: 10px;
    font-weight: bold;
    cursor: pointer;
    box-shadow: 0 4px 10px rgba(255,69,69,0.3);
    z-index: 10;
  }

  /* --- Barra inferior --- */
  .bottom-bar {
    position: fixed;
    bottom: 0;
    width: 100%;
    background-color: #141414;
    display: flex;
    justify-content: space-around;
    padding: 10px 0;
    border-top: 2px solid #ff4545;
    box-shadow: 0 -3px 10px rgba(0,0,0,0.5);
  }

  .bottom-bar i {
    font-size: 22px;
    color: #888;
    cursor: pointer;
    transition: color 0.3s, transform 0.2s;
  }

  .bottom-bar i.active {
    color: #ff4545;
    transform: scale(1.2);
  }

  /* --- Búsqueda y menú --- */
  #searchSection, #menuSection {
    display: none;
    text-align: center;
    padding: 20px;
    animation: fadeIn 0.4s ease;
  }

  #searchInput {
    width: 85%;
    padding: 10px;
    border-radius: 10px;
    border: none;
    outline: none;
    font-size: 16px;
    margin-bottom: 20px;
    text-align: center;
    background-color: #222;
    color: #fff;
  }

  /* --- Menú mejorado --- */
  .menu-options {
    display: flex;
    flex-direction: column;
    gap: 15px;
    padding: 10px;
    align-items: center;
    animation: slideUp 0.6s ease;
  }

  .menu-card {
    display: flex;
    align-items: center;
    background: #1b1b1b;
    border-radius: 15px;
    padding: 15px;
    width: 85%;
    box-shadow: 0 0 8px rgba(255, 77, 77, 0.2);
    cursor: pointer;
    transition: all 0.3s ease;
  }

  .menu-card:hover {
    transform: translateY(-3px);
    background: #2a2a2a;
    box-shadow: 0 0 12px rgba(255, 77, 77, 0.4);
  }

  .menu-card i {
    font-size: 28px;
    color: #ff4d4d;
    margin-right: 15px;
  }

  .menu-card h3 {
    margin: 0;
    font-size: 18px;
    color: #fff;
  }

  .menu-card p {
    margin: 3px 0 0;
    font-size: 13px;
    color: #bbb;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes slideUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
</style>
</head>
<body>

<header>📚 Max.Studium2025</header>

<main id="comicGrid">
  <div class="comic" onclick="openComic('comic1')">
    <span class="comic-number">#1</span>
    <span class="heart" onclick="toggleHeart(event, this)">❤</span>
    <img src="/srv/imgs/html/temp/qi4f3mjsdb/1760594616487.jpg" alt="Comic 1">
    <div class="info">
      <h3>Goten Kun</h3>
      <p>Español 🇪🇸</p>
    </div>
  </div>

  <div class="comic" onclick="openComic('comic2')">
    <span class="comic-number">#2</span>
    <span class="heart" onclick="toggleHeart(event, this)">❤</span>
    <img src="https://i.imgur.com/xyz789.jpg" alt="Comic 2">
    <div class="info">
      <h3>Moon Warriors</h3>
      <p>Inglés 🇬🇧</p>
    </div>
  </div>

<div class="comic" onclick="openComic('comic3')">
    <span class="comic-number">#3</span>
    <span class="heart" onclick="toggleHeart(event, this)">❤</span>
    <img src="/srv/imgs/html/temp/qi4f3mjsdb/1760594616487.jpg" alt="Comic 3">
    <div class="info">
      <h3>Moon Warriors</h3>
      <p>Inglés 🇬🇧</p>
    </div>
  </div>

<div class="comic" onclick="openComic('comic2')">
    <span class="comic-number">#2</span>
    <span class="heart" onclick="toggleHeart(event, this)">❤</span>
    <img src="https://i.imgur.com/xyz789.jpg" alt="Comic 2">
    <div class="info">
      <h3>Moon Warriors</h3>
      <p>Inglés 🇬🇧</p>
    </div>
  </div>

<div class="comic" onclick="openComic('comic2')">
    <span class="comic-number">#2</span>
    <span class="heart" onclick="toggleHeart(event, this)">❤</span>
    <img src="/srv/imgs/html/temp/qi4f3mjsdb/1760594616487.jpg" alt="Comic 2">
    <div class="info">
      <h3>Moon Warriors</h3>
      <p>Inglés 🇬🇧</p>
    </div>
  </div>

<div class="comic" onclick="openComic('comic2')">
    <span class="comic-number">#2</span>
    <span class="heart" onclick="toggleHeart(event, this)">❤</span>
    <img src="https://i.imgur.com/xyz789.jpg" alt="Comic 2">
    <div class="info">
      <h3>Moon Warriors</h3>
      <p>Inglés 🇬🇧</p>
    </div>
  </div>
</main>

<div id="reader">
  <button id="backBtn" onclick="closeComic()">⬅ Volver</button>
  <div id="comicPages"></div>
</div>

<!-- 🔍 Sección de búsqueda -->
<div id="searchSection">
  <h2>🔍 Buscar Cómic</h2>
  <input type="text" id="searchInput" placeholder="Escribe un título...">
  <div id="searchResults"></div>
</div>

<!-- ☰ Menú mejorado -->
<div id="menuSection">
  <h2 style="text-align:center; color:#ff4d4d; margin-bottom:20px;">⚙️ Menú principal</h2>

  <div class="menu-options">
    <div class="menu-card" onclick="alert('Abrir tu perfil')">
      <i class="fa-solid fa-user"></i>
      <div>
        <h3>Perfil</h3>
        <p>Edita tu información personal</p>
      </div>
    </div>

    <div class="menu-card" onclick="alert('Abrir tus cómics favoritos')">
      <i class="fa-solid fa-heart"></i>
      <div>
        <h3>Favoritos</h3>
        <p>Guarda los cómics que amas</p>
      </div>
    </div>

    <div class="menu-card" onclick="alert('Abrir configuraciones')">
      <i class="fa-solid fa-gear"></i>
      <div>
        <h3>Configuración</h3>
        <p>Personaliza la aplicación</p>
      </div>
    </div>

    <div class="menu-card" onclick="alert('Abrir ayuda y contacto')">
      <i class="fa-solid fa-circle-question"></i>
      <div>
        <h3>Ayuda y contacto</h3>
        <p>¿Necesitás asistencia?</p>
      </div>
    </div>
  </div>
</div>

<!-- Barra inferior -->
<div class="bottom-bar">
  <i id="homeBtn" class="active" onclick="showSection('home')">🏠</i>
  <i id="searchBtn" onclick="showSection('search')">🔍</i>
  <i id="menuBtn" onclick="showSection('menu')">☰</i>
</div>

<script>
const comics = {
  comic1: [
    "/srv/imgs/html/temp/qi4f3mjsdb/1760594616487.jpg",
                    "/srv/imgs/html/temp/a30q6u85xv/1760594620166.jpg",
                    "/srv/imgs/html/temp/3b8fzwspc2/1760594624056.jpg",
                    "/srv/imgs/html/temp/5w2h1c07q8/1760594627039.jpg",
                    "/srv/imgs/html/temp/gonrbkp80h/1760594629887.jpg",
                    "/srv/imgs/html/temp/gonrbkp80h/1760594632926.jpg",
                    "/srv/imgs/html/temp/gonrbkp80h/1760594635920.jpg",
                    "/srv/imgs/html/temp/gonrbkp80h/1760594638871.jpg",
                    "/srv/imgs/html/temp/cgdm73l5b6/1760594641903.jpg",
                    "/srv/imgs/html/temp/cgdm73l5b6/1760594645020.jpg",
                    "/srv/imgs/html/temp/cgdm73l5b6/1760594649192.jpg",
                    "/srv/imgs/html/temp/cgdm73l5b6/1760594652210.jpg",
                    "/srv/imgs/html/temp/l7426crsmp/1760594655658.jpg",
                    "/srv/imgs/html/temp/l7426crsmp/1760594658603.jpg",
                    "/srv/imgs/html/temp/l7426crsmp/1760594661877.jpg",
                    "/srv/imgs/html/temp/l7426crsmp/1760594664627.jpg",
                    "/srv/imgs/html/temp/l7426crsmp/1760594668210.jpg"
  ],
  comic2: [
    "https://i.imgur.com/pagina3.jpg",
    "https://i.imgur.com/pagina4.jpg"
  ]
};

let lastScroll = 0; // guarda posición de la galería

function openComic(id) {
  lastScroll = window.scrollY; // guarda donde estabas

  document.getElementById("comicGrid").style.display = "none";
  document.getElementById("reader").style.display = "block";
  document.getElementById("comicPages").innerHTML = comics[id]
    .map(img => `<img src="${img}">`)
    .join("");

  document.querySelector(".bottom-bar").style.display = "none";

  // Asegura que el lector empiece siempre desde arriba
  setTimeout(() => window.scrollTo({ top: 0, behavior: "smooth" }), 50);

  // Muestra el botón flotante
  document.getElementById("scrollTopBtn").style.display = "block";
}

function closeComic() {
  document.getElementById("reader").style.display = "none";
  document.getElementById("comicGrid").style.display = "grid";
  document.querySelector(".bottom-bar").style.display = "flex";

  // Oculta el botón flotante
  document.getElementById("scrollTopBtn").style.display = "none";

  // Vuelve a la posición anterior
  window.scrollTo({ top: lastScroll, behavior: "smooth" });
}

function closeComic() {
  document.getElementById("reader").style.display = "none";
  document.getElementById("comicGrid").style.display = "grid";
  document.querySelector(".bottom-bar").style.display = "flex";
}

function toggleHeart(event, el) {
  event.stopPropagation();
  el.classList.toggle("liked");
}

function showSection(section) {
  document.getElementById("comicGrid").style.display = section === "home" ? "grid" : "none";
  document.getElementById("searchSection").style.display = section === "search" ? "block" : "none";
  document.getElementById("menuSection").style.display = section === "menu" ? "block" : "none";

  document.querySelectorAll(".bottom-bar i").forEach(i => i.classList.remove("active"));
  if (section === "home") homeBtn.classList.add("active");
  if (section === "search") searchBtn.classList.add("active");
  if (section === "menu") menuBtn.classList.add("active");
}

// 🔍 Búsqueda corregida
const searchInput = document.getElementById("searchInput");
const searchResults = document.getElementById("searchResults");
const allComics = Array.from(document.querySelectorAll(".comic")).map(c => c.outerHTML);

searchInput.addEventListener("input", function () {
  const term = this.value.toLowerCase().trim();
  searchResults.innerHTML = ""; // limpia resultados anteriores

  if (term === "") return; // si no hay texto, no mostrar nada

  // filtra cómics sin duplicar
  const filtered = allComics.filter(html => html.toLowerCase().includes(term));

  searchResults.innerHTML = filtered.length
    ? filtered.join("")
    : "<p>No se encontró ningún cómic</p>";
});
</script>

</body>
</html>
