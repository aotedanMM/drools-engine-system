<template>
  <div class="home-container">
    <div class="m_home">
      <img src="static/img/welcome3.png">
      <p class="m_homeContent">欢迎您使用物联网规则引擎安全控制软件</p>
    </div>
    <p class="m_homeBottom1"> 中国科学院计算技术研究所</p>
    <p class="m_homeBottom2">北京中科天合科技有限公司</p>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
  name: 'Home',
  data() {
    return {
    }
  },
  computed: {
    ...mapGetters([
      'name',
      'roles'
    ])
  }
}
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
.home-container{
  width: 100% !important;
  height: 100% !important;
}
.m_home{width: 50%;height: 40%; position: absolute;top: 20%;left: 25%;text-align: center;}
.m_home img{height: 100%;}
.m_homeContent{line-height: 50px;font-size: 28px;color: #1d5fb9;}
.m_homeBottom1{position: absolute;bottom: 30px;font-size: 16px;color: #666;text-align: center; width: 100%;}
.m_homeBottom2{position: absolute;bottom: 10px;font-size: 14px;color: #666;text-align: center;width: 100%; }
</style>
