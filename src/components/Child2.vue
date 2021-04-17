<template>
  <section class="child2">
    <h1>Child 2</h1>
    <ul>
      <li id="1" @click="clickedNumber($event)">Prvni</li>
      <li id="2" @click="clickedNumber($event)">Druhy</li>
      <li id="3" @click="clickedNumber($event)">Treti</li>
      <li id="4" @click="clickedNumber($event)">Ctvrty</li>
    </ul>
  </section>
</template>
<style>
.child2 {
  width: 40%;
  margin: 2rem;
}
ul {
  display: flex;
  justify-content: space-between;
  list-style: none;
}

li {
  font-size: 1.5rem;
  border: 2px solid maroon;
  margin: 0.5rem;
  padding: 0.5rem;
  cursor: pointer;
}
</style>
<script>
export default {
  name: 'Child2',
  data() {
    return {
      num: '',
    };
  },
  methods: {
    clickedNumber: function(event) {
      let num = event.currentTarget.id;
      console.log(num);
      this.$emit('clickedNumber', num);
    },
  },
};
</script>
