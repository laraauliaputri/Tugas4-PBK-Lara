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
        title: 'Chapter 2:  Misi Antariksa',
        content: 'alam gemerlapnya bintang-bintang, kita menemukan keajaiban yang tak terbatas. Perjalanan ini mengajarkan kita untuk tidak pernah berhenti bermimpi. Di sana, di tengah impian dan ilusi, kita menemukan keberanian untuk mencapai apa pun yang kita inginkan. Jadi, biarkan mimpi membimbing kita melintasi langit yang tak terbatas, karena di sana, di balik setiap awan, mungkin saja kita menemukan bintang kita sendiri yang bersinar paling terang.'
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
}
</style>