<template>
  <div>
    <el-container>
      <el-header>
        <Header @func="getMsgFormSon" @fun="getMsg1FormSon"></Header>
      </el-header>
      <el-main>
        <router-view @keyword="getkey" :keyword="this.keyword"></router-view>

      </el-main>
      <!--      <el-footer>Footer</el-footer>-->
      <!--蒙版-->
      <div class="box-show" :style="{ display: this.boxShadow}" @mousewheel.prevent @touchmove.prevent></div>
    </el-container>
  </div>
</template>

<script>
// 苞米集
//:class="key==1||key==3||key==5?'case-con case-active':'case-con'"
import Header from '@/components/header/Header.vue'

export default {
  name: 'CaseIndex',
  components: {
    Header
  },
  data() {
    return {
      boxShadow:'none',
      isCollapse: 1,
      list:[
        {
          image:require('../../assets/img/corn/shop.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
        {
          image:require('../../assets/img/corn/sf3.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
        {
          image:require('../../assets/img/corn/sf.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
        {
          image:require('../../assets/img/corn/sf4.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
        {
          image:require('../../assets/img/corn/sf2.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
        {
          image:require('../../assets/img/corn/sf5.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
      ],
      keyword:'',
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
    next(){
      this.$router.push({name:'trends'})
    },
    getkey(data){
      // console.log('sed',data)
      this.keyword = data
    },
  },
}
</script>

<style scoped>
.el-header {
  background-color: #24344b;
  color: white;
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
  background-color: #24344b;
  color: white;
  text-align: center;
  width: 100%;
  /*height: 100vh;*/
  /*height: calc(100vh - 80px) !important;*/
  /*position: relative;*/
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

/*!*web*!*/
/*.case-box{*/
/*  width: 100%;*/
/*  !*height: 100%;*!*/
/*  !*background: pink;*!*/
/*  !*position: relative;*!*/
/*}*/
/*.case-title{*/
/*  width: 100%;*/
/*  height: 100px;*/
/*  !*background: #42b983;*!*/
/*  overflow: hidden;*/
/*  box-sizing: border-box;*/
/*  !*position: absolute;*!*/
/*  !*top: 8%;*!*/
/*}*/
/*.case-title p{*/
/*  font-size: 1rem;*/
/*  color: #5b6bdb;*/
/*  margin-top: 6px;*/
/*}*/
/*.case-title h3{*/
/*  font-size: 1.6rem;*/
/*  font-weight: 400;*/
/*  margin: 4px 0;*/
/*}*/
/*.case-g{*/
/*  width: 4%;*/
/*  height: 3px;*/
/*  background: #d1d5fc;*/
/*}*/
/*.case-gs{*/
/*  width: 50%;*/
/*  height: 100%;*/
/*  background: #6979ff;*/
/*  margin: 0;*/
/*}*/
/*.case-gb{*/
/*  width: 2%;*/
/*  height: 3px;*/
/*  background: #d1d5fc;*/
/*  margin-top: 2px;*/
/*}*/
/*.case-gbs{*/
/*  width: 50%;*/
/*  height: 100%;*/
/*  background: #6979ff;*/
/*  margin: 0;*/
/*}*/

/*!*按钮*!*/
/*.case-nav{*/
/*  width: 100%;*/
/*  height: 90px;*/
/*  !*background: #a0813d;*!*/
/*  box-sizing: border-box;*/
/*  overflow: hidden;*/
/*  !*padding-top: 1rem;*!*/
/*}*/
/*.el-radio-group{*/
/*  margin-bottom: 0!important;*/

/*}*/
/*/deep/.el-radio-button:first-child .el-radio-button__inner{*/
/*  border-left: 1px solid #2f415b!important;*/
/*}*/
/*/deep/.el-radio-button__inner{*/
/*  background: #283951;*/
/*  border: 1px solid #2f415b;*/
/*  color: white;*/
/*  padding: 16px 40px;*/
/*}*/
/*/deep/.el-radio-button__orig-radio:checked+.el-radio-button__inner{*/
/*  background: #6979ff;*/
/*  border-color: #6979ff;*/
/*  box-shadow: -1px 0 0 0 #6979ff;*/
/*}*/
/*!*内容*!*/
/*.case-con{*/
/*  width: 60%;*/
/*  height: 900px;*/
/*  !*background: #42b983;*!*/
/*  display: flex;*/
/*  justify-content: space-between;*/
/*  !*flex-flow:column wrap;*!*/
/*  !*object-fit: contain;*!*/
/*  flex-wrap: wrap;*/
/*  overflow: hidden;*/
/*}*/

/*.case-list{*/
/*  width: 100%;*/
/*  height: 314px;*/
/*  !*background: pink;*!*/
/*  cursor: pointer;*/
/*  margin: 0;*/
/*}*/
/*.case-top{*/
/*  width: 100%;*/
/*  height: 194px;*/
/*  !*background: #99a9bf;*!*/
/*}*/
/*.case-top img{*/
/*  width: 100%;*/
/*  height: 100%;*/
/*}*/

/*.case-bottom{*/
/*  width: 100%;*/
/*  height: 120px;*/
/*  background: #f4f4f4;*/
/*  border: 1px solid #f4f4f4;*/
/*  border-top: 1px solid #24344b;*/
/*  box-sizing: border-box;*/
/*  position: relative;*/
/*  overflow: hidden;*/
/*}*/
/*.case-bottom .case-bt-title{*/
/*  color: #24344b;*/
/*  position: absolute;*/
/*  top: 30%;*/
/*  right: 0;*/
/*  bottom: 0;*/
/*  left: 0;*/
/*  margin: auto;*/
/*  !*background: #5b6bdb;*!*/
/*}*/
/*.case-bottom .case-bt-con{*/
/*  color: #8d8e90;*/
/*  position: absolute;*/
/*  top: 50%;*/
/*  right: 0;*/
/*  bottom: 0;*/
/*  left: 0;*/
/*  margin: auto;*/
/*  !*background: #99a9bf;*!*/
/*}*/
/*.case-active{*/
/*  height: 476px;*/
/*}*/
/*.case-active .case-top{*/
/*  width: 100%;*/
/*  height: 356px;*/
/*}*/
/*.case-active .case-bottom{*/
/*  background: #f4f4f4;*/
/*  border: 1px solid #f4f4f4;*/
/*  border-top: 1px solid #24344b;*/
/*}*/
/*.case-active .case-bt-title{*/
/*  color: #24344b;*/
/*}*/

/*.case-ui{*/
/*  width: 32%;*/
/*  height: 812px;*/
/*  !*background: pink;*!*/
/*  cursor: pointer;*/
/*  margin: 0;*/
/*  overflow: hidden;*/
/*  !*display: flex;*!*/
/*  !*flex-wrap: wrap;*!*/
/*}*/
/*.case-list:first-child{*/
/*  margin-bottom: 22px;*/
/*}*/
/*!*按钮*!*/
/*.case-button{*/
/*  width: 120px;*/
/*  height: 2rem;*/
/*  !*background: #5b6bdb;*!*/
/*  border-radius: 30px;*/
/*  line-height: 2rem;*/
/*  overflow: hidden;*/
/*  cursor: pointer;*/
/*  color: #5f616a;*/
/*  border: 1px solid #5f616a;*/
/*  font-size: 1rem;*/
/*}*/

/*!*iphone*!*/

</style>
