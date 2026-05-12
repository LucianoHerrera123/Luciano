<template>
  <section id="noticias" class="noticias">

    <h2>Últimas Noticias de River Plate</h2>

    <div class="contenedor-noticias">

      <!-- NOTICIA 1 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1603297631951-1c3d7c3f9a3d" />
        <h3>River pasó a cuartos del Torneo Apertura</h3>
        <p>El equipo logró la clasificación tras un gran partido y se mete entre los mejores del torneo.</p>
      </div>

      <!-- NOTICIA 2 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1574629810360-7efbbe195018" />
        <h3>Gran nivel del equipo de Demichelis</h3>
        <p>River mantiene una racha positiva y se posiciona como candidato al título.</p>
      </div>

      <!-- NOTICIA 3 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1508098682722-e99c43a406b2" />
        <h3>El Monumental explotó de emoción</h3>
        <p>Los hinchas acompañaron al equipo en una noche inolvidable.</p>
      </div>

    </div>

  </section>
</template>

<script>
export default {
  name: "NoticiasComponents"
}
</script>

<style scoped>
.noticias {
  padding: 40px;
  background-color: #f5f5f5;
  text-align: center;
}

.noticias h2 {
  margin-bottom: 30px;
  color: #b30000;
}

.contenedor-noticias {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}

.card {
  background: white;
  border-radius: 10px;
  width: 300px;
  padding: 15px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.2);
  transition: 0.3s;
}

.card:hover {
  transform: scale(1.05);
}

.card img {
  width: 100%;
  border-radius: 10px;
}

.card h3 {
  margin: 10px 0;
}

.card p {
  font-size: 14px;
}
</style>