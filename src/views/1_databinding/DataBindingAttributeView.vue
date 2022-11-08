<template>
  <div>
    <!-- v-model의 경우 바뀌면 안될 데이터가 사용자에 의해 바뀔수도 있는경우
    , ReadOnly 속성을 사용할 경우 v-bind:속성명 으로 해당하는 속성에만 바인딩 (단방향 바인딩) -->
    <input type="text" name="" id="" v-bind:value="userId" readonly />
    <br><br>

    <!-- ":" 사용으로 v-bind 생략가능 -->
    <input type="text" name="" id="" :value="userId" readonly />
    <br><br>

    <img :src="imgSrc" alt="" style="width:100px; height: auto">
    <br><br>

    <input  type="search" name="" id="" v-model="txt1">
    <button :disabled="txt1 === '' ">조회</button>

  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      userId: 'JAEWOO JEONG',
      imgSrc: 'https://picsum.photos/100',
      txt1: ''
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
