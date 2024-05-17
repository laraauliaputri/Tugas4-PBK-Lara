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
        title: 'Chapter 1: Jarak',
        content: 'Orang-orang yang katanya akam terus bersama kita, pada waktunya  akan tetap memilih pemahamannya sendiri.'
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
</style>