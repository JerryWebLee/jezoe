<template>
  <div id="page-1" class="page page-1">
    <div class="bg-container1"></div>
    <div class="bg-container2"></div>
    <img src="../../assets/images/bnr-1.png" />
    <div class="act-container">
      <div class="act">
        <div class="act-hide"></div>
        <img src="../../assets/images/img-sb.png" class="img-sb" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
// 响应式
@media screen and (min-width: 1150px) {
  .moblie-nav {
    display: none;
  }
}
@media screen and (max-width: 1150px) and (min-width: 640px) {
  #page-1.page-1 {
    width: 640px;
    height: 100%;
  }
}
@media screen and (min-width: 640px) {
  .bg-container1 {
    display: none;
  }
  .bg-container2 {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: #151624;
  }
  .act-container {
    position: fixed;
    left: 0;
    right: 0;
    bottom: 95px;
    margin: auto;
    width: 200px;
    height: 200px;
    bottom: 95px;
  }
  div.act {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    top: 0;
    margin: auto;
    width: 80px;
    height: 80px;
    line-height: 80px;
    border: 1px solid #fff;
    border-radius: 50%;
    transition: all 0.6s ease-in-out;
    &:hover {
      width: 110px;
      height: 110px;
      border: 1px solid rgba(255, 255, 255, 0);
      .act-hide {
        width: 80px;
        height: 80px;
        background-color: rgba(255, 255, 255, 0.1);
        border: 1px solid rgba(255, 255, 255, 1);
      }
    }
    .act-hide {
      transition: all 0.5s 0.1s ease-in-out;
      width: 16px;
      height: 16px;
      position: absolute;
      left: 0;
      top: 0;
      bottom: 0;
      right: 0;
      margin: auto;
      border-radius: 50%;
      border: 1px solid rgba(255, 255, 255, 0);
    }
    .img-sb {
      width: 18px;
      height: 42px;
      position: absolute;
      z-index: 200;
      left: 0;
      top: 0;
      bottom: 0;
      right: 0;
      margin: auto;
      overflow: hidden;
    }
  }
}
@media screen and (max-width: 639px) {
  .bg-container2 {
    display: none;
  }
  .bg-container1 {
    display: block;
    height: 100%;
    width: 100%;
    background: url("../../assets/images/index-mb-bg.jpg") no-repeat;
    background-size: cover;
  }
  #page-1 > img {
    position: absolute;
    width: 300px;
    height: 117.3px;
    left: 0;
    top: 200px;
    right: 0;
    margin: auto;
  }
}
// 页面布局
.page-1 {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  img {
    position: absolute;
    width: 734px;
    height: 287px;
  }
}
</style>
