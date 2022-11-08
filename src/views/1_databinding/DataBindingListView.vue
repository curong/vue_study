<template>
  <div>
    <div>
      <select name="" id="">
        <option value=""></option>
        <!-- 받을변수 : 배열 선언 , 중복이 없는 key값 지정 -->
        <option :value="city.code" :key="city.code" v-for="city in cities">{{ city.title }}</option>
      </select>
    </div>
    <div>
      <table>
        <thead>
          <tr>
            <th>제품번호</th>
            <th>제품명</th>
            <th>가격</th>
            <th>주문수량</th>
            <th>합계</th>
          </tr>
        </thead>
        <tbody>
          <tr :key="drink.drinkId" v-for="drink in drinkList">

          <!-- 특정한 고유값이 없을 경우 idx 설정가능. -->
          <!-- <tr :key="i" v-for="drink, i in drinkList"> -->
            <td>{{ drink.drinkId }}</td>
            <td>{{ drink.drinkName }}</td>
            <td>{{ drink.price }}</td>
            <td> <input type="number" v-model="drink.qty"> </td>
            <td>{{ drink.price * drink.qty }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      cities: [
        { title: '서울', code: '02' },
        { title: '부산', code: '051' },
        { title: '제주', code: '064' }
      ],
      drinkList: [
        { drinkId: '1', drinkName: '코카콜라', price: 700, qty: 1 },
        { drinkId: '2', drinkName: '환타', price: 800, qty: 3 },
        { drinkId: '3', drinkName: '칠성사이다', price: 600, qty: 5 },
        { drinkId: '4', drinkName: '스프라이트', price: 800, qty: 2 },
        { drinkId: '5', drinkName: '솔의눈', price: 1000, qty: 3 }
      ]
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
