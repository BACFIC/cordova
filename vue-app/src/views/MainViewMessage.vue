<template>
  <div>
    <mt-header fixed :title="title" >
      <mt-button icon="more" slot="right"></mt-button>
      <text slot="name">不知道什么Info</text>
    </mt-header>
    <mt-cell style="text-align:left;" v-for="item in cellItems" :key= "item.index" :title="item.title" is-link>
      <img slot="icon" :src="item.icon" width="24" height="24">
    </mt-cell>
  </div>
</template>
<script>
import imgDepartment from '@/assets/department.png'
import imgAddPerson from '@/assets/add_person.png'
import imgAddProject from '@/assets/add_project.png'
export default {
  name: 'home',
  props: ['title'],
  data () {
    return {
      cellItems: [
        {
          index: 1,
          icon: imgDepartment,
          title: '组织管理'
        },
        {
          index: 2,
          icon: imgAddPerson,
          title: '添加员工'
        },
        {
          index: 3,
          icon: imgAddProject,
          title: '添加项目'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
