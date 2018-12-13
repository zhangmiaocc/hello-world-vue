<template>
  <div class="about">
    <h1 @click="clickHandler">This is an about page</h1>

    <div>{{ message }}</div>
    <div>{{ message2 }}</div>
  </div>
</template>

<script>
export default {
  // 接受父组件参数
  props: {
    propName: {
      type: Number,
      default: 0
    },
    propName2: ''
  },
  components:[],
  data() {
    return {
      message: 'Hello Vue!',
      message2: 'Hello Vue!'
    }
  },
  // 计算属性，依赖于data
  computed: {
    name() {
      return this.message+' '+this.message2
    },
    name2:{
      get:function(){
        return this.message+' '+this.message2
      },
      set: function(val){
        this.message = val
      }
    }
  },
  watch: {
    message(newValue, oldValue) { },
    message2(val){},
    name(val){}
  },
  created(){},
  mounted(){},
  methods: {
    clickHandler() {
      this.message = 'xxxxxx'
    }
  },
};
</script>

