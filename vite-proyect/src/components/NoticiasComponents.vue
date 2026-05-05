<script>
export default {
  name: "NoticiasComponents"
}
</script>

<template>
  <main class="dashboard">

    <section class="header-news">
      <h1>Noticias de River</h1>
      <p>Enterate de todo lo que pasa en el club</p>
    </section>

    <section class="featured">
      <div class="featured-card">
        <h2>🔥 River ganó el Superclásico</h2>
        <p>Gran victoria en el Monumental con un gran rendimiento del equipo.</p>
        <button>Leer más</button>
      </div>
    </section>

    <section class="news-grid">

      <div class="news-card">
        <h3>Nuevo refuerzo</h3>
        <p>El club suma una pieza clave para la temporada.</p>
      </div>

      <div class="news-card">
        <h3>Entradas disponibles</h3>
        <p>Ya podés comprar tickets para el próximo partido.</p>
      </div>

      <div class="news-card">
        <h3>Entrenamiento</h3>
        <p>El plantel se prepara en Ezeiza.</p>
      </div>

      <div class="news-card">
        <h3>DT habló con la prensa</h3>
        <p>Analizó el rendimiento del equipo.</p>
      </div>

    </section>

  </main>
</template>

<style scoped>
.dashboard {
  padding: 30px;
  max-width: 1100px;
  margin: auto;
  font-family: Arial;
}

.header-news h1 {
  font-size: 28px;
}

.header-news p {
  color: gray;
  margin-bottom: 20px;
}

.featured-card {
  background: linear-gradient(135deg, #d60000, #8b0000);
  color: white;
  padding: 20px;
  border-radius: 10px;
  margin-bottom: 20px;
}

.featured-card button {
  margin-top: 10px;
  padding: 8px 12px;
  border: none;
  background: white;
  color: #d60000;
  font-weight: bold;
  cursor: pointer;
}

.news-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 15px;
}

.news-card {
  background: #1a1a1a;
  color: white;
  padding: 15px;
  border-radius: 8px;
}
</style>