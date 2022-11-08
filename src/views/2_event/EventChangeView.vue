<template>
  <div>
    <!-- 방법 - 1 -->
    <select @change="changeCity($event)" v-model="selectedCity">
      <!-- 방법 - 2 -->
    <!-- <select v-on:change="changeCity" v-model="selectedCity"> -->
      <option value=""> == 도시선택 ==</option>
      <option :value="city.cityCode" :key="city.cityCode" v-for="city in cityList">{{ city.title }}</option>
    </select>
    <!-- 협업 시에는 change 이벤트를 사용하여 구현하는것이 다른사람이 볼때 분석이 쉽다. -->
    <select>
      <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in selectedDongList">
        {{ dong.dongTitle }} </option>
    </select>
    <!-- 메소드를 생성하지 않고 바로 변경하는방법 -->
    <select>
      <option :value="dong.dongCode" :key="dong.dongCode"
        v-for="dong in dongList.filter(dong => dong.cityCode === this.selectedCity)">{{ dong.dongTitle }}</option>
    </select>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      selectedCity: [],
      cityList: [
        { cityCode: '02', title: '서울' },
        { cityCode: '051', title: '부산' },
        { cityCode: '064', title: '제주' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: '인헌동' },
        { cityCode: '02', dongCode: '2', dongTitle: '역삼동' },
        { cityCode: '02', dongCode: '3', dongTitle: '마포동' },
        { cityCode: '051', dongCode: '4', dongTitle: '대연동' },
        { cityCode: '051', dongCode: '5', dongTitle: '남포동' },
        { cityCode: '051', dongCode: '6', dongTitle: '망미동' },
        { cityCode: '051', dongCode: '7', dongTitle: '제송동' },
        { cityCode: '064', dongCode: '8', dongTitle: '제주 1동' },
        { cityCode: '064', dongCode: '9', dongTitle: '제주 2동' },
        { cityCode: '064', dongCode: '10', dongTitle: '제주 3동' },
        { cityCode: '064', dongCode: '11', dongTitle: '제주 4동' }
      ],
      selectedDongList: []

    }
  },
  setup() { },
  created() { },
  mounted() { },
  unmounted() { },
  methods: {
    changeCity(event) {
      console.log(event.target.tagName)
      this.selectedDongList = this.dongList.filter(dong => dong.cityCode === this.selectedCity)
    }
  }
}
</script>

<style scoped>

</style>
