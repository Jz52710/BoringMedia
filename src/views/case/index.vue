<template>
  <div>
    <el-container>
      <!--      <el-header>-->
      <!--        <Header @func="getMsgFormSon" @fun="getMsg1FormSon"></Header>-->
      <!--      </el-header>-->
      <el-main>
        <!--web-->
        <div class="case-box hidden-sm-and-down">
          <div class="case-title">
            <p>Mansory projects</p>
            <h3>Corn pile</h3>
            <div class="case-g">
              <div class="case-gs"></div>
            </div>
            <div class="case-gb">
              <div class="case-gbs"></div>
            </div>
          </div>

          <div class="case-nav">
            <el-radio-group v-model="isCollapse" style="margin-bottom: 20px;">
              <el-radio-button :label="1">All</el-radio-button>
              <el-radio-button :label="2">Latest</el-radio-button>
              <el-radio-button :label="3">Selling</el-radio-button>
              <el-radio-button :label="4">Services</el-radio-button>
              <el-radio-button :label="5">3d design</el-radio-button>
            </el-radio-group>
          </div>

          <div class="case-con">

            <!--            <div class="case-list" v-for="(list,key) in list" :key="key" :class="key==0||key==3?'case-list case-active':'case-list'">-->
            <!--              <div class="case-top">-->
            <!--                <img :src="list.image" alt="">-->
            <!--              </div>-->
            <!--              <div class="case-bottom">-->
            <!--                <p class="case-bt-title">{{list.title}}</p>-->
            <!--                <p class="case-bt-con">{{list.con}}</p>-->
            <!--              </div>-->
            <!--            </div>-->

            <ul class="case-ui">
              <div class="case-list case-active">
                <div class="case-top">
                  <div class="case-m"></div>
                  <div class="case-but" @click="nextdetails(list[0].id)">View More</div>
                  <img :src="list[0].image" alt="">
                </div>
                <div class="case-bottom">
                  <p class="case-bt-title">{{list[0].title}}</p>
                  <p class="case-bt-con">{{list[0].con}}</p>
                </div>
              </div>
              <div class="case-list">
                <div class="case-top">
                  <div class="case-m"></div>
                  <div class="case-but" @click="nextdetails(list[1].id)">View More</div>
                  <img :src="list[1].image" alt="">
                </div>
                <div class="case-bottom">
                  <p class="case-bt-title">{{list[1].title}}</p>
                  <p class="case-bt-con">{{list[1].con}}</p>
                </div>
              </div>
            </ul>

            <ul class="case-ui">
              <div class="case-list">
                <div class="case-top">
                  <div class="case-m"></div>
                  <div class="case-but" @click="nextdetails(list[2].id)">View More</div>
                  <img :src="list[2].image" alt="">
                </div>
                <div class="case-bottom">
                  <p class="case-bt-title">{{list[2].title}}</p>
                  <p class="case-bt-con">{{list[2].con}}</p>
                </div>
              </div>
              <div class="case-list case-active">
                <div class="case-top">
                  <div class="case-m"></div>
                  <div class="case-but" @click="nextdetails(list[3].id)">View More</div>
                  <img :src="list[3].image" alt="">
                </div>
                <div class="case-bottom">
                  <p class="case-bt-title">{{list[3].title}}</p>
                  <p class="case-bt-con">{{list[3].con}}</p>
                </div>
              </div>
            </ul>

            <ul class="case-ui">
              <div class="case-list">
                <div class="case-top">
                  <div class="case-m"></div>
                  <div class="case-but" @click="nextdetails(list[4].id)">View More</div>
                  <img :src="list[4].image" alt="">
                </div>
                <div class="case-bottom">
                  <p class="case-bt-title">{{list[4].title}}</p>
                  <p class="case-bt-con">{{list[4].con}}</p>
                </div>
              </div>
              <div class="case-list">
                <div class="case-top">
                  <div class="case-m"></div>
                  <div class="case-but" @click="nextdetails(list[5].id)">View More</div>
                  <img :src="list[5].image" alt="">
                </div>
                <div class="case-bottom">
                  <p class="case-bt-title">{{list[5].title}}</p>
                  <p class="case-bt-con">{{list[5].con}}</p>
                </div>
              </div>
            </ul>
            <div class="case-button" @click="next">
              More Projects
            </div>
          </div>

        </div>

        <!--iphone-->
        <div class="iphone-case-box hidden-md-and-up">
          <div class="iphone-case-title">
            <p>Mansory projects</p>
            <h3>Corn pile</h3>
            <div class="iphone-case-g">
              <div class="iphone-case-gs"></div>
            </div>
            <div class="iphone-case-gb">
              <div class="iphone-case-gbs"></div>
            </div>
          </div>

          <div class="iphone-case-nav">
            <el-radio-group v-model="isCollapse">
              <el-radio-button :label="1">All</el-radio-button>
              <el-radio-button :label="2">Latest</el-radio-button>
              <el-radio-button :label="3">Selling</el-radio-button>
              <el-radio-button :label="4">Services</el-radio-button>
              <el-radio-button :label="5">3d design</el-radio-button>
            </el-radio-group>
          </div>

          <div class="iphone-case-con">

            <div class="iphone-case-list" v-for="(list,key) in list" :key="key">
              <div class="case-top">
                <div class="case-m"></div>
                <div class="case-but iphone-case-but" @click="nextdetails(key)">View More</div>
                <img :src="list.image" alt="">
              </div>
              <div class="case-bottom">
                <p class="case-bt-title">{{list.title}}</p>
                <p class="case-bt-con">{{list.con}}</p>
              </div>
            </div>

            <div class="iphone-case-button" @click="next">
              More Projects
            </div>
          </div>

        </div>

        <!--底边栏-->
        <!--        <el-footer>-->
        <!--          &lt;!&ndash;横杠&ndash;&gt;-->
        <!--          <div class="gang-box"></div>-->
        <!--          <p class="hidden-sm-and-down p-size">媒趣科技智能有限公司</p>-->
        <!--          <p class="hidden-md-and-up p-show-size">媒趣科技智能有限公司</p>-->
        <!--        </el-footer>-->
      </el-main>

      <!--蒙版-->
      <!--      <div class="box-show" :style="{ display: this.boxShadow}"></div>-->
      <!--      &lt;!&ndash;线&ndash;&gt;-->
      <!--      <div class="line-box"></div>-->
      <!--      <div class="line-right-box"></div>-->
    </el-container>
  </div>
</template>

<script>
// 最新动态
// import HelloWorld from './components/HelloWorld.vue'
// import Header from '@/components/header/Header.vue'

export default {
  name: 'Index',
  components: {
    // HelloWorld
    // Header
  },
  data() {
    return {
      boxShadow:'none',
      isCollapse: 1,
      list:[
        {
          id:0,
          image:require('../../assets/img/corn/shop.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
        {
          id:1,
          image:require('../../assets/img/corn/sf3.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
        {
          id:2,
          image:require('../../assets/img/corn/sf.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
        {
          id:3,
          image:require('../../assets/img/corn/sf4.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
        {
          id:4,
          image:require('../../assets/img/corn/sf2.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
        {
          id:5,
          image:require('../../assets/img/corn/sf5.png'),
          title:'Products of our project',
          con:'Our Projects',
        },
      ]
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
      window.scroll(0, 0);
    },
    nextdetails(data){
      // alert(data)
      this.$emit('keyword',data)
      this.$router.push({name:'casedetails'})
      window.scroll(0, 0);
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
  /*height: calc(100vh - 80px) !important;*/
  position: relative;
  padding:0!important;
  /*margin-top: 80px;*/
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
.case-box{
  width: 100%;
  /*height: 100%;*/
  /*background: pink;*/
  /*position: relative;*/
}
.case-title{
  width: 100%;
  height: 100px;
  /*background: #42b983;*/
  overflow: hidden;
  box-sizing: border-box;
  /*position: absolute;*/
  /*top: 8%;*/
}
.case-title p{
  font-size: 1rem;
  color: #5b6bdb;
  margin-top: 6px;
}
.case-title h3{
  font-size: 1.6rem;
  font-weight: 400;
  margin: 4px 0;
}
.case-g{
  width: 4%;
  height: 3px;
  background: #d1d5fc;
}
.case-gs{
  width: 50%;
  height: 100%;
  background: #6979ff;
  margin: 0;
}
.case-gb{
  width: 2%;
  height: 3px;
  background: #d1d5fc;
  margin-top: 2px;
}
.case-gbs{
  width: 50%;
  height: 100%;
  background: #6979ff;
  margin: 0;
}

/*按钮*/
.case-nav{
  width: 100%;
  height: 90px;
  /*background: #a0813d;*/
  box-sizing: border-box;
  overflow: hidden;
  /*padding-top: 1rem;*/
}
.el-radio-group{
  margin-bottom: 0!important;

}
/deep/.el-radio-button:first-child .el-radio-button__inner{
  border-left: 1px solid #2f415b!important;
}
/deep/.el-radio-button__inner{
  background: #283951;
  border: 1px solid #2f415b;
  color: white;
  padding: 16px 40px;
}
/deep/.el-radio-button__orig-radio:checked+.el-radio-button__inner{
  background: #6979ff;
  border-color: #6979ff;
  box-shadow: -1px 0 0 0 #6979ff;
}
/*内容*/
.case-con{
  width: 60%;
  height: 900px;
  /*background: #42b983;*/
  display: flex;
  justify-content: space-between;
  /*flex-flow:column wrap;*/
  /*object-fit: contain;*/
  flex-wrap: wrap;
  overflow: hidden;
}

.case-list{
  width: 100%;
  height: 314px;
  /*background: pink;*/
  cursor: pointer;
  margin: 0;
}
.case-list:hover .case-m{
  opacity: .5;
}
.case-list:hover .case-but{
  opacity: 1;
}
.case-but:hover{
  background: #24355b!important;
}
.case-top{
  width: 100%;
  height: 194px;
  /*background: #99a9bf;*/
  position: relative;
}
.case-top .case-m{
  background: #efefef;
  width: 100%;
  height: 100%;
  position: absolute;
  opacity: 0;
  transition: opacity .3s;
}
.case-top .case-but{
  width: 180px;
  height: 54px;
  background: #314767;
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;
  border-radius: 3px;
  line-height: 54px;
  opacity: 0;
  transition: opacity .3s;
}
.case-top img{
  width: 100%;
  height: 100%;
}

.case-bottom{
  width: 100%;
  height: 120px;
  background: #f4f4f4;
  border: 1px solid #f4f4f4;
  border-top: 1px solid #24344b;
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
}
.case-bottom .case-bt-title{
  color: #24344b;
  position: absolute;
  top: 30%;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;
  /*background: #5b6bdb;*/
}
.case-bottom .case-bt-con{
  color: #8d8e90;
  position: absolute;
  top: 50%;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;
  /*background: #99a9bf;*/
}
.case-active{
  height: 476px;
}
.case-active .case-top{
  width: 100%;
  height: 356px;
}
.case-active .case-bottom{
  background: #f4f4f4;
  border: 1px solid #f4f4f4;
  border-top: 1px solid #24344b;
}
.case-active .case-bt-title{
  color: #24344b;
}

.case-ui{
  width: 32%;
  height: 812px;
  /*background: pink;*/
  cursor: pointer;
  margin: 0;
  overflow: hidden;
  /*display: flex;*/
  /*flex-wrap: wrap;*/
}
.case-list:first-child{
  margin-bottom: 22px;
}
/*按钮*/
.case-button{
  width: 120px;
  height: 2rem;
  /*background: #5b6bdb;*/
  border-radius: 30px;
  line-height: 2rem;
  overflow: hidden;
  cursor: pointer;
  color: #5f616a;
  border: 1px solid #5f616a;
  font-size: 1rem;
}


/*iphone*/
.iphone-case-box{
  width: 100%;
  /*background: palevioletred;*/
}
.iphone-case-title{
  width: 100%;
  height: 5rem;
  /*background: #42b983;*/
  overflow: hidden;
  box-sizing: border-box;
  /*position: absolute;*/
  /*top: 8%;*/
}
.iphone-case-title p{
  font-size: 1rem;
  color: #5b6bdb;
  margin-top: .4rem;
}
.iphone-case-title h3{
  font-size: 1.4rem;
  font-weight: 400;
  margin: 4px 0;
}
.iphone-case-g{
  width: 8%;
  height: 3px;
  background: #d1d5fc;
}
.iphone-case-gs{
  width: 50%;
  height: 100%;
  background: #6979ff;
  margin: 0;
}
.iphone-case-gb{
  width: 4%;
  height: 3px;
  background: #d1d5fc;
  margin-top: 2px;
}
.iphone-case-gbs{
  width: 50%;
  height: 100%;
  background: #6979ff;
  margin: 0;
}

/*按钮*/
.iphone-case-nav{
  width: 100%;
  height: 3.6rem;
  /*background: #a0813d;*/
  box-sizing: border-box;
  overflow: hidden;
  /*padding-top: 1rem;*/
}
.iphone-case-nav .el-radio-group{
  margin-bottom: 0!important;
}
.iphone-case-nav /deep/.el-radio-button:first-child .el-radio-button__inner{
  border-left: 1px solid #2f415b!important;
}
.iphone-case-nav /deep/.el-radio-button__inner{
  background: #283951;
  border: 1px solid #2f415b;
  color: white;
  /*padding: 0!important;*/
  padding: .8rem;
  font-size: .2rem;
}
.iphone-case-nav /deep/.el-radio-button__orig-radio:checked+.el-radio-button__inner{
  background: #6979ff;
  border-color: #6979ff;
  box-shadow: -1px 0 0 0 #6979ff;
}

/*列表*/
.iphone-case-con{
  width: 80%;
  /*height: 900px;*/
  /*background: #42b983;*/
  /*display: flex;*/
  /*justify-content: space-between;*/
  /*flex-flow:column wrap;*/
  /*object-fit: contain;*/
  /*flex-wrap: wrap;*/
  overflow: hidden;
}
.iphone-case-list{
  margin-bottom: 1rem;
}

.iphone-case-list:hover .case-m{
  opacity: .5;
}
.iphone-case-list:hover .case-but{
  opacity: 1;
}
.case-but:hover{
  background: #24355b!important;
}
.iphone-case-list .iphone-case-but{
  width: 138px;
  height: 48px;
  line-height: 48px;
}

/*下面*/
.iphone-case-button{
    width: 120px;
  height: 2rem;
  /*background: #5b6bdb;*/
  border-radius: 30px;
  line-height: 2rem;
  overflow: hidden;
  cursor: pointer;
  color: #5f616a;
  border: 1px solid #5f616a;
  font-size: .8rem;
  margin-bottom: 1rem;
}

</style>