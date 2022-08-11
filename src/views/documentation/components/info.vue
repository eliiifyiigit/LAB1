<template>
  <div>
    <el-row
      justify="space-between"
      :gutter="20"
      style="padding-top: 20px;"
    >
      <el-col
        :md="{'offset':0, 'span':24}"
        :lg="{'offset':0, 'span':24}"
      >
        <span style="font-size: 12px"><strong>CORPORATE</strong></span><br>
        <el-link style="font-size: 10px" :underline="false">About us</el-link><br>
        <el-link style="font-size: 10px" :underline="false">Press</el-link><br>
        <el-link style="font-size: 10px" :underline="false">Human resources</el-link><br>
        <el-link style="font-size: 10px" :underline="false">News from us</el-link>

      </el-col>

    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Info'
}
</script>

<style scoped>

</style>
