<template>
  <div id="footer" class="container-fluid">
    <div class="logo">
<!--      <img src="@/assets/img/logo_white.png" alt="logo图">-->
      <img src="@/assets/img/jqmy_logo.png" alt="logo图">
    </div>
    <p class="title">钟磊家居有限公司官网</p>
    <p class="address_tel_fax">
    <span>工厂体验馆地址：河北省廊坊市三河县钟磊家具有限公司</span>
      <span>Tel：888-888-888</span>
      <span>Fax：8888-88888888</span>
    </p>
    <p class="email_wx">
      <span>邮箱：zhonglei123@qq.com</span>
      <span>公司微信号：zhonglei123</span>
    </p>
    <p class="copy">Copyright &copy; 2018 - 2019 钟磊家居</p>
  </div>
</template>
<script>
export default {
  name: "Footer",
  data() {
    return {};
  }
};
</script>
<style scoped>
#footer {
  width: 100%;
  height: 100%;
  color: #fff;
  background: #474747;
  overflow: hidden;
  text-align: center;
}
.logo {
  width: 95px;
  height: 45px;
  margin: 50px auto 20px;
}
.logo img{
  width: 95px;
  height: 45px;
  margin: 50px auto 20px;
}
.title {
  font-size: 25px;
  margin-bottom: 20px;
}
.address_tel_fax {
  color: #d3d3d3;
  font-size: 14px;
  margin: 10px 0;
}
.email_wx {
  color: #d3d3d3;
  font-size: 14px;
}
.copy {
  color: #d3d3d3;
  font-size: 14px;
  margin: 50px 0 10px;
}
@media screen and (max-width: 997px) {
  .title {
    font-size: 20px;
  }
  .address_tel_fax {
    font-size: 12px;
  }
  .email_wx {

  font-size: 12px;
}
.copy {
  font-size: 12px;
  margin: 30px 0 10px;
}
}
</style>

