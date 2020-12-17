<template>
  <div id="page-container">
    <nav-header @changeHeight="changeHeight" />
    <transition name="append">
      <ghh-click-nav v-show="isShow" :isShow="isShow" />
    </transition>
    <div id="page-toggle">
      <page-1 />
      <page-2 />
      <page-3 />
      <page-4 />
      <page-5 />
      <page-6 />
      <page-7 />
      <page-8 />
    </div>
  </div>
</template>

<script>
import NavHeader from "./components/HomePage/NavHeader.vue";
import GhhClickNav from "./components/HomePage/GhhClickNav.vue";
import Page1 from "./components/HomePage/Page1.vue";
import Page2 from "./components/HomePage/Page2.vue";
import Page3 from "./components/HomePage/Page3.vue";
import Page4 from "./components/HomePage/Page4.vue";
import Page5 from "./components/HomePage/Page5.vue";
import Page6 from "./components/HomePage/Page6.vue";
import Page7 from "./components/HomePage/Page7.vue";
import Page8 from "./components/HomePage/Page8.vue";

export default {
  data() {
    return {
      isShow: false
    };
  },
  components: {
    NavHeader,
    GhhClickNav,
    Page1,
    Page2,
    Page3,
    Page4,
    Page5,
    Page6,
    Page7,
    Page8
  },
  mounted() {},
  methods: {
    changeHeight(isShow) {
      this.isShow = isShow;
    }
  }
};
</script>

<style lang="less" scoped>
// 公共样式
@import url("./less/index.less");

#page-container {
  height: 100%;
  overflow: hidden;
  #page-toggle {
    height: 100%;
    .page {
      height: 100%;
    }
  }
}
// GhhClickNav组件页面动画
.append-enter-active,
.append-leave-active {
  transition: height 0.4s ease-in-out;
}
.append-enter,
.append-leave-to {
  height: 0% !important;
}
</style>
