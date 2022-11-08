<template>
  <div>
    <h1> Hello {{ userName }}</h1>
    <p> {{ message }} </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userName: 'Jaewoo Jeong',
      message: 'VUE 공부중',
      arr: [],
      obj: {}
    }
  }
}
</script>

<style scoped>

</style>
