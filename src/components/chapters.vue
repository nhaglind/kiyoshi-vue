<template>
  <div class="chapters">
    <ul class="chapterName">
      <li v-for="chapter in chapters">
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

</style>
