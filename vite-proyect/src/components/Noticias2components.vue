<template>
  <section id="noticias" class="noticias">

    <h2>📰 Noticias de River Plate</h2>

    <div class="contenedor">

      <div class="card" v-for="(noticia, index) in noticias" :key="index">
        <img :src="noticia.img" />
        <h3>{{ noticia.titulo }}</h3>
        <p>{{ noticia.descripcion }}</p>
        <button @click="verMas(noticia.titulo)">Ver más</button>
      </div>

    </div>

  </section>
</template>

<script>
export default {
  name: "Noticias2Components",
  data() {
    return {
      noticias: [
        {
          titulo: "River pasó a cuartos del Torneo Apertura",
          descripcion: "El equipo de River logró una gran victoria y se metió entre los mejores del torneo argentino.",
          img: "https://images.unsplash.com/photo-1603297631951-1c3d7c3f9a3d"
        },
        {
          titulo: "Gran momento del equipo",
          descripcion: "River mantiene una racha positiva y se perfila como candidato al título.",
          img: "https://images.unsplash.com/photo-1574629810360-7efbbe195018"
        },
        {
          titulo: "Fiesta en el Monumental",
          descripcion: "Los hinchas acompañaron al equipo en una noche increíble.",
          img: "https://images.unsplash.com/photo-1508098682722-e99c43a406b2"
        },
        {
          titulo: "Nuevo refuerzo en camino",
          descripcion: "El club negocia la llegada de un jugador clave para el próximo torneo.",
          img: "https://images.unsplash.com/photo-1517927033932-b3d18e61fb3a"
        }
      ]
    }
  },
  methods: {
    verMas(titulo) {
      alert("Abrir noticia: " + titulo)
    }
  }
}
</script>

<style scoped>
.noticias {
  padding: 50px;
  background: #f5f5f5;
  text-align: center;
}

.noticias h2 {
  color: #b30000;
  margin-bottom: 30px;
}

/* GRID */
.contenedor {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

/* CARD */
.card {
  background: white;
  border-radius: 12px;
  padding: 15px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.2);
  transition: 0.3s;
}

.card:hover {
  transform: translateY(-5px);
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

/* BOTÓN */
.card button {
  margin-top: 10px;
  background: #b30000;
  color: white;
  border: none;
  padding: 6px 12px;
  border-radius: 20px;
  cursor: pointer;
}

.card button:hover {
  background: #800000;
}
</style>