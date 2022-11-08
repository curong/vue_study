<template>
  <div>
    <select v-model="selectData" name="" id="">
      <option value="">---</option>
      <option value="02">서울</option>
      <option value="051">부산</option>
      <option value="064">제주</option>
    </select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectData: '051'
    }
  }
}
</script>

<style>

</style>
