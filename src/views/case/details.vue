<template>
  <div>
    <el-container>
      <!--      <el-header>-->
      <!--        <Header @func="getMsgFormSon" @fun="getMsg1FormSon"></Header>-->
      <!--      </el-header>-->
      <el-main>
        <!--web-->
        <div class="details-box hidden-sm-and-down">
          <div class="new-top" @click="back">{{title}}</div>
          <div class="new-bot">
            <h1>{{ list[keyword].title1 }}</h1>
            <div class="new-video">
              <video autoplay :src="list[keyword].video" controls preload="auto" style="width: 100%;height: 100%"></video>
            </div>
            <h2>{{list[keyword].title2}}</h2>
            <p class="new-text" v-html="list[keyword].text"></p>
          </div>
        </div>


        <!--手机版-->
        <div class="iphone-details-box hidden-md-and-up">
          <div class="iphone-new-top" @click="back">{{title}}</div>
          <div class="iphone-new-bot">
            <h1>{{ list[keyword].title1 }}</h1>
            <div class="iphone-new-video">
              <video autoplay :src="list[keyword].video" controls preload="auto" style="width: 100%;height: 100%"></video>
            </div>
            <h2>{{list[keyword].title2}}</h2>
            <p class="iphone-new-text" v-html="list[keyword].text"></p>
          </div>
        </div>

        <!--底边栏-->
        <el-footer>
          <!--横杠-->
          <div class="gang-box"></div>
          <p class="hidden-sm-and-down p-size">媒趣科技智能有限公司</p>
          <p class="hidden-md-and-up p-show-size">媒趣科技智能有限公司</p>
        </el-footer>
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
  name: 'Details',
  props:['keyword'],
  components: {
    // HelloWorld
    // Header
  },
  data() {
    return {
      boxShadow:'none',
      title:'<< BACK',
      list:[{
        title1:'智慧农场',
        title2:'摘要',
        video:require('../../assets/img/video/v1.mp4'),
        text:'上海港汇恒隆广场于11月19日举行周年庆典-GATEWAY TO INSPIRATION焕新派对，Wonderlabs有幸参与此次盛大的庆典，并制作了INSPIRATION LAB，光波鼓，镜像Battle，微笑大挑战，潮流灵体验等5项互动装置。<br/>' +
            '&nbsp;<br/>' +
            '「Inspiration Lab位于港汇广场内街，当进入Inspiration Lab时，即刻会被炫彩夺目的光影吸引目光。消费者的移动轨迹，可以创造出各种渐变幻彩的粒子效果，相机记录下这一幕即可分享朋友圈」<br/>' +
            '&nbsp;<br/>' +
            '「光波鼓位于广场内街两侧，为了增强灯带的视觉效果，灯带被架设出山峦般高低起伏的效果。体验者可以同时击打鼓面，触发光波沿着线路向远处传播，从而产生带有动画的视觉效果，有趣的是光波的速度变化取决于体验者击鼓的速度与强度」<br/>' +
            '&nbsp;<br/>' +
            '「这两项互动装置，错落分布在商场南座的二楼和三楼，镜像battle采用Kinect体感动作捕捉技术，体验者根据屏幕中提示动作，做出相同动作，动作越标准得分越高；微笑大挑战，我们采用了面部分析技术,微笑过程中实时检测体验者面部，分析后给出微笑分值」<br/>' +
            ' &nbsp;<br/>' +
            '「潮流灵体验位于商场北座1楼，我们在两台显示屏中设计了巨大的礼品贩卖机效果，利用leap motion体感控制器，可以捕捉到手部手指的关节点，体验者通过指定动作，控制屏幕中虚拟手臂，实现抽取虚拟奖品<br/>'+' &nbsp;<br/>'+'客户<br/>' +' &nbsp;<br/>'+
            '远景集团<br/>'+'&nbsp;<br/>'
      }, {
        title1:'智慧农场2',
        title2:'摘要',
        video:require('../../assets/img/video/v2.mp4'),
        text:'上海港汇恒隆广场于11月19日举行周年庆典-GATEWAY TO INSPIRATION焕新派对，Wonderlabs有幸参与此次盛大的庆典，并制作了INSPIRATION LAB，光波鼓，镜像Battle，微笑大挑战，潮流灵体验等5项互动装置。<br/>' +
            '&nbsp;<br/>' +
            '「Inspiration Lab位于港汇广场内街，当进入Inspiration Lab时，即刻会被炫彩夺目的光影吸引目光。消费者的移动轨迹，可以创造出各种渐变幻彩的粒子效果，相机记录下这一幕即可分享朋友圈」<br/>' +
            '&nbsp;<br/>' +
            '「光波鼓位于广场内街两侧，为了增强灯带的视觉效果，灯带被架设出山峦般高低起伏的效果。体验者可以同时击打鼓面，触发光波沿着线路向远处传播，从而产生带有动画的视觉效果，有趣的是光波的速度变化取决于体验者击鼓的速度与强度」<br/>' +
            '&nbsp;<br/>' +
            '「这两项互动装置，错落分布在商场南座的二楼和三楼，镜像battle采用Kinect体感动作捕捉技术，体验者根据屏幕中提示动作，做出相同动作，动作越标准得分越高；微笑大挑战，我们采用了面部分析技术,微笑过程中实时检测体验者面部，分析后给出微笑分值」<br/>' +
            ' &nbsp;<br/>' +
            '「潮流灵体验位于商场北座1楼，我们在两台显示屏中设计了巨大的礼品贩卖机效果，利用leap motion体感控制器，可以捕捉到手部手指的关节点，体验者通过指定动作，控制屏幕中虚拟手臂，实现抽取虚拟奖品<br/>'+' &nbsp;<br/>'+'客户<br/>' +' &nbsp;<br/>'+
            '远景集团<br/>'+'&nbsp;<br/>'
      },{
        title1:'智慧农场3',
        title2:'摘要',
        video:require('../../assets/img/video/v3.mp4'),
        text:'上海港汇恒隆广场于11月19日举行周年庆典-GATEWAY TO INSPIRATION焕新派对，Wonderlabs有幸参与此次盛大的庆典，并制作了INSPIRATION LAB，光波鼓，镜像Battle，微笑大挑战，潮流灵体验等5项互动装置。<br/>' +
            '&nbsp;<br/>' +
            '「Inspiration Lab位于港汇广场内街，当进入Inspiration Lab时，即刻会被炫彩夺目的光影吸引目光。消费者的移动轨迹，可以创造出各种渐变幻彩的粒子效果，相机记录下这一幕即可分享朋友圈」<br/>' +
            '&nbsp;<br/>' +
            '「光波鼓位于广场内街两侧，为了增强灯带的视觉效果，灯带被架设出山峦般高低起伏的效果。体验者可以同时击打鼓面，触发光波沿着线路向远处传播，从而产生带有动画的视觉效果，有趣的是光波的速度变化取决于体验者击鼓的速度与强度」<br/>' +
            '&nbsp;<br/>' +
            '「这两项互动装置，错落分布在商场南座的二楼和三楼，镜像battle采用Kinect体感动作捕捉技术，体验者根据屏幕中提示动作，做出相同动作，动作越标准得分越高；微笑大挑战，我们采用了面部分析技术,微笑过程中实时检测体验者面部，分析后给出微笑分值」<br/>' +
            ' &nbsp;<br/>' +
            '「潮流灵体验位于商场北座1楼，我们在两台显示屏中设计了巨大的礼品贩卖机效果，利用leap motion体感控制器，可以捕捉到手部手指的关节点，体验者通过指定动作，控制屏幕中虚拟手臂，实现抽取虚拟奖品<br/>'+' &nbsp;<br/>'+'客户<br/>' +' &nbsp;<br/>'+
            '远景集团<br/>'+'&nbsp;<br/>'
      },{
        title1:'智慧农场4',
        title2:'摘要',
        video:require('../../assets/img/video/v4.mp4'),
        text:'上海港汇恒隆广场于11月19日举行周年庆典-GATEWAY TO INSPIRATION焕新派对，Wonderlabs有幸参与此次盛大的庆典，并制作了INSPIRATION LAB，光波鼓，镜像Battle，微笑大挑战，潮流灵体验等5项互动装置。<br/>' +
            '&nbsp;<br/>' +
            '「Inspiration Lab位于港汇广场内街，当进入Inspiration Lab时，即刻会被炫彩夺目的光影吸引目光。消费者的移动轨迹，可以创造出各种渐变幻彩的粒子效果，相机记录下这一幕即可分享朋友圈」<br/>' +
            '&nbsp;<br/>' +
            '「光波鼓位于广场内街两侧，为了增强灯带的视觉效果，灯带被架设出山峦般高低起伏的效果。体验者可以同时击打鼓面，触发光波沿着线路向远处传播，从而产生带有动画的视觉效果，有趣的是光波的速度变化取决于体验者击鼓的速度与强度」<br/>' +
            '&nbsp;<br/>' +
            '「这两项互动装置，错落分布在商场南座的二楼和三楼，镜像battle采用Kinect体感动作捕捉技术，体验者根据屏幕中提示动作，做出相同动作，动作越标准得分越高；微笑大挑战，我们采用了面部分析技术,微笑过程中实时检测体验者面部，分析后给出微笑分值」<br/>' +
            ' &nbsp;<br/>' +
            '「潮流灵体验位于商场北座1楼，我们在两台显示屏中设计了巨大的礼品贩卖机效果，利用leap motion体感控制器，可以捕捉到手部手指的关节点，体验者通过指定动作，控制屏幕中虚拟手臂，实现抽取虚拟奖品<br/>'+' &nbsp;<br/>'+'客户<br/>' +' &nbsp;<br/>'+
            '远景集团<br/>'+'&nbsp;<br/>'
      },{
        title1:'智慧农场5',
        title2:'摘要',
        video:require('../../assets/img/video/v5.mp4'),
        text:'上海港汇恒隆广场于11月19日举行周年庆典-GATEWAY TO INSPIRATION焕新派对，Wonderlabs有幸参与此次盛大的庆典，并制作了INSPIRATION LAB，光波鼓，镜像Battle，微笑大挑战，潮流灵体验等5项互动装置。<br/>' +
            '&nbsp;<br/>' +
            '「Inspiration Lab位于港汇广场内街，当进入Inspiration Lab时，即刻会被炫彩夺目的光影吸引目光。消费者的移动轨迹，可以创造出各种渐变幻彩的粒子效果，相机记录下这一幕即可分享朋友圈」<br/>' +
            '&nbsp;<br/>' +
            '「光波鼓位于广场内街两侧，为了增强灯带的视觉效果，灯带被架设出山峦般高低起伏的效果。体验者可以同时击打鼓面，触发光波沿着线路向远处传播，从而产生带有动画的视觉效果，有趣的是光波的速度变化取决于体验者击鼓的速度与强度」<br/>' +
            '&nbsp;<br/>' +
            '「这两项互动装置，错落分布在商场南座的二楼和三楼，镜像battle采用Kinect体感动作捕捉技术，体验者根据屏幕中提示动作，做出相同动作，动作越标准得分越高；微笑大挑战，我们采用了面部分析技术,微笑过程中实时检测体验者面部，分析后给出微笑分值」<br/>' +
            ' &nbsp;<br/>' +
            '「潮流灵体验位于商场北座1楼，我们在两台显示屏中设计了巨大的礼品贩卖机效果，利用leap motion体感控制器，可以捕捉到手部手指的关节点，体验者通过指定动作，控制屏幕中虚拟手臂，实现抽取虚拟奖品<br/>'+' &nbsp;<br/>'+'客户<br/>' +' &nbsp;<br/>'+
            '远景集团<br/>'+'&nbsp;<br/>'
      },{
        title1:'智慧农场6',
        title2:'摘要',
        video:require('../../assets/img/video/v5.mp4'),
        text:'上海港汇恒隆广场于11月19日举行周年庆典-GATEWAY TO INSPIRATION焕新派对，Wonderlabs有幸参与此次盛大的庆典，并制作了INSPIRATION LAB，光波鼓，镜像Battle，微笑大挑战，潮流灵体验等5项互动装置。<br/>' +
            '&nbsp;<br/>' +
            '「Inspiration Lab位于港汇广场内街，当进入Inspiration Lab时，即刻会被炫彩夺目的光影吸引目光。消费者的移动轨迹，可以创造出各种渐变幻彩的粒子效果，相机记录下这一幕即可分享朋友圈」<br/>' +
            '&nbsp;<br/>' +
            '「光波鼓位于广场内街两侧，为了增强灯带的视觉效果，灯带被架设出山峦般高低起伏的效果。体验者可以同时击打鼓面，触发光波沿着线路向远处传播，从而产生带有动画的视觉效果，有趣的是光波的速度变化取决于体验者击鼓的速度与强度」<br/>' +
            '&nbsp;<br/>' +
            '「这两项互动装置，错落分布在商场南座的二楼和三楼，镜像battle采用Kinect体感动作捕捉技术，体验者根据屏幕中提示动作，做出相同动作，动作越标准得分越高；微笑大挑战，我们采用了面部分析技术,微笑过程中实时检测体验者面部，分析后给出微笑分值」<br/>' +
            ' &nbsp;<br/>' +
            '「潮流灵体验位于商场北座1楼，我们在两台显示屏中设计了巨大的礼品贩卖机效果，利用leap motion体感控制器，可以捕捉到手部手指的关节点，体验者通过指定动作，控制屏幕中虚拟手臂，实现抽取虚拟奖品<br/>'+' &nbsp;<br/>'+'客户<br/>' +' &nbsp;<br/>'+
            '远景集团<br/>'+'&nbsp;<br/>'
      },{
        title1:'智慧农场7',
        title2:'摘要',
        video:require('../../assets/img/video/v6.mp4'),
        text:'上海港汇恒隆广场于11月19日举行周年庆典-GATEWAY TO INSPIRATION焕新派对，Wonderlabs有幸参与此次盛大的庆典，并制作了INSPIRATION LAB，光波鼓，镜像Battle，微笑大挑战，潮流灵体验等5项互动装置。<br/>' +
            '&nbsp;<br/>' +
            '「Inspiration Lab位于港汇广场内街，当进入Inspiration Lab时，即刻会被炫彩夺目的光影吸引目光。消费者的移动轨迹，可以创造出各种渐变幻彩的粒子效果，相机记录下这一幕即可分享朋友圈」<br/>' +
            '&nbsp;<br/>' +
            '「光波鼓位于广场内街两侧，为了增强灯带的视觉效果，灯带被架设出山峦般高低起伏的效果。体验者可以同时击打鼓面，触发光波沿着线路向远处传播，从而产生带有动画的视觉效果，有趣的是光波的速度变化取决于体验者击鼓的速度与强度」<br/>' +
            '&nbsp;<br/>' +
            '「这两项互动装置，错落分布在商场南座的二楼和三楼，镜像battle采用Kinect体感动作捕捉技术，体验者根据屏幕中提示动作，做出相同动作，动作越标准得分越高；微笑大挑战，我们采用了面部分析技术,微笑过程中实时检测体验者面部，分析后给出微笑分值」<br/>' +
            ' &nbsp;<br/>' +
            '「潮流灵体验位于商场北座1楼，我们在两台显示屏中设计了巨大的礼品贩卖机效果，利用leap motion体感控制器，可以捕捉到手部手指的关节点，体验者通过指定动作，控制屏幕中虚拟手臂，实现抽取虚拟奖品<br/>'+' &nbsp;<br/>'+'客户<br/>' +' &nbsp;<br/>'+
            '远景集团<br/>'+'&nbsp;<br/>'
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
    back(){
      this.$router.push({name:'case'})
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
  /*background-color: pink;*/
  color: white;
  text-align: center;
  line-height: 60px;
  width: 100%;
  height: 100%;
  padding: 0;
  position: relative;
}
.el-main {
  background-color: #24344b;
  color: white;
  text-align: center;
  width: 100%;
  /*height: 100vh;*/
  /*height: calc(100vh - 80px) !important;*/
  position: absolute;
  padding:0!important;
  /*margin-top: 80px;*/
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
/*footer*/
.p-size{
  color: white;
}
.p-show-size{
  font-size: 0.8rem;
  line-height: 5.6;
  color: white;
}
/*横杠*/
.gang-box{
  width: 50%;
  height: 2px;
  position: absolute;
  left: 0;
  right: 0;
  top: 18%;
  bottom: 0;
  margin: 0 auto;
  z-index: 99;
  background: white;
}
/*线*/
.line-box{
  position: fixed;
  width: 2px;
  height: 100%;
  background: white;
  z-index: 99;
  left: 10%;
  opacity: .2;
}
.line-right-box{
  position: fixed;
  width: 2px;
  height: 100%;
  background: white;
  z-index: 99;
  /*right: 18%;*/
  right: 10%;
  opacity: .2;
}

/*web*/
.details-box{
  width: 56%;
  height: 100%;
  /*background: #5b6bdb;*/
}
.new-top{
  text-align: right;
  /*background: #a0813d;*/
  cursor: pointer;
  padding-right: 8px;
}
.new-bot{
  width: 100%;
  height: 100%;
  /*background: pink;*/
}
.new-bot h1{
  font-size: 1.5rem;
  color: white;
  padding: 1rem 0;
}
.new-video{
  width: 100%;
  height: 610px;
  padding-bottom: 45px;
  /*background: #5b6bdb;*/
}
.new-bot h2{
  font-size: 1rem;
  text-align: left;
  padding-left: 8px;
  font-weight: 500;
  padding-bottom: 1rem;
}
.new-text{
  font-size: 1rem;
  line-height: 1.5;
  text-align: left;
  padding: 0 8px;
}

/*手机版*/
/*顶部*/
.iphone-details-box{
  width: 76%;
  height: 100%;
  /*background: #5b6bdb;*/
}
.iphone-new-top{
  text-align: right;
  /*background: #a0813d;*/
  cursor: pointer;
  padding-right: 8px;
}
.iphone-new-bot{
  width: 100%;
  height: 100%;
  /*background: pink;*/
}
.iphone-new-bot h1{
  font-size: 1.2rem;
  color: white;
  padding: .6rem 0;
}
.iphone-new-video{
  width: 100%;
  height: 11rem;
  padding-bottom: 20px;
  /*background: #5b6bdb;*/
}
.iphone-new-bot h2{
  font-size: 1rem;
  text-align: left;
  padding-left: 8px;
  font-weight: 500;
  padding-bottom: 1rem;
}
.iphone-new-text{
  font-size: .8rem;
  line-height: 1.5;
  text-align: left;
  padding: 0 8px;
}

</style>
