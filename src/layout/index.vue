<template>
  <el-container>
    <i
      class="icons"
      :class="isCollapse ? 'el-icon-s-unfold' : 'el-icon-s-fold'"
      @click="isCollapse = !isCollapse"
    />
    <el-header>
      <Nav />
    </el-header>
    <el-container>
      <el-aside :width="isCollapse ? '64px' : '200px'">
        <AsideNav :is-collapse="isCollapse" />
      </el-aside>
      <el-main>Main</el-main>
    </el-container>
  </el-container>
</template>

<script>
import Nav from './header/nav'
import AsideNav from './aside/aside-nav'
export default {
  components: { Nav, AsideNav },
  data() {
    return {
      isCollapse: true
    }
  }
}
</script>

<style lang="less" scoped>
.el-container {
  position: absolute;
  width: 100%;
  top: 0px;
  left: 0;
  bottom: 0;
}
.el-header {
  padding: 0;
  z-index: 1000;
}

.el-header .el-menu {
  border-bottom: none;
}
.el-aside,
.el-main {
  padding-top: 60px;
}
.el-aside {
  background: #545c64;
}
.el-aside .el-menu {
  border-right: none;
}
.el-icon-s-unfold:before,
.el-icon-s-fold:before {
  position: fixed;
  top: 75px;
  font-size: 30px;
  z-index: 464564;
}
.el-icon-s-unfold:before {
  transition-duration: 0.2s;
  left: 64px;
}
.el-icon-s-fold:before {
  transition-duration: 0.5s;
  left: 200px;
}
</style>
