<template>
  <el-container>
      <el-aside width="200px">
          <Sidebar/>
      </el-aside>
      <el-container>
          <el-header>Header</el-header>
          <el-main>Main</el-main>
      </el-container>
  </el-container>
</template>

<script>
import Sidebar from './Sidebar.vue'
export default {
  data(){
      return{}
  },
  components:{
    Sidebar
  }
}
</script>

<style>
html, body{
    margin: 0;
    padding: 0;
    height: 100%;
}

.el-container{
    height: 100%;
}

.el-aside::-webkit-scrollbar{
    display: none;
}
</style>
