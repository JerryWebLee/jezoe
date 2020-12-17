<template>
  <div class="moblie-nav">
    <transition name="top-down">
      <div class="mob-sub-nav" v-show="isShow">
        <ul>
          <li class="mob1">
            <dl class="bg1">
              <dt></dt>
              <dd>
                <h3><a href="">云搜宝</a></h3>
              </dd>
            </dl>
            <dl class="bg2">
              <dt></dt>
              <dd>
                <h3><a href="">整合营销</a></h3>
              </dd>
            </dl>
            <dl class="bg3">
              <dt></dt>
              <dd>
                <h3><a href="">云客网</a></h3>
              </dd>
            </dl>
            <dl class="bg4">
              <dt></dt>
              <dd>
                <h3><a href="">社群化营销</a></h3>
              </dd>
            </dl>
          </li>
          <li class="mob2">
            <dl class="bg1">
              <dt></dt>
              <dd>
                <h3><a href="/">首页</a></h3>
              </dd>
            </dl>
            <dl class="bg2">
              <dt></dt>
              <dd>
                <h3><a href="">关于</a></h3>
              </dd>
            </dl>
            <dl class="bg3">
              <dt></dt>
              <dd>
                <h3><a href="">资讯</a></h3>
              </dd>
            </dl>
            <dl class="bg4">
              <dt></dt>
              <dd>
                <h3><a href="">招聘</a></h3>
              </dd>
            </dl>
            <dl class="bg5">
              <dt></dt>
              <dd>
                <h3><a href="">联络</a></h3>
              </dd>
            </dl>
          </li>
          <li class="mob3">
            <p class="img1"><span>057187357437</span></p>
            <p class="img2">
              <a
                href="http://wpa.qq.com/msgrd?v=3&uin=2851282535&site=qq&menu=yes"
                target="_blank"
                >在线咨询</a
              >
            </p>
            <p class="img3">
              <a href="">全国分公司联系方式</a>
            </p>
          </li>
        </ul>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  props: {
    isShow: Boolean
  }
};
</script>

<style lang="less" scoped>
// 响应式
@media screen and (max-width: 1150px) and (min-width: 640px) {
  div.moblie-nav {
    width: 640px;
    height: 100%;
  }
}
@media screen and (min-width: 1151px) {
  .moblie-nav {
    display: none;
  }
}
@media screen and (max-width: 1150px) {
  .moblie-nav .mob-sub-nav {
    width: 600px;
  }
  .moblie-nav .mob-sub-nav ul li {
    width: 33.33333%;
  }
}
@media screen and (max-width: 760px) {
  .moblie-nav .mob-sub-nav {
    width: 320px;
  }
  .moblie-nav .mob-sub-nav ul li.mob3 {
    display: none;
  }
  .moblie-nav .mob-sub-nav ul li {
    width: 50%;
  }
}
// 过渡
.top-down-enter-active,
.top-down-leave-active {
  transition: top 0.4s ease-in-out;
}
.top-down-enter,
.top-down-leave-to {
  top: -300px !important;
}

.moblie-nav {
  position: absolute;
  z-index: 9990;
  height: 100%;
  width: 100%;
  overflow: hidden;
  background-color: rgba(56, 59, 67, 0.9);
  .mob-sub-nav {
    height: 352px;
    position: absolute;
    left: 0;
    top: 175px;
    right: 0;
    bottom: auto;
    margin: 0 auto;
    ul {
      height: 270px;
      padding: 0;
      display: flex;
      justify-content: space-between;
      li {
        dl {
          height: 24px;
          margin-bottom: 30px;
          dt {
            width: 24px;
            height: 24px;
            float: left;
          }
          dd {
            height: 24px;
            margin-left: 24px;
            padding-left: 15px;
            h3 {
              display: flex;
              align-items: center;
              height: 24px;
              line-height: 24px;
              margin: 0;
              a {
                font-size: 16px;
                color: #d1d1d2;
                transition: color 0.3s linear;
                &:hover {
                  color: #fff;
                }
              }
            }
          }
        }
        &:nth-of-type(1) {
          .bg1 dt {
            background: url("../../assets/images/r1.png") no-repeat center;
          }
          .bg2 dt {
            background: url("../../assets/images/r4.png") no-repeat center;
          }
          .bg3 dt {
            background: url("../../assets/images/r5.png") no-repeat center;
          }
          .bg4 dt {
            background: url("../../assets/images/r8.png") no-repeat center;
          }
        }
        &:nth-of-type(2) {
          .bg1 dt {
            background: url("../../assets/images/r2.png") no-repeat center;
          }
          .bg2 dt {
            background: url("../../assets/images/r3.png") no-repeat center;
          }
          .bg3 dt {
            background: url("../../assets/images/r6.png") no-repeat center;
          }
          .bg4 dt {
            background: url("../../assets/images/r7.png") no-repeat center;
          }
          .bg5 dt {
            background: url("../../assets/images/r9.png") no-repeat center;
          }
        }
        p {
          height: 40px;
          line-height: 40px;
          margin-bottom: 35px;
          a,
          span {
            color: #fff;
            margin-left: 60px;
          }
          span {
            color: #fff;
            margin-left: 60px;
            font-size: 18px;
          }
          a {
            display: inline-block;
            text-decoration: none;
            font-size: 12px;
            border: 1px solid #fff;
            border-radius: 20px;
          }
          &.img1 {
            background: url("../../assets/images/img1.png") no-repeat left
              center;
          }
          &.img2 {
            background: url("../../assets/images/img3.png") no-repeat left
              center;
            a {
              width: 100px;
              height: 24px;
              line-height: 24px;
              text-align: center;
              vertical-align: middle;
            }
          }
          &.img3 {
            background: url("../../assets/images/img2.png") no-repeat left
              center;
            a {
              width: 140px;
              height: 24px;
              line-height: 24px;
              text-align: center;
              vertical-align: middle;
            }
          }
        }
      }
    }
  }
}
</style>
