<template>
  <header class="nav">
    <div class="nav-logo">
      <a href="javascript:;">
        <img src="../../assets/images/logo.png" alt="logo" />
      </a>
    </div>
    <div class="nav-ghh">
      <div class="ghh ghh-1"></div>
      <div class="ghh ghh-2"></div>
      <div class="ghh ghh-3"></div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
.nav {
  position: relative;
  top: 0;
  width: 100%;
  height: 50px;
  padding: 2px 0;
  background-color: rgba(0, 0, 0, 0.2);
  .nav-logo {
    margin-left: 10px;
  }
  .nav-ghh {
    position: absolute;
    width: 40px;
    height: 30px;
    top: 0;
    bottom: 0;
    right: 30px;
    margin: auto 0;
    .ghh {
      position: absolute;
      left: 0;
      right: 0;
      margin: auto;
      width: 33.6px;
      height: 3px;
      background-color: #ed6c00;
      &.ghh-1 {
        top: 5px;
      }
      &.ghh-2 {
        top: 0;
        bottom: 0;
      }
      &.ghh-3 {
        bottom: 5px;
      }
    }
  }
}
</style>
