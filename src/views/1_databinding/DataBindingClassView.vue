<template>
  <div>
    <div>
      <div :class="{ 'text-red': hasError, 'active': isActive }">클래스 바인딩</div>
      <div :class="class2">클래스 바인딩2</div>
    </div>
    <div>
      <button @click="makeError">에러발생</button>
      <button @click="activeOn">활성화</button>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      isActive: false,
      hasError: false,
      class2: ['active', 'hasError']
    }
  },
  setup() { },
  created() { },
  mounted() { },
  unmounted() { },
  methods: {
    makeError() {
      this.hasError === true ? this.hasError = false : this.hasError = true
    },
    activeOn() {
      this.isActive === true ? this.isActive = false : this.isActive = true
    }
  }
}
</script>

<style scoped>
.active {
  background-color: greenyellow;
  font-weight: bold;
}

.text-red {
  color: red;
}
</style>
