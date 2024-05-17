<template>
  <div class="chapter-list">
    <h2>Daftar Chapter:</h2>
    <ul>
      <li v-for="chapter in chapters" :key="chapter.id" @click="selectChapter(chapter.id)">
        {{ chapter.title }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['chapters'],
  methods: {
    selectChapter(chapterId) {
      this.$emit('chapterClicked', chapterId);
    }
  }
}
</script>

<style scoped>
.chapter-list {
  margin-bottom: 20px;
  font-size: 18px;
}

.chapter-list h2 {
  font-size: 24px;
  margin-bottom: 10px;
}

.chapter-list ul {
  list-style-type: none;
  padding: 0;
}

.chapter-list li {
  cursor: pointer;
  margin-bottom: 5px;
  padding: 5px 10px;
  background-color: #ffd4f2;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.chapter-list li:hover {
  background-color: #ddd;
}
</style>