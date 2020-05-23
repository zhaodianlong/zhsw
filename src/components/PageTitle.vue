<template>
  <div class="box">
    <div class="t-box">
      <img src="../assets/title.png" class="title" alt="">
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.box {
  width: 100%;
  min-width: 1920px;
  height: 70px;
  .t-box {
    width: 993px;
    height: 70px;
    background: url('../assets/title-box.png');
    margin: 0 auto;
    text-align: center;
    .title {
      width: 612px;
      height: 47px;
      margin-top: 14px;
    }
  }
}
</style>