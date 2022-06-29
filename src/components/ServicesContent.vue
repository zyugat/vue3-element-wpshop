<script lang="ts" setup>
import 'element-plus/theme-chalk/display.css'
</script>

<template>
  <section class="services">
    <el-container>
      <el-aside width="235" class="hidden-md-and-down">
        <a href="">
          <img src="@/assets/services/sem.webp" alt="" />
        </a>
      </el-aside>
      <el-main class="content">
        <ul>
          <li class="col-item">
            <h2>私人定制型网站</h2>
            <p>你能想到的功能，我们都能为你创作</p>
          </li>
          <li class="col-item">
            <h2>商城型网站</h2>
            <p>为你提供方便的产品和客户管理系统</p>
          </li>
          <li class="col-item">
            <h2>营销型网站</h2>
            <p>非模板不死板，多功能设计互动营销</p>
          </li>
          <li class="col-item">
            <h2>外贸型网站</h2>
            <p>因地制宜的外贸建站订单源源不断</p>
          </li>
          <li class="col-item">
            <h2>网站内容营销</h2>
            <p>高质量原创博客和文章持续产出、优化</p>
          </li>
          <li class="col-item">
            <h2>Google SEO</h2>
            <p>全球性搜索引擎，高质量优化排位靠前</p>
          </li>
          <li class="col-item">
            <h2>全面SEO优化</h2>
            <p>网站内外部SEO齐上阵,助你省下广告费</p>
          </li>
          <li class="col-item">
            <h2>Facebook推广</h2>
            <p>大型社交平台的图文推广和软文推广</p>
          </li>
          <li class="col-item">
            <div>
              <h2>谷歌搜索SEA</h2>
              <p>全球性搜索引擎付费广告，少花钱高转化</p>
            </div>
          </li>
          <li class="col-item">
            <div>
              <h2>百度搜索SEA</h2>
              <p>国民级搜索引擎付费广告，少花钱高转化</p>
            </div>
          </li>
        </ul>
      </el-main>
    </el-container>
  </section>
</template>

<style scoped lang="scss">
.services {
  display: block;
  max-width: $max_width;
  height: 432px;
  background-color: #fff;
  border: 1px solid #fff;

  .content {
    display: flex;
    color: black;
    padding: 0px;

    li:nth-last-child(1) {
      width: 40%;
      height: 108px;
      padding: 0;

      &::before {
        content: '';
        position: absolute;
        left: calc(50% + 3rem);
        bottom: 0.5rem;
        width: 6rem;
        height: 4rem;
        background: url(@/assets/services/baidu.svg) no-repeat;
      }

      // 内部文字内边距
      div {
        position: absolute;
        top: 15px;
        width: 50%;
        padding: 0px 15px;
      }
    }

    li:nth-last-child(2) {
      width: 40%;
      height: 108px;
      padding: 0;
      // 外部定位
      // padding: 15px 0px;
      // padding-right: 150px;

      &::before {
        background: none;
      }

      // 内部文字内边距
      div {
        position: absolute;
        top: 15px;
        width: 50%;
        padding: 0px 15px;
      }
    }

    // 1.如果想窗口缩小不换行,可以通过设置width+百分比控制.
    // 2.添加border边框后发现他自动换行了，可以添加`box-sizing: border-box;`属性
    .col-item {
      float: left;
      position: relative;
      height: 215px;
      width: 20%;
      padding-top: 2.8rem;
      padding-left: 1rem;
      padding-right: 1rem;
      border: 1px solid #f1f1f1;

      &::before {
        content: '';
        position: absolute;
        left: calc(50% - 1.5rem);
        bottom: 2rem;
        width: 3rem;
        height: 3rem;
        background: url(@/assets/services/custom.svg) no-repeat;
      }

      h2 {
        text-align: center;
        font-size: 1.1rem;
      }
      p {
        text-align: center;
        font-size: 0.9rem;
        color: rgba(91, 95, 102, 1);
      }
    }
  }
}
</style>
