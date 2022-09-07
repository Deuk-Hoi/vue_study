<template>
  <div>
    <div>
      <select>
        <option :key="city.code" :value="city.code" v-for="city in cities">
          {{ city.title }}
        </option>
      </select>
    </div>
    <div>
      <table>
        <thead>
          <th>주문번호</th>
          <th>상품이름</th>
          <th>가격</th>
          <th>제품수량</th>
          <th>합계</th>
        </thead>
        <tbody>
          <tr :key="drink.drinkId" v-for="drink in drinkList">
            <td>{{ drink.drinkId }}</td>
            <td>{{ drink.drinkName }}</td>
            <td>{{ drink.price }}</td>
            <td><input type="number" v-model="drink.qty" /></td>
            <td>{{ drink.qty * drink.price }}</td>
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
        {
          title: '서울',
          code: '02'
        },
        {
          title: '부산',
          code: '053'
        },
        {
          title: '제주',
          code: '064'
        }
      ],
      drinkList: [
        {
          drinkId: 1,
          drinkName: '아메리카노',
          price: 2000,
          qty: 1
        },

        {
          drinkId: 2,
          drinkName: '레몬에이드',
          price: 3500,
          qty: 1
        },

        {
          drinkId: 3,
          drinkName: '플레인요거트',
          price: 4000,
          qty: 2
        },

        {
          drinkId: 4,
          drinkName: '초코라떼',
          price: 3500,
          qty: 4
        }
      ]
    }
  },
  setup() {},
  create() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
