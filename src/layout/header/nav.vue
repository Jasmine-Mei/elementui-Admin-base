<template>
  <el-menu
    :default-active="activeIndex2"
    class="el-menu-demo"
    mode="horizontal"
    text-color="#fff"
    active-text-color="#ffd04b"
    menu-trigger="click"
    @select="handleSelect"
  >
    <el-menu-item class="logo">logo</el-menu-item>
    <el-submenu index="1" class="fr">
      <template slot="title">
        <img
          class="img"
          src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1606997306640&di=60915e8e75dd2e9f2765383bc166eb6e&imgtype=0&src=http%3A%2F%2Fimg.ratoo.net%2Fuploads%2Fallimg%2F190513%2F7-1Z513101959.gif"
          alt=""
        ></template>
      <el-menu-item>退出登录</el-menu-item>
    </el-submenu>
  </el-menu>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: '1',
      activeIndex2: '1'
    }
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>

<style lang="less" scoped>
.fr {
  float: right;
}
.logo {
  width: 200px;
}
.img {
  width: 30px;
  border-radius: 50%;
}
/deep/.el-icon-arrow-down:before{
  font-size: 20px;
}
</style>
