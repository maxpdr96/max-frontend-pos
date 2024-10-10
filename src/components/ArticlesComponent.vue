<script setup lang="ts">
import { ref } from 'vue'
import ArticleItem from './ArticleItem.vue'

const articles = [
  {
    heading: 'Flexbox: Como Centralizar Elementos com Facilidade',
    content:
      "Aprenda a utilizar o Flexbox para alinhar e centralizar elementos na sua página de forma intuitiva.\n" +
      "Este guia rápido mostra como o Flexbox pode simplificar seu layout.",
    url: "https://css-tricks.com/snippets/css/a-guide-to-flexbox/"
  },
  {
    heading: 'Grid Layout: O Guia Completo para Layouts Responsivos',
    content:
      "Descubra como o CSS Grid permite criar layouts complexos e adaptáveis a diferentes dispositivos.\n" +
      "Saiba como organizar seus elementos de forma eficiente e moderna.",
    url: "https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_grid_layout/Basic_concepts_of_grid_layout"
  },
  {
    heading: 'As Melhores Ferramentas de Desenvolvimento para Front-End em 2024',
    content:
      "Conheça as ferramentas indispensáveis para desenvolvedores front-end neste ano.\n" +
      "Aumente sua produtividade e otimize seu workflow com esses recursos.",
    url: "http://localhost"
  },
  {
    heading: 'Media Queries: Tornando Seu Site Responsivo',
    content:
      "Domine as media queries para adaptar seu site a uma variedade de tamanhos de tela.\n" +
      "Melhore a experiência do usuário criando layouts que se ajustam a qualquer dispositivo.",
    url: "http://localhost"
  },
  {
    heading: 'React vs. Vue: Qual Escolher para Seu Próximo Projeto?',
    content:
      "Compare os principais frameworks de JavaScript e descubra qual é o mais adequado para você.\n" +
      "Analise suas diferenças em performance, curva de aprendizado e flexibilidade.",
    url: "http://localhost"
  },
  {
    heading: 'Otimizando o Desempenho do Front-End com Lazy Loading',
    content:
      "Aprenda como implementar lazy loading e acelerar o tempo de carregamento do seu site.\n" +
      "Reduza a carga inicial e melhore a experiência do usuário com técnicas avançadas.",
    url: "http://localhost"
  },
  {
    heading: 'SASS vs. LESS: Qual Pré-Processador de CSS Usar?',
    content:
      "Entenda as principais diferenças entre SASS e LESS e descubra qual se adapta melhor ao seu projeto." +
      " Saiba qual ferramenta pode otimizar seu processo de estilização.",
    url: "http://localhost"
  }
]

const articlesToShow = ref(4)

const showMoreArticles = () => {
  articlesToShow.value += 4
}
</script>

<template>
  <div>
    <ArticleItem v-for="(article, index) in articles.slice(0, articlesToShow)" :key="index">
      <template #heading>
        <a :href="article.url" target="_blank" rel="noopener">{{ article.heading }}</a>
      </template>
      <div v-html="article.content"></div>
    </ArticleItem>

    <div v-if="articlesToShow < articles.length" style="text-align: center;">
      <button @click="showMoreArticles">
        Ver mais
      </button>
    </div>
  </div>
</template>

<style scoped>
button {
  margin-top: 2rem;
  padding: 0.5rem 1rem;
  background-color: #2f548c;
  color: white;
  border: none;
  cursor: pointer;
  font-size: 1rem;
  border-radius: 0.3rem;
}

button:hover {
  background-color: #6a91e8;
}
</style>