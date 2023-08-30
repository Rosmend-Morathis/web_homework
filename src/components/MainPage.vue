<template>
  <el-container>
      <el-aside width="200px">
          <Sidebar/>
      </el-aside>
      <el-container>
        <el-header>
            <Header/>
        </el-header>
        <el-main>
            <DeviceList/>
        </el-main>
      </el-container>
  </el-container>
</template>

<script>
import Sidebar from './Sidebar.vue'
import Header from './Header.vue'
import DeviceList from './DeviceList.vue'
export default {
  data(){
      return{}
  },
  components:{
    Sidebar,
    Header,
    DeviceList
  }
}
</script>

<style>
html, body{
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
}

.el-container{
    height: 100%;
}

.el-aside::-webkit-scrollbar{
    display: none;
}

.el-header{
    width: 100%;
    height: 40px;
    margin: 0;
    border-bottom: 2px solid rgba(0, 0, 0, 0.1);
    font-size: 14px;
}
</style>
