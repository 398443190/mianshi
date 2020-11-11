<template>
  <div class="right">
    <div class="header">
      <el-button type="danger">相关因素分析</el-button>
      <el-button>行业相关分析</el-button>
    </div>
    <div class="select">
      <div class="select-item">
        <label for="" class="label">负荷指标</label>
        <el-select
          v-model="value"
          placeholder="请选择"
          size="small"
          class="sele"
        >
          <el-option label="全社会用电月度" value="全社会用电月度"> </el-option>
        </el-select>
      </div>
      <div class="select-item">
        <label for="" class="label">相关因素</label>
        <el-select
          v-model="value"
          placeholder="请选择"
          size="small"
          class="sele"
        >
          <el-option label="item.label" value="item.value"> </el-option>
        </el-select>
      </div>
      <div class="select-item">
        <label for="" class="label">分析时间</label>
        <el-date-picker
          v-model="value1"
          type="date"
          placeholder=""
          class="sele"
        >
        </el-date-picker>
        <span>至</span>
        <el-date-picker
          v-model="value1"
          type="date"
          placeholder=""
          class="sele"
        >
        </el-date-picker>
      </div>
      <el-button type="primary">分析</el-button>
    </div>
    <div class="echartBody">
      <el-row :gutter="20">
        <el-col :span="12">
          <el-card style="height: 500px">
            <add-fenxi />
          </el-card>
        </el-col>
        <el-col :span="12">
          <el-card style="height: 500px">
            <add-fenxi1 height="100%" width="100%" id="id1" />
          </el-card>
        </el-col>
        <el-col :span="12" style="paddingtop: 20px">
          <el-card style="height: 500px">
            <add-fenxi2 height="100%" width="100%" id="id2" />
          </el-card>
        </el-col>
        <el-col :span="12" style="paddingtop: 20px">
          <el-card style="height: 500px">
            <add-fenxi3 height="100%" width="100%" id="id3" />
          </el-card>
        </el-col>
        <el-col :span="12" style="paddingtop: 20px">
          <el-card style="height: 500px">
            <add-fenxi4 height="100%" width="100%" id="id4" />
          </el-card>
        </el-col>
        <el-col :span="12" style="paddingtop: 20px">
          <el-card style="height: 500px">
            <add-fenxi5 height="100%" width="100%" id="id5" />
          </el-card>
        </el-col>
        <el-col :span="24" style="paddingtop: 20px">
          <el-card style="height: 500px" class="table">
            <add-fenxi6 />
          </el-card>
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>
import AddFenxi from '../AddFenxi'
import AddFenxi1 from '../AddFenxi1'
import AddFenxi2 from '../AddFenxi2'
import AddFenxi3 from '../AddFenxi3'
import AddFenxi4 from '../AddFenxi4'
import AddFenxi5 from '../AddFenxi5'
import AddFenxi6 from '../AddFenxi6'
export default {
  data () {
    return {
      value: '全社会用电月度',
      value1: ''
    }
  },
  components: {
    AddFenxi,
    AddFenxi1,
    AddFenxi2,
    AddFenxi3,
    AddFenxi4,
    AddFenxi5,
    AddFenxi6
  }
}
</script>

<style lang='scss'>
.right {
  .header {
    padding: 20px;
    border: 1px solid #666;
  }
  .select {
    padding: 20px;
    border: 1px solid #666;
    .select-item {
      display: inline-block;
      .label {
        padding-right: 10px;
      }
      .sele {
        padding-right: 20px;
      }
      span {
        padding: 0 20px;
      }
    }
    .el-select {
      .el-input__inner {
        background: #1d1d1d;
        color: #fff;
      }
    }
    .el-date-editor {
      .el-input__inner {
        background: #1d1d1d;
        color: #fff;
      }
    }
  }
  .echartBody {
    padding: 20px;
    border: 1px solid #666;
    .el-card {
      background: #1d1d1d;
    }
    .table {
      .el-card__body {
        padding: 0;
      }
    }
  }
}
</style>
