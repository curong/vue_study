<template>
  <div>
    <!-- <input type="search" @keyup="checkEnter($event)" v-model="searchText" /> -->
    <input type="search" @keyup.enter="doSearch" v-model="searchText" />
    <input type="search" @keyup.ctrl.enter="doSearch" v-model="searchText" />
    <button @click="doSearch">조회</button>
    <button type="submit" @click.prevent="doSearch">Prevent</button>
  </div>
</template>
<!--
  1. .enter
  2. .tab
  3. .delete
  4. .esc
  5. .space
  6. .up
  7. .down
  8. .left
  9. .right
  10. .ctrl (컨트롤 키)
  11. .stop - event.stopPropagation()
 -->
<script>
export default {
  components: {},
  data() {
    return {
      searchText: ''
    }
  },
  setup() { },
  created() { },
  mounted() { },
  unmounted() { },
  methods: {
    doSearch() {
      console.log(this.searchText)
      this.searchText = ''
    },
    checkEnter(event) {
      if (event.keyCode === 13) {
        this.doSearch()
      }
    }
  }
}
</script>

<style scoped>

</style>
