<template>
<div class="">
  <div class="titleed"><span class="">数据分析关联表</span>
    <el-button class="button" type="text"><i class="el-icon-download" />下载</el-button>
  </div>
  <el-table
    :data="tableData"
    border
    style="width: 100%">
    <el-table-column
      prop="date"
      label="日期"
      width="100">
    </el-table-column>
    <el-table-column
      prop="date"
      align="center"
      label="全社会用电量"
      width="180">
    </el-table-column>
    <el-table-column
      prop="name"
      align="center"
      label="全社会用电量增长率"
      width="180">
    </el-table-column>
    <el-table-column
      prop="address"
      align="center"
      label="太原月平均温度">
    </el-table-column>
    <el-table-column
      prop="address"
      align="center"
      label="太原月平均温度增长">
    </el-table-column>
    <el-table-column
      prop="address"
      align="center"
      label="全社会用电量对太原月平均温度的弹性系数">
    </el-table-column>
  </el-table>
</div>
</template>

<script>
export default {
  data () {
    return {
      tableData: [{
        date: '2016-05-02',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄'
      }, {
        date: '2016-05-04',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1517 弄'
      }, {
        date: '2016-05-01',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1519 弄'
      }, {
        date: '2016-05-03',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1516 弄'
      }]
    }
  }
}
</script>

<style lang="less">
.titleed {
  height: 50px;
  line-height: 50px;
  padding: 0 10px;
  color: red;
  display: flex;
  justify-content: space-between;

}
.el-table th, .el-table tr {
    background-color: #1d1d1d !important;
    color: #fff;
    :hover{
    background-color: #1d1d1d !important;
    }
}
</style>
