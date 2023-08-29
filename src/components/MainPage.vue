<template>
  <el-container>
      <el-aside width="200px">
          <navi/>
      </el-aside>
      <el-container>
          <el-header>Header</el-header>
          <el-main>Main</el-main>
      </el-container>
  </el-container>
</template>

<script>
import Navi from './Navi.vue'
export default {
  data(){
      return{}
  },
  components:{
      Navi
  }
}
</script>

<style>

</style>
