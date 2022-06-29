<script lang="ts" setup>
import 'element-plus/theme-chalk/display.css'
</script>

<template>
  <footer>
    <div class="content">
      <div class="header">
        <img src="@/assets/logo.png" alt="" />
        <p>专注于定制型网站建设和海外网站建设</p>
        <span></span>
      </div>
      <div class="inner"></div>
      <div class="bottom"></div>
    </div>
  </footer>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
footer {
  display: block;
  width: 100%;
  height: 530px;
  margin: 0;
  padding: 0;
  color: #fff;
  background: #191f2b url(@/assets/background_footer.svg) no-repeat center;
  background-size: cover;

  .content {
    max-width: $max_width;
    margin: 0 auto;
    border: 1px solid red;

    .header {
      position: relative;
      img {
        position: absolute;
        display: inline-block;
      }
      p {
        display: inline-block;
        margin: 0 auto;
      }
      // &:after {
      //   content: '';
      //   display: block;
      //   height: 0;
      //   clear: both;
      //   /* 不可见 */
      //   visibility: hidden;
      // }
    }
  }
}
</style>
