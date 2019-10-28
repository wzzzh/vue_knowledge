<!--模块名称-->
<template>
    <div>
        <el-input type="text" v-model="form.num"></el-input>
        <p>{{ age }}</p>
        <el-button type="primary" @click="handleClick">点击</el-button>
    </div>
</template>

<script>
export default {
  data () {
    return {
      form: {
        num: 0,
        name: 'lili'
      },
      age: 0
    }
  },
  components: {

  },
  mounted () {

  },
  methods: {
    handleClick () {
      //   this.form.num++
      this.$set(this.form, 'sex', '女')
    }
  },
  watch: {
    'form.num': function (newValue, oldValue) {
      this.age = oldValue
    },
    form: {
      handler: function (newValue, oldValue) {
        console.log(newValue, oldValue)
      },
      deep: true,
      immediate: true
    }
  }
}
</script>

<style>
</style>
