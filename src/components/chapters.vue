<template>
  <div class="chapters">
    <button v-on:click="getChapters()">Retrieve Data</button>
    <ul class="chapterName">
      <li v-for="chapter in reverse">
        <input type="checkbox" class="toggle" v-model="chapter.read">
        <span :class="{read: chapter.read}">
        {{chapter.number}} - {{chapter.title}}
        </span>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'chapters',
    data() {
      return {
        chapters: [
          {
            number: 1,
            title: 'The Three Kingdoms',
            read: false
          },
          {
            number: 2,
            title: 'The Four Kingdoms',
            read: false
          },
          {
            number: 3,
            title: 'The Five Kingdoms',
            read: false
          }
        ]
      }
    },
    computed: {
      reverse: function() {
        return this.chapters.reverse();
      }
    },
    methods: {
      getChapters: function () {
        this.$http.get('https://www.mangaeden.com/api/manga/4e70e9f6c092255ef7004336/')
          .then (response => {
            this.chapters = response.json();
          }, response => {
            console.log("error");
            // error callback
        });
      }
    }
  }
</script>

<style scroped>

.read {
  text-decoration: line-through;
}

.chapterName {
  margin: 0 auto;
}

ul {
  padding: 0;
}

li {
  list-style: none;
}

button {
  border-radius: 0px;
  color: white;
  font-size: 1em;
  background: #2c3e50;
  border: none;
  padding: 5px 20px;
  margin-bottom: 20px;
}

button:hover {
  background-color: #688aad;
}

</style>
