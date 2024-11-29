<template>
  <div v-for="(b,i) in blogData" :key="i">
    <h5 @click="$router.push(('/detail/0'))">{{b.title}}</h5>
    <p>{{b.date}}</p>
  </div>
</template>

<script>
export default {
  name: 'List',
  props: {
    blogData: Array,
  },
  components: {
  }
}
</script>

<style>

</style>