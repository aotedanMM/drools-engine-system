<template>
  <el-scrollbar wrap-class="scrollbar-wrapper">
    <div class="m_logo">
<!--      <img src="static/img/logo3.png">-->
      <p style="color: #fff;font-size: 16px;line-height: 60px">物联网规则引擎安全控制软件</p>
    </div>
    <el-menu
      :show-timeout="200"
      :default-active="$route.path"
      :collapse="isCollapse"
      mode="vertical"
      background-color="#172b59"
      text-color="#fff"
      active-text-color="#fff"
      width="260"
    >
      <sidebar-item v-for="route in routes" :key="route.name" :item="route" :base-path="route.path"/>
    </el-menu>
  </el-scrollbar>
</template>

<script>
import { mapGetters } from 'vuex'
import SidebarItem from './SidebarItem'

export default {
  components: { SidebarItem },
  computed: {
    ...mapGetters([
      'sidebar'
    ]),
    routes() {
      return this.$router.options.routes
    },
    isCollapse() {
      return !this.sidebar.opened
    }
  }
}
</script>
