<template>
  <div class="test">
    <input type="text" v-model="title"><br />
    <h1>{{title}} is the best show.</h1>
    <p v-if="showName">{{user.firstName}} {{user.lastName}}</p>
    <p v-else="showName">Nobody</p>
    <button v-on:click="ohayo('ohayo gozaimasu おはようございます!')">ohayo!</button>
    <input type="text" v-on:keyup="pressKey" v-on:keyup.enter="enterHit">
  </div>
</template>

<script>
  export default {
    name: 'test',
    data() {
      return {
        title: 'Purizun Sukūru',
        user: {
          firstName: 'Kiyoshi',
          lastName: 'Fujino'
        },
        showName: true
      }
    },
    methods: {
      ohayo: function(gozaimasu) {
        alert(gozaimasu);
      },
      pressKey: function(e){
        var x = e.target.value;
        console.log(x + ' wrong!');
      },
      enterHit: function(){
        console.log("You hit enter!");
      }
    }
  }
</script>


<style scoped>

ul {
  padding: 0;
}

li {
  list-style: none;
}
</style>
