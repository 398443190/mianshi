<template>
  <div class="common-card">
    <div class="title">{{title}}</div>
    <div class="value">{{value}}</div>
    <div class="chart">
      <slot></slot>
    </div>
    <div class="total">
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    value: {
      type: String,
      default: '   '
    }
  }
}
</script>

<style lang="scss" scoped>
.title {
  font-size: 18px;
  color: red;
}
.value {
  font-size: 15px;
  color: #fff;
  letter-spacing: 1px;
  margin-top: 8px;
}
.chart {
  height: 450px;
}
.line {
  margin: 10px 0;
  border-top: 1px solid #eee;
}
.total {
  font-size: 12px;
  color: #666;
}
</style>
