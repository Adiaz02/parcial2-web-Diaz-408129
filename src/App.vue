<template>
  <div>
    <Header />
    <main class="container">
      <Sidebar />
      <section class="content">
        <Tabs />
        <router-view></router-view>
      </section>
    </main>
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import Sidebar from './components/SideBar.vue'
import Tabs from './components/Tabs.vue'
</script>
