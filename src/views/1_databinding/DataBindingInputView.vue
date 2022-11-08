<template>
  <div>
    <!-- v-model 태그를 사용할 경우 data() 함수안의 값을 사용한다. (v-model 사용 시 양방향 데이터 바인딩) -->
    <!-- 값을 수정하면 자동으로 값이 바뀌어있으며 사용자가 값을 바꾸어도 자동으로 바뀐다. -->
    <!-- document 조회하지 않아도 값을 확인가능 -->
    <!-- 양방향데이터 바인딩과 Virtual DOM을 모두 사용. 속도에서 이점 발휘 -->
    <input @change="myFunction" type="text" v-model="userId" /> <!-- 전달 할 파라미터가 없을경우 myFunction() 함수의 '()' 괄호를 생략가능 -->
    <button @click="changeData">변경</button>
    <br>
    <br>
    <input type="text" v-model="num1" /> +
    <input type="text" v-model="num2" />
    <span> {{ num1 + num2 }}</span>
    <br>
    <!-- 숫자값을 계산 시 v-model.number 태그를 사용할 경우 자동으로 parseInt() 처리를 해준다. -->
    <input type="text" v-model.number="num3" /> +
    <input type="text" v-model.number="num4" />
    <span>{{ num3 + num4 }}</span>
  </div>
</template>

<script>
export default {
  compornents: {},
  data() {
    return {
      userId: 'JAEWOO JEONG',
      num1: 0,
      num2: 0,
      num3: 0,
      num4: 0,
      num5: 0
    }
  },
  setup() { },
  create() { },
  mounted() { },
  methods: {
    myFunction() {
      /* Object 접근 시 this를 사용하여 해당하는 VUE를 선택하여 값을 가져올 수 있음. (data함수 안의 변수.)  */
      console.log(this.userId)
    },
    changeData() {
      switch (this.userId) {
        case 'JAEWOO JEONG': this.userId = 'DATA 변경!'
          break
        default: this.userId = 'JAEWOO JEONG'
      }
    }
  }
}
</script>

<style>

</style>
