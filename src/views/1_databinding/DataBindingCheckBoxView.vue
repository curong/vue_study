<template>
  <!-- CheckBox의 경우에는 v-model과 연결 시 Value의 데이터와 바인딩 되는것이 아닌 checked와 바인딩 되며 true일 경우 value값을 binding 시켜준다. -->
  <div>
    <div>
      <input type="checkbox" name="" id="html" value="HTML" v-model="favoriteLang" />
      <label for="html">HTML</label>
    </div>
    <div>
      <input type="checkbox" name="" id="css" value="CSS" v-model="favoriteLang" />
      <label for="css">CSS</label>
    </div>
    <div>
      <input type="checkbox" name="" id="js" value="JS" v-model="favoriteLang" />
      <label for="js">JS</label>
    </div>
    <div>선택한 지역: {{ favoriteLang }}</div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      /* Default 값으로 값을 넣어 줄 경우 체크 된 상태 */
      favoriteLang: ['JS']
    }
  },
  setup() { },
  created() { },
  mounted() { },
  unmounted() { },
  methods: {}
}
</script>

<style scoped>

</style>
