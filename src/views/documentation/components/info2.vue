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
        <span style="font-size: 12px"><strong>SHOPPING</strong></span><br>
        <el-link style="font-size: 10px" :underline="false">Order and Payment</el-link><br>
        <el-link style="font-size: 10px" :underline="false">Cancellation and Refund</el-link><br>
        <el-link style="font-size: 10px" :underline="false">Delivery Conditions</el-link><br>
        <el-link style="font-size: 10px" :underline="false">Secure Shopping</el-link>
      </el-col>

    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Info2'
}
</script>

<style scoped>

</style>
