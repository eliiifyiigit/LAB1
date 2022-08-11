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
        <span style="font-size: 12px"><strong>LEGAL</strong></span><br>
        <el-link style="font-size: 10px" :underline="false">Terms of Use</el-link><br>
        <el-link style="font-size: 10px" :underline="false">Privacy Policy</el-link><br>
        <el-link style="font-size: 10px" :underline="false">Membership Agreement</el-link><br>
        <el-link style="font-size: 10px" :underline="false">Distance Selling Contract</el-link>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Info3'
}
</script>

<style scoped>

</style>
