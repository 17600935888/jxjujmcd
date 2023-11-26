<template>
  <div id="JobChance">
    <div class="banner container-fuild text-center">工作机会</div>
    <div class="container">
      <div class="JobChance-container wow pulse">
        <h2>家具销售顾问</h2>
        <p>岗位职责</p>
        <ol>
          <li>负责家具（桌椅）产品的销售工作，完成销售任务；</li>
          <li>通过电话、网络等渠道与客户进行沟通，了解客户需求，提供专业的产品推荐和解决方案；</li>
          <li>维护客户关系，定期与客户进行回访，提供优质的售后服务；</li>
          <li>参与市场调研，了解行业动态和竞争对手情况，为公司制定销售策略提供参考；</li>
          <li>协助上级领导完成其他相关工作。</li>
        </ol>
        <p>任职要求</p>
        <ol>
          <li>大专及以上学历，市场营销、家具设计等相关专业优先；</li>
          <li>具备一定的家具销售经验，熟悉家具市场和产品特点；</li>
          <li>具备良好的沟通能力和销售技巧，能够与客户建立良好的合作关系；</li>
          <li>具备较强的学习能力和团队合作精神，能够适应快节奏的工作环境；</li>
          <li>具备较强的市场分析和判断能力，能够根据市场需求制定销售策略；</li>
          <li>熟练使用办公软件，如Word、Excel等。</li>
        </ol>
        <button class="center-block btn btn-warning btn-lg"  @click="showImage = !showImage">投递简历</button>
        <div v-if="showImage" class="overlay" @click="showImage = false">
          <img src="@/assets/img/wechat.jpg" alt="Image" class="qr-code" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { WOW } from 'wowjs';
export default {
  name: "JobChance",
  data() {
    return {
      showImage: false
    };
  },
  mounted(){
    var wow = new WOW();
    wow.init();
  }
};
</script>
<style scoped>
.banner {
  color: #fff;
  font-size: 30px;
  height: 150px;
  line-height: 150px;
  background-image: url("../assets/img/banner_2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}
.JobChance-container {
  margin: 100px;
  padding: 30px;
  transition: all ease 0.5s;
  border: 1px dashed salmon;
}
.JobChance-container h2{
  color: rgb(255, 102, 19);
  font-weight: bolder;
  text-align: center;
}
.JobChance-container p{
font-size: 20px;
  color: rgb(255, 102, 19);
  font-weight: 700;
}
.JobChance-container ol{
    list-style-type: decimal;
    padding-left: 30px;
}
.JobChance-container ol>li{
    font-size: 14px;
    line-height: 2.7rem;
}
@media screen and (max-width: 997px) {
  .JobChance-container {
    margin: 20px 0;
    padding: 20px;
    border: 1px dashed salmon;
  }
}
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.qr-code {
  max-width: 50%;
  max-height: 50%;
}
</style>

