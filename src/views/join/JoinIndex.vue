<template>
  <div>
    <el-container>
      <el-header>
        <Header @func="getMsgFormSon" @fun="getMsg1FormSon"></Header>
      </el-header>
      <el-main>
        加入我们
      </el-main>
      <el-footer>Footer</el-footer>
      <!--蒙版-->
      <div class="box-show" :style="{ display: this.boxShadow}" @mousewheel.prevent @touchmove.prevent></div>
    </el-container>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from '@/components/header/Header.vue'

export default {
  name: 'JoinIndex',
  components: {
    // HelloWorld
    Header
  },
  data() {
    return {
      boxShadow:'none',
    };
  },
  methods: {
    getMsgFormSon(data){
      this.boxShadow = data
      // console.log(this.boxShadow)
    },
    getMsg1FormSon(data){
      this.boxShadow = data
      // console.log(this.boxShadow)
    },
  },
}
</script>

<style scoped>
.el-header {
  background-color: #B3C0D1;
  color: #333;
  text-align: center;
  line-height: 80px!important;
  width: 100%;
  height: 80px!important;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 99;
  padding: 0!important;
}
.el-footer{
  background-color: #B3C0D1;
  color: #333;
  text-align: center;
  line-height: 60px;
  width: 100%;
  height: 100%;
}
.el-main {
  background-color: #E9EEF3;
  color: #333;
  text-align: center;
  width: 100%;
  /*height: 100vh;*/
  height: calc(100vh - 80px - 60px) !important;
  position: relative;
  padding:0!important;
  margin-top: 80px;
}
/*蒙版*/
.box-show{
  position: fixed;
  background: black;
  opacity: .6;
  width: 100%;
  height: 100%;
  z-index: 9;
}
</style>
