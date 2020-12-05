<template>
  
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HelloWorld from './components/HelloWorld.vue';

export default defineComponent({
  name: 'App',
  components: {
    HelloWorld
  },
  props: {
    works_1: {
      type: Number,
    },
    works_2: {
      type: Number,
      validator: () => true,
    },
    breaks_1: {
      type: Number,
      validator() { return true },
    },
    breaks_2: {
      type: Number,
      validator: function () { return true },
    },
  },
  setup(props) {
    console.log(props);
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
