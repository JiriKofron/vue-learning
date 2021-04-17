<template>
  <div id="app">
    <p>Číslo z Child2: {{ num }}</p>
    <!-- Child 1 is using props as it communicates parent to child, :num means it takes props and assign it to variable num-->
    <Child1 :num="num" />
    <!-- Child 2 is using emit as it communicates child to parent, @clickedNumber means it takes emitted method from Child2 and use it for parent method-->
    <Child2 @clickedNumber="clickedNumber" />
  </div>
</template>

<script>
// Importing both child component, so its method and variables can be shared
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
    // clickedNumber is taking method from Child1 with emit - see above in component declaration and store parametr - variable to parent component variable
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
