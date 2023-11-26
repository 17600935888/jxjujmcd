<template>
  <div id="ContactUs">
    <div class="banner container-fuild text-center">联系我们</div>
    <div class="container">
      <div class="container-fuild ContactUs-container">
        <div class="row">
          <div class="col-xs-12 col-sm-12 col-md-4">
            <div class="contact-info">
              <h2 class="text-center">联系方式</h2>
              <div class="row">
                <div class="item">
                  <img src="@/assets/img/phone_icon.png" alt="Phone Icon" class="icon" />
                  <p class="text">19876567898   (工作日：8:00~18:00)</p>
                </div>
               
              </div>
              <div class="row">
                <div class="item">
                  <div class="col-sm-12 text-center">
                    <img src="@/assets/img/wechat_icon.png" alt="WeChat Icon"  class="connect_icon"/>
                    <p class="text">19876567898   (工作日：8:00~18:00)</p>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="item">
                  <div class="col-sm-12 text-center">
                    <p><img src="@/assets/img/qq_icon.jpeg" alt="QQ Icon"  class="connect_icon"/>178953654</p>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="item">
                  <div class="col-sm-12 text-center">
                    <p><img src="@/assets/img/email_icon.jpeg" alt="Email Icon"  class="connect_icon"/>178953654@qq.com</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="col-xs-12 col-sm-12 col-md-8">
            <div id="map" class="wow zoomIn"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { WOW } from 'wowjs'
import BMap from "BMap";
export default {
  name: "ContactUs",
  data() {
    return {};
  },
  mounted() {
    var map = new BMap.Map("map"); // 创建地图实例
    var point = new BMap.Point(116.83,39.96); // 创建点坐标
    map.centerAndZoom(point, 18); // 初始化地图，设置中心点坐标和地图级别
    map.enableScrollWheelZoom(true); //开启鼠标滚轮缩放
    var marker = new BMap.Marker(point); // 创建标注
    map.addOverlay(marker); // 将标注添加到地图中
    var opts = {
      width: 50, // 信息窗口宽度
      height: 10, // 信息窗口高度
      title: "燕郊京郊批发市场" // 信息窗口标题
    };
    var infoWindow = new BMap.InfoWindow(
      "钟磊家具",
      opts
    ); // 创建信息窗口对象
    map.openInfoWindow(infoWindow, map.getCenter()); // 打开信息窗口
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
  background-image: url("../assets/img/banner_1.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}
.ContactUs-container {
  padding: 80px 0;
  transition: all ease 0.5s;
  box-sizing: border-box;
}
#map {
  width: 100%;
  height: 365px;
}
.row {
  margin-right: 0;
  margin-left: 0;
}
@media screen and (max-width: 997px) {
  .ContactUs-container {
    padding: 20px 0;
  }
}
.text-center {
  text-align: center;
}
.connect_icon {
  width: 30px;
  height: 25px;
  margin-top: auto;
  margin-bottom: auto;
  margin-left: 0;
  margin-right: auto;
}
.item {
  display: flex;
  align-items: center;
  border-bottom: 1px solid #000;
}

.icon {
  width: 30px;
  height: 30px;
  margin-right: 10px;
}

.text {
  flex-grow: 1;
  margin: 0; /* 添加这一行 */
}
</style>

