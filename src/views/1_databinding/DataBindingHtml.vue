<template>
  <div>
    <!-- VUE에서 InnerText로 값을 바인딩 -->
    <div> {{ htmlBinding }} </div>

    <!-- 1. Vue의 Directive를 사용하여 해당하는 데이터를 바인딩 -->
    <!-- 2. v-html을 사용 시 InnerHtml로 넣어줌 -->
    <!-- 3. Div => htmlBinding HTML형식으로 바인딩 -->
    <div v-html="htmlBinding"></div>
  </div>
</template>

<script>
export default {
  /* 앞으로 VUE에서 가장 많이보게 될 형태 */
  compornents: {},
  data() {
    return {
      htmlBinding: '<p style="color: red">빨간색 문자</p>'
    }
  },
  setup() { },
  create() { },
  mounted() { },
  moethod() { }

}
</script>

<style>

</style>
