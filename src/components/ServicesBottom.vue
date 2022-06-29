<script lang="ts" setup>
import 'element-plus/theme-chalk/display.css'
</script>

<template>
  <section class="services-bottom">
    <ul class="content">
      <li>
        <h3>搜索引擎适配</h3>
        <p>定制网站的每一细节皆可量身设计，你的想象皆可定制</p>
      </li>
      <li>
        <h3>先设计后编程</h3>
        <p>品牌建站以数据分析结果为依据，设计稿改到满意为止</p>
      </li>
      <li>
        <h3>推广学堂</h3>
        <p>海外优化师分享15年海外推广经验，推广细节全掌握</p>
      </li>
    </ul>
  </section>
</template>

<style scoped lang="scss">
.services-bottom {
  max-width: $max_width;
  height: 171px;
  box-shadow: 0 0 15px rgb(0 0 0 / 10%);
  margin: 0 auto;
  padding: 3rem;

  .content {
    display: flex;

    li {
      flex: 1;
      position: relative;
      height: 75px;
      padding: 0 3rem 0 4rem;

      &:nth-child(n)::before {
        content: '';
        position: absolute;
        bottom: calc(50% - 26px);
        left: 0;
        width: 52px;
        height: 52px;
        background: url(@/assets/services/time.svg) no-repeat;
      }

      p {
        font-size: 0.9rem;
        color: rgba(91, 95, 102, 1);
      }
    }
  }
}
</style>
