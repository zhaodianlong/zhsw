<template>
  <div class="box" @click="toPage">
    <div class="title-box">
      <div class="title">{{ data.name }}</div>
    </div>
    <img :src="data.img" class="system" alt="">
  </div>
</template>

<script>
export default {
  props: {
    data: {
      type: Object,
      default() {
        return {};
      }
    }
  },
  methods: {
    toPage() {
      var a = document.createElement("a");
      a.setAttribute("href", `${this.data.url}`);
      a.setAttribute("target", "_blank");
      a.click();
      document.getElementsByTagName("body")[0].appendChild(a);
    }
  }
}
</script>

<style lang="scss" scoped>
.box {
  width: 400px;
  height: 280px;
  background: url('../assets/system-bg.png') no-repeat;
  background-size: 100% 100%;
  position: relative;
  margin-bottom: 10px;
  .title-box {
    width: 273px;
    height: 29px;
    position: absolute;
    top: 4px;
    left: 50%;
    margin-left: -136.5px;
    background: url('../assets/system-title-bg.png') no-repeat;
    .title {
      font-size:24px;
      font-family: 'Source Han Sans CN';
      font-weight:400;
      color:rgba(254,255,255,1);
      text-align: center;
      margin-top: -16px;
    }
  }
  .system {
    width:360px;
    height: 240px;
    position: absolute;
    top: 50%;
    left: 50%;
    margin-left: -180px;
    margin-top: -119px;
  }
  &:hover {
    transform: scale(1.1);
    cursor: pointer;
  }
}
</style>