<template>
<div>
  <mt-header fixed :title="title">
    <mt-button icon="more" slot="right"></mt-button>
    <text slot="name">不知道什么Info</text>
  </mt-header>
  <mt-navbar v-model="selected">
    <mt-tab-item id="1">未完成</mt-tab-item>
    <mt-tab-item id="2">已完成</mt-tab-item>
  </mt-navbar>

  <!-- tab-container -->
  <mt-tab-container :value="active">
    <mt-tab-container-item id="1">
      <mt-cell v-for="n in 10" :title="'内容 ' + n" />
    </mt-tab-container-item>
    <mt-tab-container-item id="2">
      <mt-cell v-for="n in 4" :title="'测试 ' + n" />
    </mt-tab-container-item>
  </mt-tab-container>
</div>
</template>

<script>
export default {
  name: 'app',
  props: ['title'],
  data () {
    return {
      selected: '1'
    }
  },
  computed: {
    active () {
      return this.selected
    }
  }
}
</script>

<style>
</style>
