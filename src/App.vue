<template>
  <div id="app">
    <p>Číslo z Child2: {{ num }}</p>
    <Child1 :num="num" />
    <Child2 @clickedNumber="clickedNumber" />
  </div>
</template>

<script>
import Child1 from './components/Child1';
import Child2 from './components/Child2';

export default {
  name: 'App',
  components: {
    Child1,
    Child2,
  },
  data() {
    return {
      num: '',
    };
  },
  methods: {
    clickedNumber(num) {
      this.num = num;
      console.log(num);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  flex-wrap: wrap;
}

p {
  flex-basis: 100%;
  display: block;
}
</style>
