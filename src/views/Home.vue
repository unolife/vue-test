<template>
  <div>
    <h1>Welcome to {{title2}}</h1>
    <input type="text" v-model="input1" />
    <button type="button" @click="getData">Get</button>
    <button type="button" @click="setData">Set</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: '개발자의 품격',
      title2: 'Seoul',
      input1: '이메일',
    };
  },
  watch: {
    input1() {
      console.log(this.input1);
    },
    title() {},
  },
  methods: { // vue는 two-way 바인딩이 가능함
    getData() {
      alert(this.input1); // 메소드 안에서 데이터 접근하려면 this를 써야함
    },
    setData() {
      this.input1 = '12345';
    }
  },
  beforeCreate() {
    console.log('before create');
  },
  created() {
    console.log('created');
  },
  beforeMount(){},
  mounted(){},
  beforeUpdate(){},
  updated(){},
  beforeDestroy(){},
  destroyed(){},
};
</script>