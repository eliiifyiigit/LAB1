<template>
  <div class="navbar" style="background-color: #505357">

    <el-row
      justify="space-between"
      :gutter="20"
      style="padding-top: 5px"
    >
      <el-col
        :md="{'offset':3, 'span':3}"
        :lg="{'offset':3, 'span':3}"
        :sm="4"
      >

        <el-link icon="el-icon-goods" href="https://element.eleme.io" target="_blank" style="color: white">Stores</el-link>
        <el-link icon="el-icon-s-management" href="https://element.eleme.io" target="_blank" style="color: white; padding-left: 10px">Catalog</el-link>

      </el-col>
      <el-col
        :md="{'offset':3, 'span':7}"
        :lg="{'offset':3, 'span':7}"
        :sm="4"
      >

        <span style="color: #8493A8;"> Watsons Beauty and Personal Care Awards Nominees!</span>

      </el-col>
      <el-col
        :md="{'offset':2, 'span':5}"
        :lg="{'offset':2, 'span':5}"
        :sm="4"
      >
        <span style="color: white;">Call us:(+90) 850 123 45 67 <i class="el-icon-mobile-phone" /></span>

      </el-col>
    </el-row>

  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  components: {
  },
  computed: {
    ...mapGetters([
      'avatar',
      'device'
    ])
  },
  methods: {
    async logout() {
      await this.$store.dispatch('user/logout')
      this.$router.push(`/login?redirect=${this.$route.fullPath}`)
    }
  }
}
</script>

<style lang="scss" scoped>
.navbar {
  height: 30px;
  overflow: hidden;
  position: relative;
  background: #fff;
  box-shadow: 0 1px 4px rgba(0,21,41,.08);

}
</style>
