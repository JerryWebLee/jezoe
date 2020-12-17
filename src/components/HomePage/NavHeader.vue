<template>
  <header class="nav">
    <div class="nav-logo">
      <a href="javascript:;">
        <img src="../../assets/images/logo.png" alt="logo" />
      </a>
    </div>
    <div class="nav-container">
      <div class="nv1">
        <ul>
          <li><a href="">云搜宝</a></li>
          <li></li>
          <li><a href="">整合营销</a></li>
          <li></li>
          <li><a href="">云客网</a></li>
          <li></li>
          <li><a href="">社群化营销</a></li>
        </ul>
      </div>
      <div class="nv2">
        <ul>
          <li><a href="">关于</a></li>
          <li></li>
          <li><a href="">资讯</a></li>
          <li></li>
          <li><a href="">招聘</a></li>
          <li></li>
          <li><a href="">联络</a></li>
        </ul>
      </div>
    </div>
    <div :class="['nav-ghh', changeColor]">
      <div :class="['ghh-container', rotateAll]" @click="ghhTransition">
        <div :class="['ghh', 'ghh-1', rotateDown, bgColor]"></div>
        <div class="ghh ghh-2" v-show="ghhShow"></div>
        <div :class="['ghh', 'ghh-3', rotateUp, bgColor]"></div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      ghhShow: true
    };
  },
  methods: {
    // nav-ghh点击事件触发过渡动画
    ghhTransition: function() {
      this.ghhShow = !this.ghhShow;
      this.$emit("changeHeight", !this.ghhShow);
    }
  },
  computed: {
    bgColor() {
      return !this.ghhShow ? "bgColor" : "";
    },
    rotateAll() {
      return !this.ghhShow ? "rotateAll" : "";
    },
    rotateDown() {
      return !this.ghhShow ? "rotateDown" : "";
    },
    rotateUp() {
      return !this.ghhShow ? "rotateUp" : "";
    },
    changeColor() {
      return !this.ghhShow ? "change-color" : "";
    }
  }
};
</script>

<style lang="less" scoped>
// 响应式
@media screen and (min-width: 1151px) {
  header.nav {
    height: 70px;
    background-color: #373b46;
    .nav-logo {
      margin-left: 90px;
    }
    .nav-ghh {
      display: none;
    }

    ul {
      margin: 0;
      padding: 0;
    }
    ul li {
      list-style: none;
      a {
        text-decoration: none;
        color: #d6d6d8;
        font-size: 14px;
        &:hover {
          color: red;
        }
      }
    }
    .nav-container {
      margin-left: 340px;
      margin-right: 64px;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .nv2 ul {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .nv1 ul {
      width: 400px;
      li {
        display: inline-block;
        height: 45px;
        line-height: 45px;
      }
    }
    .nv2 ul {
      width: 180px;
      li a {
        font-size: 12px;
      }
    }
    .nv1 ul li:nth-of-type(even) {
      display: inline-block;
      width: 6px;
      height: 6px;
      margin-top: 20px;
      border-radius: 50%;
      background-color: #fff;
      margin: 0 10px;
      margin-bottom: 1px;
    }
  }
}
@media screen and (max-width: 1150px) {
  .nav-container {
    display: none;
  }
}
@media screen and (max-width: 1150px) and (min-width: 640px) {
  header.nav {
    width: 640px;
    height: 70px;
    .nav-logo {
      margin-left: 30px;
    }
    .nav-ghh {
      border: 2px solid #ed6c00;
      border-radius: 5px;
      width: 48px;
      height: 38px;
    }
    .change-color {
      border: 2px solid #fff !important;
    }
  }
}

// 点击nav-ghh后的过渡类
.bgColor {
  background-color: #fff !important;
}
.rotateAll {
  height: 38px;
  transform: rotate(90deg);
}
.rotateDown {
  transform: translateY(10.5px) rotate(-45deg);
}
.rotateUp {
  transform: translateY(-10.5px) rotate(45deg);
}
// 页面布局样式文件
.nav {
  position: absolute;
  z-index: 9999;
  top: 0;
  width: 100%;
  height: 50px;
  padding: 2px 0;
  background-color: rgba(0, 0, 0, 0.2);
  .nav-logo {
    margin-left: 10px;
    width: 172px;
    position: absolute;
    top: 50%;
    margin-top: -23px;
  }
  .nav-ghh {
    z-index: 10000;
    position: absolute;
    width: 40px;
    height: 30px;
    top: 0;
    bottom: 0;
    right: 30px;
    margin: auto 0;
    cursor: pointer;
    .ghh-container {
      position: absolute;
      left: 0;
      top: 0;
      width: 44px;
      height: 34px;
      transition: transform 0.3s linear;
      &:hover .ghh-1 {
        top: 4px;
      }
      &:hover .ghh-3 {
        bottom: 4px;
      }
    }
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
        transition: transform 0.3s linear;
      }
      &.ghh-2 {
        top: 0;
        bottom: 0;
      }
      &.ghh-3 {
        transition: transform 0.3s linear;
        bottom: 5px;
      }
    }
  }
}
</style>
