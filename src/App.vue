<template>
  <div id="page-container">
    <nav-header />
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
import Page1 from "./components/HomePage/Page1.vue";
import Page2 from "./components/HomePage/Page2.vue";
import Page3 from "./components/HomePage/Page3.vue";
import Page4 from "./components/HomePage/Page4.vue";
import Page5 from "./components/HomePage/Page5.vue";
import Page6 from "./components/HomePage/Page6.vue";
import Page7 from "./components/HomePage/Page7.vue";
import Page8 from "./components/HomePage/Page8.vue";

export default {
  components: {
    NavHeader,
    Page1,
    Page2,
    Page3,
    Page4,
    Page5,
    Page6,
    Page7,
    Page8
  }
};
</script>

<style lang="less">
// 公共样式
@import url("./less/index.less");
#page-container {
  height: 100%;
  overflow: hidden;
}
</style>
