<template>
    <div class="chapter">
      <h2>{{ chapter.title }}</h2>
      <p>{{ chapter.content }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        chapter: {
          title: 'Chapter 3: Titik Awal',
          content: 'Ilusi atau nyata, kau tetap fana, bersama dengan harapan, dan segala hal baik yang selalu gagal untuk diartikan.'
        }
      };
    }
  }
  </script>
  
  <style scoped>
  .chapter {
    margin-bottom: 20px;
    padding: 20px;
    background-color: #f9f9f9;
    border-radius: 10px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  .chapter h2 {
    font-size: 24px;
    margin-bottom: 10px;
    color: #ff96d6; /* Warna judul */
  }
  .chapter p {
    font-size: 16px;
    line-height: 1.6;
    color: #333; /* Warna teks */
  }
  </style>