<template>
  <common-card
    title="累计销售额"
    value="全社会用电月度与太原月平均温度关联分析"
  >
    <template>
      <div class="compare-wrapper">
        <div class="compare-wrapper-item">
          <div class="compare">
            <div class="number day">0.6</div>
            <div class="title day">相关系数</div>
          </div>
          <div class="compare">
            <div class="number month">271</div>
            <div class="title month">平均弹性系数</div>
          </div>
        </div>
        <div class="footered">
          <div>最优预测公式</div>
          <span>y=(adad.adasd) +qeqweqwe</span>
        </div>
      </div>
    </template>
  </common-card>
</template>

<script>
import commonCardMixin from '../../mixins/commonCardMixin'

export default {
  mixins: [commonCardMixin]
}
</script>

<style lang="scss" scoped>
.compare-wrapper {
  height: 100px;
  padding: 30px;
  .compare-wrapper-item {
    display: flex;
    .compare {
      display: flex;
      align-items: center;
      flex-direction: column;
      font-size: 12px;
      color: #666;
      height: 200px;
      padding-right: 20px;
      .number {
        font-size: 35px;
      }
      .title {
        font-size: 10px;
        padding-top: 20px;
      }
    .day {
      color: darkcyan;
    }
    .month {
      color: darkorange;
    }
    }
  }
    .footered {
      padding: 10px;
      height: 100px;
      background: #666;
    }
}
</style>
