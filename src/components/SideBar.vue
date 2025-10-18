<template>
  <aside class="sidebar">
    <img src="../assets/images/Photo.jpeg" alt="Foto de perfil" class="profile-pic" />
    <h2 class="profile-name">Andrés Felipe Díaz Guzmán</h2>

    <nav>
      <ul>
        <li class="hobbies">
          Hobbies
          <ul>
            <li class="hobby-item"><a href="#">Anime</a></li>
            <li class="hobby-item"><a href="#">Videojuegos</a></li>
            <li class="hobby-item"><a href="#">Música</a></li>
          </ul>
        </li>
        <li><a href="#">Amigos</a></li>
      </ul>
    </nav>

    <div class="friends-list">
      <div class="friend" v-for="(friend, index) in friends" :key="index">
        <img :src="friend.img" :alt="friend.name" />
        <p>{{ friend.name }}</p>
      </div>
    </div>

    <button class="btn-ir" @click="irUniversidad">Universidad</button>
  </aside>
</template>

<script setup>
const friends = [
  { name: 'Julian Guzmán', img: 'https://i.pravatar.cc/100?img=11' },
  { name: 'Valentina Díaz', img: 'https://i.pravatar.cc/100?img=20' },
  { name: 'Evelyn Guzmán', img: 'https://i.pravatar.cc/100?img=21' },
  { name: 'Juan Fernando', img: 'https://i.pravatar.cc/100?img=12' }
]

function irUniversidad() {
  window.location.href = 'https://www.unicatolica.edu.co'
}
</script>
