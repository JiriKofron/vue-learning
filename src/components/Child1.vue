<template>
  <section class="child1">
    <h1>Child 1</h1>
    Číslo v Child2: {{ num }}
  </section>
</template>

<style>
.child1 {
  width: 50%;
  margin: 2rem;
}
</style>

<script>
export default {
  name: 'Child1',
  data() {
    return {};
  },
};
</script>
