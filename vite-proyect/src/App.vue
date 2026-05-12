<template>
  <div>

    <!-- NAVBAR -->
    <NavbarRiver />

    <!-- HERO -->
    <section class="inicio">
      <div class="overlay">
        <h1>Bienvenido a RiverID</h1>
        <p>Viví toda la pasión del Más Grande ⚪🔴⚪</p>

        <div class="botones">
          <button @click="irANoticias">Ver Noticias</button>
          <button class="secundario" @click="alerta">Hacete Socio</button>
        </div>
      </div>
    </section>

    <!-- SECCIÓN DESTACADA -->
    <section class="destacado">
      <div class="texto">
        <h2>El Monumental vibra</h2>
        <p>
          El estadio más grande de Sudamérica late con cada partido.
          River sigue haciendo historia con su gente.
        </p>
        <button @click="irANoticias">Leer más</button>
      </div>

      <div class="imagen">
        <img src="https://www.cariverplate.com.ar/imagenes/archivos/2023-07/255679-5.jpg" />
      </div>
    </section>

    <!-- GALERÍA -->
    <section class="galeria">
      <h2>Momentos River</h2>

      <div class="grid-galeria">
        <img src="https://www.cariverplate.com.ar/los-hinchas-y-el-mas-monumental-una-formula-ideal" />
        <img src="https://images.unsplash.com/photo-1517927033932-b3d18e61fb3a" />
        <img src="https://images.unsplash.com/photo-1574629810360-7efbbe195018" />
      </div>
    </section>

    <!-- NOTICIAS -->
    <Noticias2Components />

    <!-- FOOTER -->
    <footer class="footer">
      © 2026 RiverID - El Más Grande de América
    </footer>

  </div>
</template>

<script>
import NavbarRiver from "./components/navbar.vue"
import Noticias2Components from "./components/Noticias2Components.vue"

export default {
  components: {
    NavbarRiver,
    Noticias2Components
  },
  methods: {
    irANoticias() {
      const sec = document.getElementById("noticias")
      if (sec) {
        sec.scrollIntoView({ behavior: "smooth" })
      }
    },
    alerta() {
      alert("Sistema de socios próximamente 🔥")
    }
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: white;
  color: black;
}

/* HERO CON BANDA DE RIVER */
.inicio {
  height: 90vh;
  background: linear-gradient(
      120deg,
      white 40%,
      #ee122a 40%,
      #ee122a 60%,
      white 60%
    ),
    url("https://www.cariverplate.com.ar/los-hinchas-y-el-mas-monumental-una-formula-ideal");
  background-size: cover;
  background-position: center;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* CONTENIDO HERO */
.overlay {
  background: rgba(255,255,255,0.9);
  padding: 40px;
  border-radius: 10px;
  text-align: center;
}

.overlay h1 {
  font-size: 42px;
  color: black;
}

.overlay p {
  color: #333;
}

/* BOTONES */
.botones button {
  background: #ee122a;
  color: white;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 25px;
  cursor: pointer;
}

.secundario {
  background: black;
  color: white;
}

/* DESTACADO */
.destacado {
  display: flex;
  align-items: center;
  gap: 40px;
  padding: 60px;
  background: white;
}

.texto h2 {
  color: black;
}

.texto p {
  color: #555;
}

.imagen img {
  width: 100%;
  border-radius: 10px;
}

/* GALERÍA */
.galeria {
  padding: 50px;
  text-align: center;
  background: #f5f5f5;
}

.galeria h2 {
  color: black;
}

.grid-galeria {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px,1fr));
  gap: 20px;
  margin-top: 20px;
}

.grid-galeria img {
  width: 100%;
  border-radius: 10px;
  transition: 0.3s;
}

.grid-galeria img:hover {
  transform: scale(1.05);
}

/* FOOTER */
.footer {
  background: black;
  color: white;
  text-align: center;
  padding: 25px;
  border-top: 4px solid #ee122a;
}

/* SCROLL SUAVE */
html {
  scroll-behavior: smooth;
}
</style>