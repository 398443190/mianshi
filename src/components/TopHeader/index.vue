<template>
  <div class="top-header">
    <img
      class="logo"
      src="https://datav.oss-cn-hangzhou.aliyuncs.com/uploads/images/54149aa06f26afcf26f42d66c999ee8b.png"
    />
    <div class="logo-text">
        <el-button type="text">电力电量</el-button>
        <el-button type="text">相关因素</el-button>
        <el-button type="text">智能预测</el-button>
        <el-button type="text">数据报表</el-button>
        <el-button type="text">数据关联分析</el-button>
        <el-button type="text">系统管理</el-button>
    </div>
    <div class="right-text">
        <span>算法说明<i class="el-icon-user"/></span>
        <span>操作手册<i class="el-icon-user"/></span>
        <span><i class="el-icon-user"/>admin</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'topHeader'
}
</script>

<style lang="scss" scoped>
.top-header {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 40px;
  background: rgb(36, 31, 32);
  padding: 0 20px;
  box-sizing: border-box;
  border-bottom: 2px solid #666;

  .logo {
    width: 100px;
    height: 50px;

  }

  .logo-text {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    .el-button {
      padding: 0 20px;
      color: #fff;
      border: none;
      border-radius: 0%;
      height: 40px;
      &:hover{
        background: crimson;
      }
    }
  }

  .right-text {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    span {
      padding: 0 20px;
    }
  }
}
</style>
