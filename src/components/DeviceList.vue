<template>
    <div class="devices">
        <div>
            <el-row>
                <div class="ttl_status">
                    <span>总数量：40&nbsp;&nbsp;&nbsp;&nbsp;</span>
                    <span>在线数量：20&nbsp;&nbsp;&nbsp;&nbsp;</span>
                    <span>离线数量：20</span>
                </div>
            </el-row>
        </div>
        <div class="device_search">
            <el-row>
                <el-col :span="6">
                    <span>在线状态：</span>
                    <el-select
                     v-model="value1"
                     placeholder="请选择"
                     style="width: 200px;"
                    >
                        <el-option
                         v-for="item in status"
                         :key="item.value"
                         :label="item.label"
                         :value="item.value"   
                         style="width: 200px;"
                        />
                    </el-select>
                </el-col>
                <el-col :span="6">
                    <span>房号：</span>
                    <el-input style="width: 200px" placeholder="请输入房号">
                    </el-input>
                </el-col>
                <el-col :span="6">
                    <span>房间名称：</span>
                    <el-input style="width: 200px" placeholder="请输入房间名称">
                    </el-input>
                </el-col>
                <el-col :span="6">
                    <el-button type="primary">查 询</el-button>
                    <el-button>重 置</el-button>
                </el-col>
            </el-row>  
        </div>
        
    </div>
</template>

<script lang="js" setup>
import {ref} from 'vue'

const value1 = ref([])

const status = [
    {
        value: '全部',
        label: '全部'
    },
    {
        value: '在线',
        label: '在线'
    },
    {
        value: '离线',
        label: '离线'
    },
]

</script>

<style scoped>

.ttl_status{
    font-size: 12px;
    color:green;
    margin-left: 20px;
}
.device_search{
    margin-top: 10px;
    padding: 5px;
    font-size: 14px;

}

</style>