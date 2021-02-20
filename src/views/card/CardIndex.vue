<template>
  <div>
    <el-container>
      <el-header>
        <Header @func="getMsgFormSon" @fun="getMsg1FormSon"></Header>
      </el-header>
      <el-main>

        <!--web-->
        <div class="web-box hidden-sm-and-down">

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
          <!--卡片流程-->
          <div class="xy-size">
            <h1>吸引触达</h1>
          </div>

          <div class="box-bottom">
            <div class="card-start">
              <!--线-->
              <div class="card-line">
                <div class="card-jd" :style="{height:health + '%'}"></div>
              </div>
              <!--吸引触达-->
              <div class="card-list">
                <!--                <transition name="carHistory">-->
                <div style="width: 50%;height: 100%">
                  <!--                <el-collapse-transition>-->
                  <transition name="carHistory">
                    <div class="card-list-left"  v-show="show">
                      <div class="card-list-left-left">
                        <img :src="image1" alt="">
                        <img :src="image2" alt="">
                        <img :src="image3" alt="">
                      </div>

                      <div class="card-list-left-right">
                        <div class="card-list-x"></div>
                      </div>
                    </div>
                    <!--                  </el-collapse-transition>-->
                  </transition>
                </div>
                <!--                  </transition>-->
                <div class="card-list-center">
                  <div class="card-list-d card-list-d-to" @click="increase"></div>
                </div>
                <div class="card-list-right">
                  <p class="card-list-right-p">吸引触达</p>
                </div>
              </div>
              <!--趣味互动-->
              <div class="card-list card-list-active">
                <!--                <transition name="carHistory">-->
                <div style="width: 50%;height: 100%">
                  <!--                <el-collapse-transition>-->
                  <transition name="carHistoryleft">
                    <div class="card-list-left card-list-left-active"  v-show="show1">
                      <div class="card-list-left-left">
                        <img :src="image4" alt="">
                        <img :src="image5" alt="">
                        <img :src="image6" alt="">
                      </div>

                      <div class="card-list-left-right">
                        <div class="card-list-x"></div>
                      </div>
                    </div>
                    <!--                  </el-collapse-transition>-->
                  </transition>
                </div>
                <!--                  </transition>-->
                <div class="card-list-center">
                  <div class="card-list-d card-list-d-active" @click="increase1" v-show="btn"></div>
                </div>
                <div class="card-list-right">
                  <p class="card-list-right-p card-list-right-p-active" :style="{opacity: transparent1}">趣味互动</p>
                </div>
              </div>
              <!--体验感知-->
              <div class="card-list card-list-active-one">
                <!--                <transition name="carHistory">-->
                <div style="width: 50%;height: 100%">
                  <!--                <el-collapse-transition>-->
                  <transition name="carHistory">
                    <div class="card-list-left"  v-show="show2">
                      <div class="card-list-left-left card-list-left-left-active">
                        <img :src="image7" alt="">
                        <img :src="image8" alt="">
                        <!--                        <img :src="image" alt="">-->
                      </div>

                      <div class="card-list-left-right card-list-left-right-active">
                        <div class="card-list-x"></div>
                      </div>
                    </div>
                    <!--                  </el-collapse-transition>-->
                  </transition>
                </div>
                <!--                  </transition>-->
                <div class="card-list-center">
                  <div class="card-list-d card-list-d-to" @click="increase2" v-show="btn1"></div>
                </div>
                <div class="card-list-right">
                  <p class="card-list-right-p" :style="{opacity: transparent2}">体验感知</p>
                </div>
              </div>
              <!--分享传播-->
              <div class="card-list card-list-active card-list-active-two">
                <!--                <transition name="carHistory">-->
                <div style="width: 50%;height: 100%">
                  <!--                <el-collapse-transition>-->
                  <transition name="carHistoryleft">
                    <div class="card-list-left card-list-left-active"  v-show="show3">
                      <div class="card-list-left-left">
                        <img :src="image9" alt="">
                        <img :src="image10" alt="">
                        <img :src="image11" alt="">
                      </div>

                      <div class="card-list-left-right">
                        <div class="card-list-x"></div>
                      </div>
                    </div>
                    <!--                  </el-collapse-transition>-->
                  </transition>
                </div>
                <!--                  </transition>-->
                <div class="card-list-center">
                  <div class="card-list-d card-list-d-active" @click="increase3" v-show="btn2"></div>
                </div>
                <div class="card-list-right">
                  <p class="card-list-right-p card-list-right-p-active" :style="{opacity: transparent3}">分享传播</p>
                </div>
              </div>
              <!--忠诚转换-->
              <div class="card-list card-list-active-one card-list-active-top">
                <!--                <transition name="carHistory">-->
                <div style="width: 50%;height: 100%">
                  <!--                <el-collapse-transition>-->
                  <transition name="carHistory">
                    <div class="card-list-left"  v-show="show4">
                      <div class="card-list-left-left card-list-left-left-active">
                        <img :src="image12" alt="">
                        <img :src="image13" alt="">
                        <!--                        <img :src="image" alt="">-->
                      </div>

                      <div class="card-list-left-right card-list-left-right-active">
                        <div class="card-list-x"></div>
                      </div>
                    </div>
                    <!--                  </el-collapse-transition>-->
                  </transition>
                </div>
                <!--                  </transition>-->
                <div class="card-list-center">
                  <div class="card-list-d card-list-d-to" @click="increase4" v-show="btn3"></div>
                </div>
                <div class="card-list-right">
                  <p class="card-list-right-p" :style="{opacity: transparent4}">忠诚转换</p>
                </div>
              </div>

            </div>
            <!--最后一个-->
            <div class="card-bottom">
              <div class="dian" v-show="btn4" @click="increase5"></div>
              <div class="card-bt-img" :style="{opacity:transparent}">
                <img :src="image14" alt="">
              </div>
            </div>

          </div>

        </div>


        <!--iphone-->
        <div class="iphone-box hidden-md-and-up">
          <!--上面-->
          <div class="iphone-box-top">
            <div class="iphone-card-box">
              <div class="iphone-top-left">
                <div class="iphone-left-title">全链路体验营销设计方法</div>
                <div class="iphone-left-log">BoringMedia</div>
                <p class="iphone-left-p">体验经济时代，线下体验和线上传播相对独立，造成大量成本浪费及数据流失，我们需要一种基于数据中台的体验及营销设计架构，通过标准的方法及流程，规范引流，互动，体验，传播，转化等要素，以合理的数据监测埋点及分析模型，创造不断迭代升级的文化专属体验模式。</p>
                <div class="iphone-left-but" @click="next">联系我们</div>
              </div>
              <div class="iphone-top-right"></div>
            </div>
          </div>
          <!--上面2-->
          <div class="iphone-box-center">
            <div class="iphone-box-top iphone-active">
              <div class="iphone-card-box card-active">
                <div class="iphone-top-left">
                  <div class="iphone-left-title">设计方法说明</div>
                  <!--                  <div class="left-log">BoringMedia</div>-->
                  <p class="iphone-left-p">媒趣全链路体验营销设计方法基于大量案例分析及设计方法的研究，可用于构建各种体验及服务体系，应用于零售，汽车及娱乐等行业。帮助吸引您的消费者，推动30-80%的销售增长和300-2,200%的投资回报率。</p>
                  <ul>
                    <li><i class="el-icon-success"></i>&nbsp;吸引触达</li>
                    <li><i class="el-icon-success"></i>&nbsp;趣味互动</li>
                    <li><i class="el-icon-success"></i>&nbsp;体验感知</li>
                    <li><i class="el-icon-success"></i>&nbsp;分享传播</li>
                    <li><i class="el-icon-success"></i>&nbsp;忠诚转换</li>
                    <li><i class="el-icon-success"></i>&nbsp;数据沉淀</li>
                  </ul>
<!--                  <div class="iphone-left-but" @click="next">联系我们</div>-->
                </div>
                <div class="iphone-top-right"></div>
              </div>
            </div>
          </div>
          <!--卡片流程-->
          <div class="iphone-xy-size">
            <h1>吸引触达</h1>
          </div>

          <div class="iphone-box-bottom">
            <div class="iphone-card-start">
              <!--线-->
              <div class="iphone-card-line">
                <div class="iphone-card-jd" :style="{height:health + '%'}"></div>
              </div>
              <!--吸引触达-->
              <div class="iphone-card-list">
                <!--                <transition name="carHistory">-->
                <div class="iphone-new">
                  <!--                <el-collapse-transition>-->
                  <transition name="carHistory">
                    <div class="iphone-card-list-left"  v-show="show">
                      <div class="iphone-card-list-left-left">
                        <img :src="image1" alt="">
                        <img :src="image2" alt="">
                        <img :src="image3" alt="">
                      </div>

                      <div class="iphone-card-list-left-right">
                        <div class="iphone-card-list-x"></div>
                      </div>
                    </div>
                    <!--                  </el-collapse-transition>-->
                  </transition>
                </div>
                <!--                  </transition>-->
                <div class="iphone-card-list-center">
                  <div class="iphone-card-list-d iphone-card-list-d-to" @click="increase"></div>
                </div>
<!--                <div class="iphone-card-list-right">-->
<!--                  <p class="iphone-card-list-right-p">吸引触达</p>-->
<!--                </div>-->
              </div>
              <!--趣味互动-->
              <div class="iphone-card-list iphone-card-list-active">
                <!--                <transition name="carHistory">-->
                <div  class="iphone-new">
                  <!--                <el-collapse-transition>-->
                  <transition name="carHistoryleft">
                    <div class="iphone-card-list-left iphone-card-list-left-active"  v-show="show1">
                      <div class="iphone-card-list-left-left">
                        <img :src="image4" alt="">
                        <img :src="image5" alt="">
                        <img :src="image6" alt="">
                      </div>

                      <div class="iphone-card-list-left-right">
                        <div class="iphone-card-list-x"></div>
                      </div>
                    </div>
                    <!--                  </el-collapse-transition>-->
                  </transition>
                </div>
                <!--                  </transition>-->
                <div class="iphone-card-list-center">
                  <div class="iphone-card-list-d" @click="increase1" v-show="btn"></div>
                </div>
<!--                <div class="iphone-card-list-right">-->
<!--                  <p class="iphone-card-list-right-p iphone-card-list-right-p-active" :style="{opacity: transparent1}">趣味互动</p>-->
<!--                </div>-->
              </div>
              <!--体验感知-->
              <div class="iphone-card-list iphone-card-list-active-one">
                <!--                <transition name="carHistory">-->
                <div  class="iphone-new">
                  <!--                <el-collapse-transition>-->
                  <transition name="carHistoryleft">
                    <div class="iphone-card-list-left"  v-show="show2">
                      <div class="iphone-card-list-left-left iphone-card-list-left-left-active">
                        <img :src="image7" alt="">
                        <img :src="image8" alt="">
                        <!--                        <img :src="image" alt="">-->
                      </div>

                      <div class="iphone-card-list-left-right iphone-card-list-left-right-active">
                        <div class="iphone-card-list-x"></div>
                      </div>
                    </div>
                    <!--                  </el-collapse-transition>-->
                  </transition>
                </div>
                <!--                  </transition>-->
                <div class="iphone-card-list-center">
                  <div class="iphone-card-list-d iphone-card-list-d-to" @click="increase2" v-show="btn1"></div>
                </div>
<!--                <div class="iphone-card-list-right">-->
<!--                  <p class="iphone-card-list-right-p" :style="{opacity: transparent2}">体验感知</p>-->
<!--                </div>-->
              </div>
              <!--分享传播-->
              <div class="iphone-card-list iphone-card-list-active iphone-card-list-active-two">
                <!--                <transition name="carHistory">-->
                <div  class="iphone-new">
                  <!--                <el-collapse-transition>-->
                  <transition name="carHistoryleft">
                    <div class="iphone-card-list-left iphone-card-list-left-active"  v-show="show3">
                      <div class="iphone-card-list-left-left">
                        <img :src="image9" alt="">
                        <img :src="image10" alt="">
                        <img :src="image11" alt="">
                      </div>

                      <div class="iphone-card-list-left-right">
                        <div class="iphone-card-list-x"></div>
                      </div>
                    </div>
                    <!--                  </el-collapse-transition>-->
                  </transition>
                </div>
                <!--                  </transition>-->
                <div class="iphone-card-list-center">
                  <div class="iphone-card-list-d" @click="increase3" v-show="btn2"></div>
                </div>
<!--                <div class="iphone-card-list-right">-->
<!--                  <p class="iphone-card-list-right-p iphone-card-list-right-p-active" :style="{opacity: transparent3}">分享传播</p>-->
<!--                </div>-->
              </div>
              <!--忠诚转换-->
              <div class="iphone-card-list iphone-card-list-active-one iphone-card-list-active-top">
                <!--                <transition name="carHistory">-->
                <div  class="iphone-new">
                  <!--                <el-collapse-transition>-->
                  <transition name="carHistoryleft">
                    <div class="iphone-card-list-left"  v-show="show4">
                      <div class="iphone-card-list-left-left iphone-card-list-left-left-active">
                        <img :src="image12" alt="">
                        <img :src="image13" alt="">
                        <!--                        <img :src="image" alt="">-->
                      </div>

                      <div class="iphone-card-list-left-right iphone-card-list-left-right-active">
                        <div class="iphone-card-list-x"></div>
                      </div>
                    </div>
                    <!--                  </el-collapse-transition>-->
                  </transition>
                </div>
                <!--                  </transition>-->
                <div class="iphone-card-list-center">
                  <div class="iphone-card-list-d iphone-card-list-d-to" @click="increase4" v-show="btn3"></div>
                </div>
<!--                <div class="iphone-card-list-right">-->
<!--                  <p class="iphone-card-list-right-p" :style="{opacity: transparent4}">忠诚转换</p>-->
<!--                </div>-->
              </div>

            </div>
            <!--最后一个-->
            <div class="iphone-card-bottom">
              <div class="iphone-dian" v-show="btn4" @click="increase5"></div>
              <div class="iphone-card-bt-img" :style="{opacity:transparent}">
                <img :src="image14" alt="">
              </div>
            </div>

          </div>


        </div>


      </el-main>
      <!--      <el-footer>Footer</el-footer>-->
      <!--蒙版-->
      <div class="box-show" :style="{ display: this.boxShadow}" @mousewheel.prevent @touchmove.prevent></div>
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
      health:10,
      show: true,
      show1: false,
      show2: false,
      show3: false,
      show4: false,
      show5: false,
      image1:require('../../assets/img/card/list1.png'),
      image2:require('../../assets/img/card/list2.png'),
      image3:require('../../assets/img/card/list3.png'),
      image4:require('../../assets/img/card/list4.png'),
      image5:require('../../assets/img/card/list5.png'),
      image6:require('../../assets/img/card/list6.png'),
      image7:require('../../assets/img/card/list7.png'),
      image8:require('../../assets/img/card/list8.png'),
      image9:require('../../assets/img/card/list9.png'),
      image10:require('../../assets/img/card/list10.png'),
      image11:require('../../assets/img/card/list11.png'),
      image12:require('../../assets/img/card/list12.png'),
      image13:require('../../assets/img/card/list13.png'),
      image14:require('../../assets/img/card/list14.png'),
      // isshow:true,
      btn: false,
      btn1: false,
      btn2: false,
      btn3: false,
      btn4: false,
      //透明
      transparent:0,
      transparent1:0,
      transparent2:0,
      transparent3:0,
      transparent4:0,
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
      this.health += 20;
      if (this.health > 100) {
        this.health = 100;
      }
      // this.show = true;
      this.btn = true;
      this.transparent1 = 1;
    },
    increase1(){
      this.health += 20;
      if (this.health > 100) {
        this.health = 100;
      }
      this.show1 = true;
      this.btn1 = true;
      this.transparent2 = 1;
    },
    increase2(){
      this.health += 20;
      if (this.health > 100) {
        this.health = 100;
      }
      this.show2 = true;
      this.btn2 = true;
      this.transparent3 = 1;
    },
    increase3(){
      this.health += 20;
      if (this.health > 100) {
        this.health = 100;
      }
      this.show3 = true;
      this.btn3 = true;
      this.transparent4 = 1;
    },
    increase4(){
      this.health += 20;
      if (this.health > 100) {
        this.health = 100;
      }
      this.show4 = true;
      this.btn4 = true;
      // this.transparent5 = 1;
    },
    increase5(){
      // this.show5 = !this.show5
      this.transparent = 1
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
  /*height: calc(100vh - 80px - 60px) !important;*/
  position: relative;
  padding:0!important;
  margin-top: 80px;
  overflow: hidden;
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
/*字*/
.xy-size{
  /*background: #42b983;*/
}
.xy-size h1{
  color: black;
  font-weight: 600;
  font-size: 2rem;
  line-height: 1.5;
}

/*下面*/
.box-bottom{
  width: 100%;
  height: 180vh;
  /*background: palegoldenrod;*/
  margin: 20px auto;
  margin-bottom: 40px;
  overflow: hidden;
  box-sizing: border-box;
}
.box-bottom h1{

}
.card-start{
  width: 100%;
  height: 80%;
  /*background: pink;*/
  position: relative;
  box-sizing: border-box;
  overflow: hidden;
}
.card-line{
  width: 6px;
  height: 100%;
  background: #24344b;
  position: absolute;
  /*top: 0;*/
  /*bottom: 0;*/
  right: 0;
  left: 0;
  margin: auto;
  border: 1px solid #141c2c;
  box-sizing: border-box;
  border-radius: 10px;
  overflow: hidden;
  z-index: 9;
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
  /*background: #42b983;*/
  display: flex;
  position: absolute;
  top: 1%;
}
.card-list-left{
  /*width: 50%;*/
  width: 100%;
  height: 100%;
  background: #24344b;
  display: flex;
  /*opacity: 0;*/
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
  /*background: #99a9bf;*/
  position: relative;
}
.card-list-center{
  width: 4%;
  height: 100%;
  background: #24344b;
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

  margin: auto;
  cursor: pointer;
  z-index: 9;
}
.card-list-d-to{
  left: -15px;
}
.card-list-right{
  width: 46%;
  height: 100%;
  background: #24344b;
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
  letter-spacing:8px;
  transition: opacity .3s;
}
/*右面list*/
.card-list-active{
  top: 21%;
  flex-direction: row-reverse;
}
.card-list-left-active{
  flex-direction: row-reverse;
}
.card-list-d-active{
  right: -15px;
  /*left: 0!important;*/
}
.card-list-right-p-active{
  right: 0;
}
.card-list-active-one{
  top: 41%;
}
.card-list-active-two{
  top: 61%;
}
.card-list-active-top{
  top: 81%;
}
/*左面图*/
.card-list-left-right-active{
  width: 56%;
}
.card-list-left-left-active img{
  margin: 0;
  width: 48%;
}

/*下面*/
.card-bottom{
  width: 100%;
  height: 20%;
  /*background: #42b983;*/
  position: relative;
  /*box-sizing: border-box;*/
  /*overflow: hidden;*/
}
.card-bottom .dian{
  width: 30px;
  height: 30px;
  background: #f2cf6a;
  border-radius: 50%;
  box-shadow: 0 0 20px #f2cf6a;
  position: absolute;
  left: 0;
  right: 0;
  top: -15px;
  margin: auto;
  cursor: pointer;
  z-index: 9;
}
.card-bottom .card-bt-img{
  width: 30%;
  height: 100%;
  /*background: #99a9bf;*/
  /*margin-top: 15px;*/
  padding-top: 2rem;
  box-sizing: border-box;
  opacity: 0;
  transition: opacity .3s;
  /*overflow: hidden;*/
}
.card-bottom .card-bt-img img{
  width: 58%;
}

/*动画*/
/*右到左*/
.carHistory-enter {
  animation: carHistory-dialog-fade-in 0.3s ease;
}
.carHistory-leave {
  animation: carHistory-dialog-fade-out 0.3s ease forwards;
}
.carHistory-enter-active {
  animation: carHistory-dialog-fade-in 0.3s ease;
}
.carHistory-leave-active {
  animation: carHistory-dialog-fade-out 0.3s ease forwards;
}

@keyframes carHistory-dialog-fade-in {
  0% {
    transform: translate3d(100%, 0, 0);
    /*修改这个控制左右*/
    opacity: 1;
    /*transition: opacity .3s;*/
  }
  100% {
    transform: translate3d(0, 0, 0);
    opacity: 1;
    /*transition: opacity .3s;*/
  }
}
@keyframes carHistory-dialog-fade-out {
  0% {
    transform: translate3d(0, 0, 0);
    opacity: 1;
    /*transition: opacity .3s;*/
  }
  100% {
    transform: translate3d(100%, 0, 0);
    opacity: 1;
    /*transition: opacity .3s;*/
  }
}
/*左到右*/
.carHistoryleft-enter {
  animation: carHistoryleft-dialog-fade-in 0.3s ease;
}
.carHistoryleft-leave {
  animation: carHistoryleft-dialog-fade-out 0.3s ease forwards;
}
.carHistoryleft-enter-active {
  animation: carHistoryleft-dialog-fade-in 0.3s ease;
}
.carHistoryleft-leave-active {
  animation: carHistoryleft-dialog-fade-out 0.3s ease forwards;
}

@keyframes carHistoryleft-dialog-fade-in {
  0% {
    transform: translate3d(-100%, 0, 0);
    /*修改这个控制左右*/
    opacity: 1;
    /*transition: opacity .3s;*/
  }
  100% {
    transform: translate3d(0, 0, 0);
    opacity: 1;
    /*transition: opacity .3s;*/
  }
}
@keyframes carHistoryleft-dialog-fade-out {
  0% {
    transform: translate3d(0, 0, 0);
    opacity: 1;
    /*transition: opacity .3s;*/
  }
  100% {
    transform: translate3d(-100%, 0, 0);
    opacity: 1;
    /*transition: opacity .3s;*/
  }
}


/*iphone*/
.iphone-box{
  width: 94%;
  /*height: 300vh;*/
  /*background: paleturquoise;*/
  overflow: hidden;
  box-sizing: border-box;
}
.iphone-box-top{
  width: 100%;
  height: 100vh;
  /*background: pink;*/
  margin: 20px auto;
  /*display: flex;*/
  /*padding: 30px;*/
  box-sizing: border-box;
  overflow: hidden;
  position: relative;
}
.iphone-card-box{
  width: 92%;
  /*height: 500px;*/
  /*background: #42b983;*/
  /*display: flex;*/
  box-sizing: border-box;
  overflow: hidden;
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  margin: auto;
}
.iphone-box-top .iphone-top-left{
  width: 90%;
  height: 50%;
  /*background: #99a9bf;*/
  text-align: left;
  /*padding: 6rem;*/
  box-sizing: border-box;
}
.iphone-top-left .iphone-left-title{
  color: black;
  font-weight: 600;
  font-size: 1.4rem;
  /*line-height: 1.8rem;*/
  margin-bottom: .4rem;
}
.iphone-top-left .iphone-left-log{
  width: 10rem;
  background: white;
  color: #333333;
  font-weight: 600;
  line-height: 1.5;
  margin: 0;
  box-shadow: 0 0 4px #333333;
  border-radius: 2px;
  padding: 6px;
  box-sizing: border-box;
  font-size: .8rem;
}
.iphone-top-left .iphone-left-p{
  line-height: 1.5;
  box-sizing: border-box;
  margin: .6rem 0;
  /*padding-right: 7rem;*/
}
.iphone-top-left .iphone-left-but{
  width: 6rem;
  line-height: 42px;
  background: #24262b;
  text-align: center;
  cursor: pointer;
  margin: 0;
  border-radius: 2px;
  font-size: .8rem;
}
.iphone-box-top .iphone-top-right{
  width: 90%;
  height: 50%;
  background: url("../../assets/img/card/card.png") no-repeat;
  background-size: contain;
  background-position: center;
}
.iphone-left-but:hover{
  background: #333333;
}
.iphone-active{
  margin-bottom: 0!important;
}
.iphone-box-center ul{
  color: #fba600;
  font-size: 1rem;
  /*margin-bottom: 2rem;*/
}
.iphone-box-center .iphone-top-right{
  background: url("../../assets/img/card/card1.png") no-repeat;
  background-size: contain;
  background-position: center;
}
/*字*/
.iphone-xy-size{
  font-size: 1rem;
  color: black;
  font-weight: 600;
  line-height: 1.5;
}

/*列表*/
.iphone-box-bottom{
  width: 100%;
  height: 180vh;
  /*background: palegoldenrod;*/
  margin: 20px auto;
  margin-bottom: 40px;
  overflow: hidden;
  box-sizing: border-box;
}
.iphone-box-bottom h1{

}
.iphone-card-start{
  width: 100%;
  height: 80%;
  /*background: pink;*/
  position: relative;
  box-sizing: border-box;
  overflow: hidden;
}
.iphone-card-line{
  width: 6px;
  height: 100%;
  background: #24344b;
  position: absolute;
  /*top: 0;*/
  /*bottom: 0;*/
  /*right: 0;*/
  left: .8rem;
  margin: auto;
  border: 1px solid #141c2c;
  box-sizing: border-box;
  border-radius: 10px;
  overflow: hidden;
  z-index: 9;
}
.iphone-card-jd{
  background: #eadebc;
  transition: height .6s;
}
.iphone-card-bt{
  cursor: pointer;
}
/*开练*/
.iphone-new{
  width: calc(100% - 1rem);
}
.iphone-card-list{
  width: 100%;
  height: 24vh;
  /*background: #42b983;*/
  display: flex;
  flex-direction: row-reverse;
  position: absolute;
  top: 1%;
}
.iphone-card-list-left{
  /*width: 50%;*/
  width: 100%;
  height: 100%;
  background: #24344b;
  display: flex;
  flex-direction: row-reverse;
  /*opacity: 0;*/
}
.iphone-card-list-left-left{
  display: flex;
  justify-content: space-between;
  box-sizing: border-box;
  padding: .4rem;
  border-radius: 6px;
  border: 1px solid #f2cf6a;
  overflow: hidden;
}
.iphone-card-list-left img{
  width: 30%;
  height: 100%;
}
.iphone-card-list-left-right{
  width: 8%;
  height: 100%;
  /*background: #99a9bf;*/
  position: relative;
}
.iphone-card-list-center{
  width: 1rem;
  height: 100%;
  background: #24344b;
  position: relative;
}
.iphone-card-list-x{
  width: 100%;
  height: 2px;
  background: #f2cf6a;
  position: absolute;
  top: 0;
  bottom: 0;
  margin: auto;
}
.iphone-card-list-d{
  width: 20px;
  height: 20px;
  background: #f2cf6a;
  border-radius: 50%;
  box-shadow: 0 0 8px #f2cf6a;
  position: absolute;
  top: 0;
  bottom: 0;
  /*left: .1rem;*/
  right: -.6rem;
  margin: auto;
  cursor: pointer;
  z-index: 9;
}
.iphone-card-list-d-to{
  /*left: -15px;*/
}
.iphone-card-list-right{
  width: 46%;
  height: 100%;
  background: #24344b;
  text-align: left;
  position: relative;
}
.iphone-card-list-right-p{
  height: 42px;
  position: absolute;
  top: 0;
  bottom: 0;
  margin: auto;
  font-size: 1.8rem;
  letter-spacing:8px;
  transition: opacity .3s;
}
/*右面list*/
.iphone-card-list-active{
  top: 21%;
  flex-direction: row-reverse;
}
.iphone-card-list-left-active{
  flex-direction: row-reverse;
}
.iphone-card-list-d-active{
  right: -15px;
  /*left: 0!important;*/
}
.iphone-card-list-right-p-active{
  right: 0;
}
.iphone-card-list-active-one{
  top: 41%;
}
.iphone-card-list-active-two{
  top: 61%;
}
.iphone-card-list-active-top{
  top: 81%;
}
/*左面图*/
.iphone-card-list-left-right-active{
  width: 56%;
}
.iphone-card-list-left-left-active img{
  margin: 0;
  width: 48%;
}

/*最下面*/
.iphone-card-bottom{
  width: 100%;
  height: 20%;
  /*background: #42b983;*/
  position: relative;
  /*box-sizing: border-box;*/
  /*overflow: hidden;*/
}
.iphone-card-bottom .iphone-dian{
  width: 20px;
  height: 20px;
  background: #f2cf6a;
  border-radius: 50%;
  box-shadow: 0 0 8px #f2cf6a;
  position: absolute;
  top: -.6rem;
  /*bottom: 0;*/
  left: .35rem;
  /*right: -.6rem;*/
  margin: auto;
  cursor: pointer;
  z-index: 9;
}
.iphone-card-bottom .iphone-card-bt-img{
  /*width: 30%;*/
  height: 100%;
  /*background: #99a9bf;*/
  /*margin-top: 15px;*/
  padding-top: 1.6rem;
  box-sizing: border-box;
  opacity: 0;
  transition: opacity .3s;
  /*overflow: hidden;*/
}
.iphone-card-bottom .iphone-card-bt-img img{
  width: 10rem;
  position: absolute;
  left: 0;
}

</style>
