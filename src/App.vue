<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HeaderComponent from './components/HeaderComponent.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink class="white-custom" to="/blog">Blog</RouterLink>
        <RouterLink class="white-custom" to="/about">Sobre</RouterLink>
        <RouterLink class="white-custom" to="/description">Descrição</RouterLink>
      </nav>

      <HeaderComponent name="Seu nome" />
    </div>
  </header>
  <h1>Últimas do blog</h1>
  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
  background-color: #2f558d;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

header {
  display: flex;
  place-items: center;
  padding-right: calc(var(--section-gap) / 2);
}

.logo {
  margin: 0 2rem 0 0;
}

header .wrapper {
  display: flex;
  justify-content: center;
  place-items: flex-start;
  flex-wrap: wrap;
}

@media (min-width: 1024px) {
  header .wrapper {
    flex-wrap: wrap;
    padding-bottom: 2rem;
  }
}

nav {
  text-align: left;
  font-size: 1rem;
  padding: 1rem 0;
  margin-top: 1rem;
}

h1 {
  margin-top: 2rem;
  text-align: center;
  font-weight: bold;
  font-size: 2em;
  color: #333;
}
</style>
