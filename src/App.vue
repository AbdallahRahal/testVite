<template>
  <div>
    <a href="https://dofus.com/fr/" target="_blank">
      <img src="./assets/dofus.webp" alt="Logo Dofus" style="width: 200px; height: auto;">
    </a>
    <Quiz />
  </div>
</template>

<script setup>
import Quiz from './views/Quiz.vue'
import BackButton from './components/BackButton.vue';
import { onMounted } from 'vue';

onMounted(() => {
  const isDevelopment = window.location.hostname === 'localhost';
  const favicon = document.createElement('link');
  favicon.rel = 'icon';
  favicon.type = 'image/png';
  favicon.href = `${isDevelopment ? '' : '/dofusclass'}/dofus.webp`;
  document.head.appendChild(favicon);
});
</script>
