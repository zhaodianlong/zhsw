<template>
  <div id="app">
    <PageTitle />
    <div class="content">
      <div class="left">
        <SystemItem v-for="(item, index) of leftSystems" :key="index" :data="item" />
      </div>
      <div class="earth-box">
        <div class="earth-bg">
          <img src="./assets/earth.png" class="earth" alt="">
        </div>
        <img src="./assets/earth-footer.png" class="earth-footer" alt="">
      </div>
      <div class="right">
        <SystemItem v-for="(item, index) of rightSystems" :key="index" :data="item" />
      </div>
    </div>
  </div>
</template>

<script>
import PageTitle from '@/components/PageTitle';
import SystemItem from '@/components/SystemItem';

export default {
  name: 'App',
  components: {
    PageTitle,
    SystemItem
  },
  data() {
    return {
      leftSystems: [
        {
          name: '管网GIS系统',
          img: require('./assets/system1.png')
        },
        {
          name: '智能巡检系统',
          img: require('./assets/system2.png')
        },
        {
          name: '生产调度SCADA系统',
          img: require('./assets/system3.png')
        }
      ],
      rightSystems: [
        {
          name: '营业收费系统',
          img: require('./assets/system4.png')
        },
        {
          name: '安全生产系统',
          img: require('./assets/system5.png')
        },
        {
          name: '办公自动化',
          img: require('./assets/system6.png')
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
#app {
  font-family: 'Source Han Sans CN';
  background: url('./assets/bg.png') no-repeat fixed top;
  background-size: 100% 100%;
  width: 100%;
  height: 100vh;
  min-width: 1920px;
  overflow: hidden;
  .content {
    margin-top: 20px;
    text-align: center;
    .left {
      width: 392px;
      margin-left: 139px;
      float: left;
    }
    .right {
      width: 392px;
      margin-right: 139px;
      float: right;
    }
    .earth-box {
      width: 600px;
      height: 855px;
      display: inline-block;
      margin: 134px auto 0;
      overflow: hidden;
      .earth-bg {
        .earth {
          width: 600px;
          height: 600px;
          border-radius: 100%;
          animation: myfirst 120s linear infinite;
          animation-play-state: running;
        }
        @keyframes myfirst {
          0% {
            transform: rotate(0deg);
          } 
          100% {
            transform: rotate(360deg);
          }
        }
      }
      .earth-footer {
        width: 600px;
        height: 350px;
        margin-top: -202px;
      }
    }
  }
}
</style>
