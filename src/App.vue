<template>
  <div id="app" class="app-container">
    <h1 class="novel-title">🚀 <span class="title-text">Dia Angkasa</span> 🌟</h1>
    <div class="content-wrapper">
      <ChapterList :chapters="chapters" @chapterClicked="displayChapter" />
      <div v-if="currentChapter" class="current-chapter">
        <h2>{{ currentChapter.title }}</h2>
        <p>{{ currentChapter.content }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import ChapterList from './components/ChapterList.vue';
import Chapter1 from './components/Chapter1.vue';
import Chapter2 from './components/Chapter2.vue';
import Chapter3 from './components/Chapter3.vue'; 

export default {
  name: 'App',
  components: {
    ChapterList,
    Chapter1,
    Chapter2,
    Chapter3 
  },
  data() {
    return {
      novelTitle: 'Dia Angkasa',
      chapters: [
        { id: 1, title: 'Chapter 1: Jarak', content: 'Orang-orang yang katanya akam terus bersama kita, pada waktunya  akan tetap memilih pemahamannya sendiri.' },
        { id: 2, title: 'Chapter 2: Misi Antariksa', content: 'Dalam gemerlapnya bintang-bintang, kita menemukan keajaiban yang tak terbatas. Perjalanan ini mengajarkan kita untuk tidak pernah berhenti bermimpi. Di sana, di tengah impian dan ilusi, kita menemukan keberanian untuk mencapai apa pun yang kita inginkan. Jadi, biarkan mimpi membimbing kita melintasi langit yang tak terbatas, karena di sana, di balik setiap awan, mungkin saja kita menemukan bintang kita sendiri yang bersinar paling terang.' },
        { id: 3, title: 'Chapter 3: Titik Awal', content: 'Ilusi atau nyata, kau tetap fana, bersama dengan harapan, dan segala hal baik yang selalu gagal untuk diartikan.' } 
      ],
      currentChapter: null
    };
  },
  methods: {
    displayChapter(chapterId) {
      this.currentChapter = this.chapters.find(chapter => chapter.id === chapterId);
    }
  }
}
</script>

<style>
#app {
  background-color: #ffd4f2; /* Warna pink pastel */
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
}

.app-container {
  max-width: 800px;
  width: 100%;
}

.novel-title {
  font-family: 'Comic Sans MS', cursive, sans-serif;
  text-align: center;
  font-size: 36px;
  margin-bottom: 20px;
  padding: 10px 20px;
  border: 3px solid #ff96d6; /* Warna bingkai */
  border-radius: 10px;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.title-text {
  color: #ff96d6; /* Warna teks */
}

.content-wrapper {
  background-color: #fff;
  padding: 20px;
  border-radius: 20px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  width: 100%;
  max-width: 600px;
}

.current-chapter {
  margin-top: 30px;
}
</style>