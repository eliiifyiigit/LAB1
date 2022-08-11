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
        <span style="font-size: 12px"><strong>HELP CENTER</strong></span><br>
        <el-link style="font-size: 10px" :underline="false">FAQ</el-link><br>
        <el-link style="font-size: 10px" :underline="false">Contact Center</el-link>

      </el-col>

    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Info4'
}
</script>

<style scoped>

</style>
