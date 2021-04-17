<template>
  <section class="child1">
    <h1>Child 1</h1>
    Číslo v Child2: {{ num }}
    <div v-for="post in posts" v-bind:key="post.id" v-show="post.id === numero">
      <h2>{{ post.title }}</h2>
    </div>
  </section>
</template>

<style>
.child1 {
  width: 48%;
  margin: 2rem;
}
</style>

<script>
export default {
  name: 'Child1',
  props: ['num'],
  data() {
    return {
      posts: [
        { id: 1, title: 'Den první' },
        { id: 2, title: 'Den druhý' },
        { id: 3, title: 'Den třetí' },
        { id: 4, title: 'Den čtvrtý' },
      ],
      numero: this.num,
    };
  },
};
</script>
