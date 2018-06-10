<template>
  <div class= "test">
    <input type="text" v-model="title"><br />
    <span v-html="title"></span>
    <p v-if="showName">{{user.name}}</p>
    <ul>
      <li v-for="item in items">{{item.title}}</li>
    </ul>
    <button v-on:click="greet('Hello World')">Say Greeting</button>
  </div>
</template>

<script>
  export default {
  name: 'test',
  data() {
  return {
    title: 'Learning Vue.js',
    user: {
    name: 'Alan'
          },
          showName: true,
          items: [
          {title:'Item one'},
          {title:'Item two'},
          {title:'Item three'}
                 ]
       }
    },
    methods: {
    greet: function(greeting){
    alert(greeting);
    }
    }
  }
</script>

<style scoped>


</style>
