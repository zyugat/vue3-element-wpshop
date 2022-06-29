<script lang="ts" setup>
import { reactive } from 'vue'
import 'element-plus/theme-chalk/display.css'

const navList = reactive([
  {
    name: '主页',
    class: 'nav-item hidden-xs-only',
  },
  {
    name: '关于我们',
    class: 'nav-item hidden-xs-only',
  },
  {
    name: '价格',
    class: 'nav-item hidden-md-and-down',
  },
  {
    name: '建站流程',
    class: 'nav-item hidden-md-and-down',
  },
  {
    name: '外贸建站',
    class: 'nav-item hidden-md-and-down',
  },
  {
    name: '网站建设',
    class: 'nav-item hidden-xs-only',
  },
  {
    name: '电商学堂',
    class: 'nav-item hidden-xs-only',
  },
])
</script>

<template>
  <header>
    <div class="header">
      <div class="header-logo">
        <a href="">
          <img src="@/assets/logo.png" />
        </a>
      </div>
      <nav>
        <ul>
          <li v-for="item in navList" :key="item.name" :class="item.class">
            {{ item.name }}
          </li>
          <li class="nav-item hidden-xs-only phone">020-12345678</li>
          <li class="nav-item hidden-xs-only">
            <button>联系我们</button>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
header {
  position: sticky;
  top: 0;
  z-index: 100;
  width: 100%;
  height: 60px;
  color: #fff;
  background-color: #191f2b;
  line-height: 60px;

  // 重要！！这里由于使用了定位,如果想居中绝对不可用使用margin，会导致其他布局出错!!
  .header {
    position: relative;
    max-width: $max_width;
    height: 60px;
    left: calc(50% - $max_width/2);
    // margin: 0 auto;

    .header-logo {
      float: left;
      line-height: 90px;

      img {
        width: 40px;
        height: 40px;
      }
    }

    // 如果在nav中用的是右浮动 那么当窗口缩小的时候，会导致整行下移，而不是下移右边多出的元素<联系我们>
    nav {
      position: absolute;
      right: 0;
      .nav-item {
        float: left;
        margin-left: 2rem;

        button {
          position: relative;
          top: -2px;
          width: 95px;
          height: 33px;
          border: 1px solid #fff;
          border-radius: 4px;
          font-weight: 600;
          color: #fff;
          background-color: #191f2b;
        }
      }

      // 微调距离前一个元素距离
      .phone {
        position: relative;
        margin-left: 5rem;
      }
      // 1.position用来定位元素,2.content必须存在,3.w和h设置图片大小
      .phone::before {
        position: absolute;
        top: 1.4rem;
        left: -1.4rem;
        width: 20px;
        height: 20px;
        background: url(@/assets/phone.svg) no-repeat;
        content: '';
      }
    }
  }
}
</style>
