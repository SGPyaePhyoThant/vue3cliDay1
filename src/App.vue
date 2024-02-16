<template>
  <h3>{{title}}</h3>
  <input type="text" ref="name">
  <input type="number" ref="age">
  <button @click="handleClick">click</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
  data() {
    return {
      title: 'This is my vue 3 version app'
    }
  },
  methods:{
    handleClick(){
       const nameElement = this.$refs.name as HTMLElement; // Explicitly type this.$refs.name as HTMLElement
    nameElement.classList.add('active');
    nameElement.focus();
    }
  }
  
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
