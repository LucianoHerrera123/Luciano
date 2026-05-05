<script>
export default {
  name: "NavbarRiver"
}
</script>

<template>
  <!-- NAVBAR RIVER -->
  <header class="header">
    <div class="container">

      <!-- LOGO -->
      <div class="logo">
        <span class="shield">🔴⚪</span>
        <div class="text">
          <span class="title">RiverID </span>
          <span class="subtitle">Club Atlético River Plate</span>
        </div>
      </div>

      <!-- NAV -->
      <nav>
        <ul class="nav-links">
          <li><a href="#">Inicio</a></li>
          <li><a href="#">Entradas</a></li>
          <li><a href="#">Socio</a></li>
          <li><a href="#">Beneficios</a></li>
        </ul>
      </nav>

      <!-- CTA (tipo RiverID) -->
      <div class="actions">
        <button class="login">Ingresar</button>
        <button class="register">Registrarse</button>
      </div>

    </div>
  </header>

  <!-- CONTENIDO DEMO -->
  <main class="main">
    <h1>Bienvenido a RiverID</h1>
  </main>

  <!-- FOOTER SIMPLE PRO -->
  <footer class="footer">
    <div class="footer-content">
      <span class="brand">🔴 River Plate</span>
      <span class="legal">Sistema RiverID para socios e hinchas</span>
    </div>

    <div class="copy">
      © 2026 Club Atlético River Plate
    </div>
  </footer>
</template>

<style>
/* RESET */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* BODY */
body {
  font-family: Arial, sans-serif;
  background: #0b0b0b;
  color: white;
}

/* HEADER */
.header {
  position: sticky;
  top: 0;
  background: white;
  color: black;
  border-bottom: 3px solid #d60000;
  padding: 12px 30px;
  z-index: 1000;
}

/* CONTAINER */
.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* LOGO */
.logo {
  display: flex;
  align-items: center;
}

.shield {
  font-size: 24px;
  margin-right: 10px;
}

.text .title {
  font-weight: bold;
  color: #d60000;
  font-size: 16px;
}

.text .subtitle {
  font-size: 11px;
  color: #555;
}

/* NAV */
.nav-links {
  display: flex;
  list-style: none;
  gap: 20px;
}

.nav-links a {
  text-decoration: none;
  color: black;
  font-size: 14px;
  font-weight: 500;
  transition: 0.3s;
}

/* hover estilo River */
.nav-links a:hover {
  color: #d60000;
}

/* BOTONES */
.actions {
  display: flex;
  gap: 10px;
}

.login {
  background: transparent;
  border: 1px solid #d60000;
  color: #d60000;
  padding: 6px 12px;
  cursor: pointer;
  border-radius: 4px;
  transition: 0.3s;
}

.login:hover {
  background: #d60000;
  color: white;
}

.register {
  background: #d60000;
  border: none;
  color: white;
  padding: 6px 12px;
  cursor: pointer;
  border-radius: 4px;
  transition: 0.3s;
}

.register:hover {
  background: #a80000;
}

/* MAIN */
.main {
  height: 60vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* FOOTER */
.footer {
  background: #111;
  border-top: 2px solid #d60000;
  padding: 15px 20px;
  margin-top: 40px;
}

/* contenido */
.footer-content {
  display: flex;
  justify-content: space-between;
  font-size: 13px;
  opacity: 0.8;
}

/* copy */
.copy {
  text-align: center;
  margin-top: 10px;
  font-size: 12px;
  opacity: 0.5;
}
</style>