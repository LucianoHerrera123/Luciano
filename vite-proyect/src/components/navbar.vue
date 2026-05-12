<template>
  <header class="header">
    <nav class="nav">

      <!-- LOGO -->
      <div class="logo">
        <h2>RiverID</h2>
      </div>

      <!-- LINKS -->
      <ul class="nav-links">
        <li><a href="#" @click="setActive('inicio')" :class="{active: active === 'inicio'}">Inicio</a></li>
        <li><a href="#" @click="setActive('noticias')" :class="{active: active === 'noticias'}">Noticias</a></li>
        <li><a href="#" @click="setActive('equipo')" :class="{active: active === 'equipo'}">Equipo</a></li>
        <li><a href="#" @click="setActive('socios')" :class="{active: active === 'socios'}">Socios</a></li>
      </ul>

      <!-- DERECHA -->
      <div class="right-section">

        <!-- BUSCADOR -->
        <input 
          type="text" 
          placeholder="Buscar..." 
          v-model="search"
        />

        <!-- BOTÓN -->
        <button @click="login">Ingresar</button>
      </div>

    </nav>
  </header>
</template>

<script>
export default {
  name: "NavbarRiver",
  data() {
    return {
      active: "inicio",
      search: ""
    }
  },
  methods: {
    setActive(seccion) {
      this.active = seccion
    },
    login() {
      alert("Función de login próximamente 😎")
    }
  }
}
</script>

<style scoped>
.header {
  background: linear-gradient(90deg, #b30000, #800000);
  padding: 12px 20px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.3);
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

/* LOGO */
.logo h2 {
  color: white;
  margin: 0;
  font-weight: bold;
}

/* LINKS */
.nav-links {
  list-style: none;
  display: flex;
  gap: 25px;
}

.nav-links li a {
  color: white;
  text-decoration: none;
  font-weight: 600;
  position: relative;
  transition: 0.3s;
}

/* HOVER EFECTO */
.nav-links li a::after {
  content: "";
  position: absolute;
  width: 0%;
  height: 2px;
  background: white;
  bottom: -5px;
  left: 0;
  transition: 0.3s;
}

.nav-links li a:hover::after {
  width: 100%;
}

/* ACTIVO */
.active {
  border-bottom: 2px solid white;
}

/* DERECHA */
.right-section {
  display: flex;
  align-items: center;
  gap: 10px;
}

/* BUSCADOR */
.right-section input {
  padding: 5px 10px;
  border-radius: 20px;
  border: none;
  outline: none;
}

/* BOTÓN */
.right-section button {
  background-color: white;
  color: #b30000;
  border: none;
  padding: 6px 12px;
  border-radius: 20px;
  cursor: pointer;
  font-weight: bold;
  transition: 0.3s;
}

.right-section button:hover {
  background-color: #eee;
}
</style>