<template>
  <div class="sidebar">
    <div class="logo">
      <img src="@/assets/logo_transparent.png" alt="">
    </div>
    <el-col>
      <el-menu 
        active-text-color="#ffd04b"
        background-color="rgb(0, 21, 41)"
        default-active="2" 
        class="el-menu-vertical" 
        text-color="#fff" 
      >
        <el-menu-item index="1">
            <el-icon :size="40" style="margin-top: 5px"><House/></el-icon>
            <span>主页</span>
        </el-menu-item>
        <el-sub-menu index="2">
          <template #title>
            <el-icon :size="40"><SetUp/></el-icon>
            <span>用电架构</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="1-1">楼宇管理</el-menu-item>
            <el-menu-item index="1-2">部门管理</el-menu-item>
            <el-menu-item index="1-3">房间管理</el-menu-item>
          </el-menu-item-group>
        </el-sub-menu>
        <el-sub-menu index="3">
          <template #title>
            <el-icon :size="40"><Operation/></el-icon>
            <span>设备管理</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="2-1">智能空调</el-menu-item>
            <el-menu-item index="2-2">智能空开</el-menu-item>
            <el-menu-item index="2-3">智能开关</el-menu-item>
            <el-menu-item index="2-4">人体检测相机</el-menu-item>
          </el-menu-item-group>
        </el-sub-menu>
        <el-sub-menu index="4">
          <template #title>
            <el-icon :size="40"><CollectionTag/></el-icon>
            <span>用电管理</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="3-1">用电控制</el-menu-item>
            <el-menu-item index="3-2">用电能耗</el-menu-item>
            <el-menu-item index="3-3">自动关停</el-menu-item>
          </el-menu-item-group>
        </el-sub-menu>
        <el-menu-item index="5">
          <el-icon :size="40"><Calendar/></el-icon>
          <span>系统日志</span>
        </el-menu-item>
      </el-menu>
    </el-col>
  </div>
</template>
  
<script>
export default {
  data() {
    return {
      activeMenu: 'home',
    };
  },
  methods: {
    handleMenuSelect(index) {
      this.activeMenu = index;
      // 在这里可以根据index进行路由跳转或其他操作
    },
  },
};
</script>
  
<style scoped>

.sidebar {
  width: 200px;
  height: 100%;
  background: rgb(0, 33, 64);
}

.logo{
  width: 100%;
}
.logo img{
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.el-menu{
  height: 100vh;
}

.el-menu-vertical {
  height: 100%;
  border: none;
  background: transparent;
}

.el-menu-item{
  background:rgb(0, 21, 41);
}
</style>
  