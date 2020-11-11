<template>
  <div class="container">
    <loading v-if="ready">Loading...</loading>
    <div :options="{ width: '100%', height: '100%' }" v-else>
      <div class="header">
        <top-header />
      </div>
      <div class="center">
          <div class="left">
              <total-left />
          </div>
          <div class="right">
              <total-right />
          </div>
      </div>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
import Loading from '../../components/Loading'
import TopHeader from '../../components/TopHeader'
import TotalLeft from '../../components/Left'
import TotalRight from '../../components/Right'

export default {
  components: {
    Loading,
    TopHeader,
    TotalLeft,
    TotalRight
  },
  data() {
    return {
      ready: true,
    };
  },
  mounted() {
      this.readyed()
  },
  methods: {
    readyed() {
      setTimeout(() => {
        this.ready = false
      }, 500)
    },
  },
};
</script>

<style lang="less" scoped>
.container {
  //width: 100%;
  height: 100vh;
  // background-color: rgb(50, 47, 48);
  background: rgb(29, 29, 29);
  color: #fff;
  overflow-y: auto;
    .separator-wrapper {
      height: 10px;
    }

    .center {
      flex: 1;
      display: flex;

      .left {
        flex: 0 0 400px;
        display: flex;
        flex-direction: column;
        width: 860px;
        height: 100%;
        margin: 0 10px;
        box-sizing: border-box;
        background: rgb(60, 61, 64);
      }

      .right {
        flex: 1;
        display: flex;
        flex-direction: column;
        height: 100%;
        margin: 0 10px;
        max-width: 2960px;
        overflow: hidden;

        .right-top1 {
          height: 206px;
          margin-bottom: 20px;
        }

        .right-top2 {
          height: 48px;
          margin-bottom: 20px;
        }

        .right-bottom {
          flex: 1;
          display: flex;

          .right-left {
            display: flex;
            flex-direction: column;
            width: 1917px;

            .right-left1 {
              height: 999px;
            }

            .right-left2 {
              height: 80px;
              padding-top: 20px;
              box-sizing: border-box;
            }

            .right-left3 {
              height: 350px;
              margin-top: 10px;

              .dv-border-box-8 {
                width: 100%;
                height: 100%;
                padding: 5px;
                box-sizing: border-box;
                background: rgb(66, 68, 70);
                border-radius: 10px;
                box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.3);
              }
            }

            .right-left4 {
              height: 220px;
              margin-top: 10px;
            }
          }

          .right-right {
            flex: 1;
            display: flex;
            flex-direction: column;
            margin-left: 10px;

            .right-right1 {
              width: 100%;
              height: 999px;
              padding-right: 10px;
              box-sizing: border-box;
            }

            .right-right2 {
              width: 100%;
              height: 650px;
              margin-top: 20px;
            }
          }
        }
      }
    }
}
</style>
