<template>
  <div class="intro">
    <h1>{{title}}</h1>
    <p>Tracking chapters read in {{title}}.</p>
  </div>
</template>

<script>
  export default {
    name: 'intro',
    data() {
      return {
        title: 'Purizun Sukūru', // Actually Kangoku Gakuen
      }
    }
  }

</script>
