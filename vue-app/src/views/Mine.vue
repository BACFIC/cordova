<template>
  <div id="fff">
    <mt-header fixed :title="title" >
      <mt-button icon="more" slot="right"></mt-button>
    </mt-header>
    <div style="width:100%;height:100px;background-color:lightblue;display:flex;flex-direction:column;align-items:center;justify-content:center;">
      <img class="touxiang" src="../assets/logo.png" style="display:flex;" />
      <div style="display:flex;width:50px;height:30px;font-size:12px;color:white">用户名</div>
    </div>
    <div style="height:20px"></div>
    <mt-cell isLink title="用户信息"></mt-cell>
    <mt-cell isLink title="当前版本" label="2.3.2"></mt-cell>
    <div style="height:20px"></div>
    <mt-cell isLink title="在线帮助"></mt-cell>
    <div style="height:20px"></div>
    <mt-cell isLink title="意见反馈"></mt-cell>
    <mt-cell isLink title="关于"></mt-cell>
    <mt-cell isLink title="清除缓存"></mt-cell>
    <div style="height:20px"></div>
    <mt-button type="primary" size="large">退出账号</mt-button>
  </div>
</template>
<script>
export default {
  name: '',
  props: ['title'],
  data () {
    return {

    }
  }
}
</script>
<style scoped>
#fff {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  padding-top: 40px;
  /*background-color: gray;*/
}
.touxiang{
    width:50px;height:50px;background-color:yellow;
　　border-radius: 50px 50px 50px 50px; /* 所有角都使用半径为5px的圆角，此属性为CSS3标准属性 */
　　-moz-border-radius:  50px 50px 50px 50px; /* Mozilla浏览器的私有属性 */
　　-webkit-border-radius:  50px 50px 50px 50px; /* Webkit浏览器的私有属性 */
}
</style>
