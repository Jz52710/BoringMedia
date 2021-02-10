<template>
  <div>
    <el-container>
      <el-header>
        <Header @func="getMsgFormSon" @fun="getMsg1FormSon"></Header>
      </el-header>
      <el-main>

        <!--web-->
        <div class="web-box">

          <div class="box-top">
            <div class="card-box">
              <div class="top-left">
                <div class="left-title">全链路体验营销设计方法</div>
                <div class="left-log">BoringMedia</div>
                <p class="left-p">体验经济时代，线下体验和线上传播相对独立，造成大量成本浪费及数据流失，我们需要一种基于数据中台的体验及营销设计架构，通过标准的方法及流程，规范引流，互动，体验，传播，转化等要素，以合理的数据监测埋点及分析模型，创造不断迭代升级的文化专属体验模式。</p>
                <div class="left-but" @click="next">联系我们</div>
              </div>
              <div class="top-right"></div>
            </div>
          </div>

          <div class="box-center">
            <div class="box-top">
              <div class="card-box card-active">
                <div class="top-left">
                  <div class="left-title">设计方法说明</div>
                  <!--                  <div class="left-log">BoringMedia</div>-->
                  <p class="left-p">媒趣全链路体验营销设计方法基于大量案例分析及设计方法的研究，可用于构建各种体验及服务体系，应用于零售，汽车及娱乐等行业。帮助吸引您的消费者，推动30-80%的销售增长和300-2,200%的投资回报率。</p>
                  <ul>
                    <li><i class="el-icon-success"></i>&nbsp;吸引触达</li>
                    <li><i class="el-icon-success"></i>&nbsp;趣味互动</li>
                    <li><i class="el-icon-success"></i>&nbsp;体验感知</li>
                    <li><i class="el-icon-success"></i>&nbsp;分享传播</li>
                    <li><i class="el-icon-success"></i>&nbsp;忠诚转换</li>
                    <li><i class="el-icon-success"></i>&nbsp;数据沉淀</li>
                  </ul>
                  <div class="left-but" @click="next">联系我们</div>
                </div>
                <div class="top-right"></div>
              </div>
            </div>
          </div>

          <div class="box-bottom">
            <h1>吸引触达</h1>
            <div class="card-start">
              <!--线-->
              <div class="card-line">
                <div class="card-jd" :style="{height:health + '%'}"></div>
              </div>
              <!--              <div class="card-bt" @click="increase">112312313123</div>-->
              <div class="card-list">
                <div style="width: 50%;height: 100%">
                <el-collapse-transition>
<!--                  <transition name="slideFade">-->
                <div class="card-list-left"  v-show="show">
                  <div class="card-list-left-left">
                    <img :src="image" alt="">
                    <img :src="image" alt="">
                    <img :src="image" alt="">
                  </div>

                  <div class="card-list-left-right">
                    <div class="card-list-x"></div>
                  </div>
                </div>
                  </el-collapse-transition>
<!--                  </transition>-->
                  </div>
                <div class="card-list-center">
                  <div class="card-list-d" @click="show=!show"></div>
                </div>
                <div class="card-list-right">
                  <p class="card-list-right-p">吸引触达</p>
                </div>
              </div>
            </div>

          </div>

        </div>

<!--        <transition name="slideFade">-->
<!--    <div  v-if="isshow" transiton="slideFade" style="background: #99a9bf">123</div>-->
<!--</transition>-->
<!--        <div @click="isshow=!isshow">111</div>-->

        <!--iphone-->

      </el-main>
      <!--      <el-footer>Footer</el-footer>-->
      <!--蒙版-->
      <div class="box-show" :style="{ display: this.boxShadow}"></div>
    </el-container>
  </div>
</template>

<script>
// 全链路卡片
// import HelloWorld from './components/HelloWorld.vue'
import Header from '@/components/header/Header.vue'

export default {
  name: 'CardIndex',
  components: {
    // HelloWorld
    Header
  },
  data() {
    return {
      boxShadow:'none',
      health:20,
      show: true,
      image:require('../../assets/img/card/list1.png'),
      isshow:true,
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
      this.$router.push({name:'concerning'})
    },
    increase(){
      this.health += 10;
      if (this.health > 100) {
        this.health = 100;
      }
    }
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
  /*height: calc(100vh - 80px - 60px) !important;*/
  position: relative;
  padding:0!important;
  margin-top: 80px;
  overflow: hidden;
}
/*蒙版*/
.box-show{
  position: absolute;
  background: black;
  opacity: .6;
  width: 100%;
  height: 100%;
  z-index: 9;
}

/*web*/
.web-box{
  width: 66%;
  height: 100%;
  /*background: #007aff;*/
  overflow: hidden;
  box-sizing: border-box;
}
.box-top{
  width: 100%;
  height: 50vh;
  /*background: pink;*/
  margin: 20px auto;
  /*display: flex;*/
  /*padding: 30px;*/
  box-sizing: border-box;
  overflow: hidden;
  position: relative;
}
.card-box{
  width: 92%;
  height: 500px;
  /*background: #42b983;*/
  display: flex;
  box-sizing: border-box;
  overflow: hidden;
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  margin: auto;
}
.box-top .top-left{
  width: 60%;
  height: 100%;
  /*background: #99a9bf;*/
  text-align: left;
  padding: 6rem;
  box-sizing: border-box;
}
.top-left .left-title{
  color: black;
  font-weight: 600;
  font-size: 1.8rem;
  /*line-height: 1.8rem;*/
  margin-bottom: 1rem;
}
.top-left .left-log{
  width: 200px;
  background: white;
  color: #333333;
  font-weight: 600;
  line-height: 2;
  margin: 0;
  box-shadow: 0 0 4px #333333;
  border-radius: 2px;
  padding: 6px;
  box-sizing: border-box;
}
.top-left .left-p{
  line-height: 1.5;
  box-sizing: border-box;
  margin: 1rem 0;
  /*padding-right: 7rem;*/
}
.top-left .left-but{
  width: 8rem;
  line-height: 46px;
  background: #24262b;
  text-align: center;
  cursor: pointer;
  margin: 0;
  border-radius: 2px;
}
.box-top .top-right{
  width: 40%;
  height: 100%;
  background: url("../../assets/img/card/card.png") no-repeat;
  background-size: contain;
  background-position: center;
}
.left-but:hover{
  background: #333333;
}



/*中间*/
.box-center{
  width: 100%;
  height: 50vh;
  /*background: antiquewhite;*/
  margin: 20px auto;
}
.card-active{
  flex-direction: row-reverse;
}
.box-center .top-right{
  background: url("../../assets/img/card/card1.png") no-repeat;
  background-size: contain;
  background-position: center;
}
.box-center .top-left{
  padding: 4rem;
}
.box-center ul{
  color: #fba600;
  font-size: 1rem;
  margin-bottom: 2rem;
}

/*下面*/
.box-bottom{
  width: 100%;
  height: 168vh;
  background: palegoldenrod;
  margin: 20px auto;
}
.box-bottom h1{
  color: black;
  font-weight: 600;
  font-size: 2rem;
  line-height: 1.5;
}
.card-start{
  width: 100%;
  height: 100%;
  background: pink;
  position: relative;
}
.card-line{
  width: 6px;
  height: 100%;
  background: #24344b;
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  margin: auto;
  border: 1px solid #141c2c;
  box-sizing: border-box;
  border-radius: 10px;
  overflow: hidden;
}
.card-jd{
  background: #eadebc;
  transition: height .6s;
}
.card-bt{
  cursor: pointer;
}
/*开练*/
.card-list{
  width: 100%;
  height: 26vh;
  background: #42b983;
  display: flex;
}
.card-list-left{
  /*width: 50%;*/
  width: 100%;
  height: 100%;
  background: #2c3e50;
  display: flex;

}
.card-list-left-left{
  display: flex;
  justify-content: space-between;
  box-sizing: border-box;
  padding: 10px;
  border-radius: 6px;
  border: 1px solid #f2cf6a;
  overflow: hidden;
}
.card-list-left img{
  width: 30%;
  height: 100%;
}
.card-list-left-right{
  width: 8%;
  height: 100%;
  background: #99a9bf;
  position: relative;
}
.card-list-center{
  width: 4%;
  height: 100%;
  background: palevioletred;
  position: relative;
}
.card-list-x{
  width: 100%;
  height: 2px;
  background: #f2cf6a;
  position: absolute;
  top: 0;
  bottom: 0;
  margin: auto;
}
.card-list-d{
  width: 30px;
  height: 30px;
  background: #f2cf6a;
  border-radius: 50%;
  box-shadow: 0 0 20px #f2cf6a;
  position: absolute;
  top: 0;
  bottom: 0;
  left: -15px;
  margin: auto;
  cursor: pointer;
}
.card-list-right{
  width: 46%;
  height: 100%;
  background: paleturquoise;
  text-align: left;
  position: relative;
}
.card-list-right-p{
  height: 42px;
  position: absolute;
  top: 0;
  bottom: 0;
  margin: auto;
  font-size: 1.8rem;
  letter-spacing:8px

}

/*iphone*/
.slideFade-enter {
    animation: slideFade-dialog-fade-in 0.5s ease;
}
  .slideFade-leave {
    animation: slideFade-dialog-fade-out 0.5s ease forwards;
  }
  .slideFade-enter-active {
    animation: slideFade-dialog-fade-in 0.5s ease;
  }
  .slideFade-leave-active {
    animation: slideFade-dialog-fade-out 0.5s ease forwards;
  }

  @keyframes slideFade-dialog-fade-in {
    0% {
      transform: translate3d(100%, 0, 0);
      /*//修改这个可以控制，上下左右动画，例如：100%为从右到左*/
      opacity: 1;
    }
    100% {
      transform: translate3d(0, 0, 0);
      opacity: 1;
    }
  }
  @keyframes slideFade-dialog-fade-out {
    0% {
      transform: translate3d(0, 0, 0);
      opacity: 1;
    }
    100% {
      transform: translate3d(100%, 0, 0);
      opacity: 1;
    }
  }


</style>
