<template>
  <section class="child2">
    <h1>Child 2</h1>
    <ul>
      <li>Prvni</li>
      <li>Druhy</li>
      <li>Treti</li>
      <li>Ctvrty</li>
    </ul>
  </section>
</template>
<style>
.child2 {
  width: 50%;
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
    return {};
  },
};
</script>
