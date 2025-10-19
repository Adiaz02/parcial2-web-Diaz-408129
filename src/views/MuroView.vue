<template>
  <div>
    <h3>Muro</h3>
    <div class="new-post">
      <textarea placeholder="Escribe algo..."></textarea>
      <button class="btn-compartir">Compartir</button>
    </div>

    <div class="post" v-for="(post, index) in posts" :key="index">
      <h4>{{ post.title }}</h4>
      <p>{{ post.content }}</p>
      <div class="time">{{ post.time }}</div>
      <div class="actions">
        <button>👍 Me gusta</button>
        <button>💬 Comentar</button>
      </div>
    </div>
  </div>
</template>

<script setup>
const posts = [
  {
    title: 'Invitación a seminario de IA',
    content: 'Te invito a particiar en el seminario de IA que se realizará en la universidad Unicátolica, el día 14/09/2025 a las 4:00pm. No faltes!!!.',
    time: 'Posteado el Lunes a las 8:45pm'
  },
  {
    title: 'Pelicula Kimetsu no Yaiba',
    content: 'Te invito a ver la película Kimetsu no Yaiba, que se estrenará el 14/09/2025 quienes van a ir??.',
    time: 'Posteado el Domingo a las 7:02am'
  },
  {
    title: 'Estudia programación',
    content: 'Te invito a unirte a mi grupo de estudio de programación. Estamos aprendiendo JavaScript y sería genial contar contigo.',
    time: 'Posteado hoy a las 10:00am'
  }
]
</script>
