<script lang="ts" setup></script>

<template>
  <section class="hero">
    <div class="content">
      <el-row>
        <el-col :span="14" class="left">
          <h1>
            <span>外贸建站服务</span>
            WordPress设计与开发
          </h1>
          <p>
            专注于WordPress主题设计与插件开发。云集海内外工程师为企业客户提供谷歌推广服务，到目前已有99年WordPress外贸建站经验。
          </p>
          <a href="">了解更多</a>
        </el-col>
        <el-col :span="8" class="right">
          <img src="@/assets/hero_main.svg" alt="" />
        </el-col>
      </el-row>
    </div>
  </section>
</template>

<style scoped lang="scss">
// 1.no-repeat+center不重复背景
// 2. background-size: cover; 拉伸图片
.hero {
  display: block;
  width: 100%;
  height: 36rem;
  margin: 0;
  padding: 0;
  color: #fff;
  background: #191f2b url(@/assets/background_header.svg) no-repeat center;
  background-size: cover;

  // 这里居中需要-40px
  .content {
    position: relative;
    max-width: $max_width;
    height: 36rem;
    left: calc(50% - $max_width/2 - 40px);
    padding: 0;
    margin: 0;

    .left {
      h1 {
        display: block;
        font-size: 2.5rem;
        font-weight: 700;
        margin-top: 5rem;

        span {
          display: block;
          font-size: 1.6rem;
          font-weight: 100;
        }
      }
      // 这里设置文字长度，让文字和图片有间隔
      p {
        max-width: 80%;
      }

      a {
        position: relative;
        display: inline-block;
        line-height: 2.7rem;

        padding: 0rem 3rem 0rem 2rem;
        margin-top: 2rem;
        border: 1px solid #35bae6;
        border: none;
        border-radius: 4px;

        color: #fff;
        background: #35bae6;

        font-weight: 400;
        font-size: 1rem;
        letter-spacing: 1.5px;

        &::before {
          content: '';
          position: absolute;
          width: 1rem;
          height: 1rem;
          right: 1.1rem;
          top: 0.9rem;
          background: url(@/assets/bt_arrow.svg) no-repeat;
        }
      }
    }
    .right {
      position: absolute;
      right: 80px;
      img {
        width: 430px;
        height: 430px;
        content: '';
      }
    }
  }
}
</style>
