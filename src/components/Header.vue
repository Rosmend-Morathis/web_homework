<template>
    <div class="header">
        <el-row>
            <div class="pagetitle">
                <el-icon :size="20"><Memo/></el-icon>
                <span>设备管理/智能空调</span>
            </div>
            <div class="butts">
                <el-button>
                    <el-icon :size="15"><Search/></el-icon>
                </el-button>
                <el-button>
                    <el-icon :size="15"><Bell/></el-icon>
                </el-button>
                <el-button>
                    <el-icon :size="15"><User/></el-icon>
                    <span>Dreity</span>
                </el-button>
            </div>
        </el-row>  
    </div>
</template>

<script>

</script>

<style scoped>
.header {
    position: relative;
    margin: auto;
    height: 40px;
    padding-top: 10px;
    top: 0;
    left: 0;
}
.pagetitle{
    margin-top: 5px;
    display: flex;
    justify-content: center;
}
.pagetitle span{
    margin-left: 5px;
}

.butts{
    position: absolute;
    right: 0;
}

.el-button{
    border: transparent;
    font-size: 12px;
}

</style>