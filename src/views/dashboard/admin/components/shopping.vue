<template>
  <div>
    <el-row
      justify="space-between"
      :gutter="20"
      style="padding-top: 20px; padding-bottom: 20px; "
    >
      <el-col
        :md="{'offset':0, 'span':24}"
        :lg="{'offset':0, 'span':24}"
      >
        <el-card style="padding-bottom: 20px;">
          <el-card>
            <el-col
              :md="{'offset':0, 'span':12}"
              :lg="{'offset':0, 'span':12}"
            >
              <img
                style="height: 100px"
                src="https://www.watsons.com.tr/medias/sys_master/prd-images/hac/hb7/8973480198174/prd-front-BP_1295728_195x195/prd-front-BP-1295728-195x195.png"
                class="image"
              >
            </el-col>
            <el-col
              :md="{'offset':0, 'span':12}"
              :lg="{'offset':0, 'span':12}"
            >
              <span style="font-size: 10px">Herbal Science Boom Butter Hair Care Oil 190 ml</span>
              <el-input-number v-model="num1" style="width: 70%" size="mini" :min="1" :max="10" @change="handleChange" />
              <span style="font-weight: bold;">44,95TL</span>
            </el-col>
          </el-card>
          <el-card>
            <el-col
              :md="{'offset':0, 'span':12}"
              :lg="{'offset':0, 'span':12}"
            >
              <img
                style="height: 100px"
                src="https://www.watsons.com.tr/medias/sys_master/prd-images/h26/hfd/8887254810654/prd-front-BP_168000_195x195/prd-front-BP-168000-195x195.jpeg"
                class="image"
              >
            </el-col>
            <el-col
              :md="{'offset':0, 'span':12}"
              :lg="{'offset':0, 'span':12}"
            >
              <span style="font-size: 10px">Ashley Joy Strengthening Shampoo 400ml</span>
              <el-input-number v-model="num2" style="width: 70%" size="mini" :min="1" :max="10" @change="handleChange" />
              <span style="font-weight: bold;">29,45TL</span>

            </el-col>
          </el-card>
          <el-col
            :md="{'offset':0, 'span':24}"
            :lg="{'offset':0, 'span':24}"
            style="padding-top: 20px"
          >
            <el-input v-model="code" placeholder="Discount Code" @keyup.enter.native="codeFunc" />
          </el-col>
          <el-col
            :md="{'offset':0, 'span':12}"
            :lg="{'offset':0, 'span':12}"
            style="padding-top: 20px"
          >
            <span>
              Subtotal
            </span>
          </el-col>
          <el-col
            :md="{'offset':0, 'span':12}"
            :lg="{'offset':0, 'span':12}"
            style="padding-top: 20px"
          >
            <span style="float: right">
              <strong>74,40 TL</strong>
            </span>
          </el-col>
          <el-col
            :md="{'offset':0, 'span':12}"
            :lg="{'offset':0, 'span':12}"
            style="padding-top: 20px"
          >
            <span>
              Shipping
            </span>
          </el-col>
          <el-col
            :md="{'offset':0, 'span':12}"
            :lg="{'offset':0, 'span':12}"
            style="padding-top: 20px"
          >
            <span style="float: right">
              <strong>10,50 TL</strong>
            </span>

          </el-col>
          <el-col
            :md="{'offset':0, 'span':24}"
            :lg="{'offset':0, 'span':24}"
            style="padding-top: 10px"
          >
            <el-divider />
          </el-col>
          <el-col
            :md="{'offset':0, 'span':12}"
            :lg="{'offset':0, 'span':12}"
            style="padding-top: 20px"
          >
            <span>
              <strong>Total</strong>
            </span>
          </el-col>
          <el-col
            :md="{'offset':0, 'span':12}"
            :lg="{'offset':0, 'span':12}"
            style="padding-top: 20px"
          >
            <span style="float: right">
              <strong>84,90 TL</strong>
            </span>

          </el-col>
        </el-card>

      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Shopping',
  data() {
    return {
      num1: 1,
      num2: 1,
      code: ''
    }
  },
  methods: {
    handleChange(value) {
      console.log(value)
    },
    codeFunc() {
      this.$message({
        message: this.code + ' discount code added.',
        type: 'success'
      })
    }
  }
}
</script>

<style scoped>

</style>
