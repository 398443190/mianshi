<template>
  <common-card
  >
    <template>
  <div :id="id" :class="className" :style="{height:height,width:width}" />
    </template>
  </common-card>
</template>

<script>
import echarts from 'echarts'
import commonCardMixin from '../../mixins/commonCardMixin'
export default {
  mixins: [commonCardMixin],
  props: {
    className: {
      type: String,
      default: 'chart'
    },
    id: {
      type: String,
      default: 'chart'
    },
    width: {
      type: String,
      default: '200px'
    },
    height: {
      type: String,
      default: '200px'
    }
  },
  data () {
    return {
      chart: null
    }
  },
  mounted () {
    this.initChart()
  },
  beforeDestroy () {
    if (!this.chart) {
      return
    }
    this.chart.dispose()
    this.chart = null
  },
  methods: {
    initChart () {
      this.chart = echarts.init(document.getElementById(this.id))

      this.chart.setOption({
        title: {
          text: '自然增长分析',
          textStyle: {
            fontWeight: 'normal',
            fontSize: 18,
            color: 'red'
          },
          left: '1%'
        },
        tooltip: {
          trigger: 'axis',
          axisPointer: {
            type: 'shadow',
            lineStyle: {
              color: '#57617B'
            }
          }
        },
        legend: {
          top: 25,
          icon: 'rect',
          itemWidth: 14,
          itemHeight: 5,
          itemGap: 13,
          data: ['太原平均温度增长率', '全社会电量增长率'],
          textStyle: {
            fontSize: 12,
            color: '#F1F1F3'
          }
        },
        grid: {
          top: 80,
          left: '2%',
          right: '2%',
          bottom: '2%',
          containLabel: true
        },
        xAxis: [{
          type: 'category',
          axisLine: {
            lineStyle: {
              color: '#57617B'
            }
          },
          data: ['2020/01', '2020/02', '2020/03', '2020/04', '2020/05', '2020/05', '2020/06', '2020/07', '2020/08', '2020/09', '2020/10', '2020/11', '2020/12']
        }],
        yAxis: [{
          type: 'value',
          name: '电量/万kw.h',
          axisTick: {
            show: false
          },
          axisLine: {
            lineStyle: {
              color: '#57617B'
            }
          },
          axisLabel: {
            margin: 10,
            textStyle: {
              fontSize: 14
            }
          },
          splitLine: {
            lineStyle: {
              color: '#57617B'
            }
          }
        },
        {
          type: 'value',
          name: '温度(°C)',
          min: 0,
          max: 25,
          interval: 5,
          axisLabel: {
            formatter: '{value} '
          }
        }],
        series: [{
          name: '太原平均温度增长率',
          type: 'bar',
          barWidth: '35%',
          backgroundStyle: {
            color: 'rgba(220, 220, 220, 0.8)'
          },
          data: [220, 182, 191, 134, 150, 120, 110, 125, 145, 122, 165, 122, 200]
        }, {
          name: '全社会电量增长率',
          type: 'line',
          smooth: true,
          symbol: 'circle',
          symbolSize: 5,
          showSymbol: false,
          lineStyle: {
            normal: {
              width: 1
            }
          },
          itemStyle: {
            normal: {
              color: 'rgb(0,136,212)',
              borderColor: 'rgba(0,136,212,0.2)',
              borderWidth: 12

            }
          },
          data: [12, 11, 12, 15, 22, 15, 22, 20, 12, 11, 14, 15, 20]
        }]
      })
    }
  }
}
</script>
