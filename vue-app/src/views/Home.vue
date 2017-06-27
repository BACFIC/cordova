<template>
  <div id="home">
    <mt-tab-container :value="active">
      <mt-tab-container-item id='1'>
        <message-view title="标签1"></message-view>
      </mt-tab-container-item>
      <mt-tab-container-item id='2'>
        <project-view title="标签2"></project-view>
      </mt-tab-container-item>
      <mt-tab-container-item id='3'>
        <Mine title="我的信息"></Mine>
      </mt-tab-container-item>
    </mt-tab-container>
    <mt-tabbar v-model="selected" :fixed="true">
      <mt-tab-item v-for="item in tabItems" :key="item.index" :id="item.index">
        <img slot="icon" :src="item.src">
        {{item.text}}
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>

<script>
import logo from '@/assets/logo.png'
export default {
  name: 'home',
  data () {
    return {
      tabItems: [
        {
          index: '1',
          src: logo,
          text: '消息'
        },
        {
          index: '2',
          src: logo,
          text: '项目'
        },
        {
          index: '3',
          src: logo,
          text: '我的'
        }
      ],
      selected: '1'
    }
  },
  computed: {
    active: function () {
      return this.selected
    }
  },
  components: {
    'message-view': require('./MainViewMessage.vue'),
    'project-view': require('./MainViewProject.vue'),
    'Mine': require('./Mine.vue')
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #home{
    padding-bottom: 55px
  }
</style>
