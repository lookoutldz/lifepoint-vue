<template>
  <el-container>
    <el-header>{{title}}</el-header>
    <el-main>{{title}}</el-main>
    <el-footer>{{title}}</el-footer>
  </el-container>
</template>

<script>
export default {
  name: 'Life',
  data () {
    return {
      title: 'Life'
    }
  },
  methods: {
    ok () {
      alert('ok')
    }
  }
}
</script>
<style>
</style>
