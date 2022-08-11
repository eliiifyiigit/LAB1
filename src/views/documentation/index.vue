<template>
  <div class="dashboard-editor-container">
    <div>
      <el-row
        justify="space-between"
        :gutter="20"
      >
        <el-col
          :md="{'offset':3, 'span':2}"
          :lg="{'offset':3, 'span':2}"
          :sm="4"
        >
          <el-image
            src="https://www.watsons.com.tr/medias/sys_master/images/h85/h39/8920546869278/logo-watsons/logo-watsons.png"
            fit="scale-down"
          />
        </el-col>
        <el-col
          :md="{'offset':0, 'span':9}"
          :lg="{'offset':0, 'span':9}"
          :sm="4"
        >
          <el-input
            v-model="input2"
            placeholder="Write the product or category you are looking for"
            prefix-icon="el-icon-search"
            @keyup.enter.native="search"
          >
            >
          </el-input>
        </el-col>
        <el-col
          :md="{'offset':0, 'span':3}"
          :lg="{'offset':0, 'span':3}"
          :sm="4"
          style="padding-top: 10px"
        >
          <span> Hello, <strong>Clara Clara</strong></span>
        </el-col>
        <el-col
          :md="{'offset':0, 'span':1}"
          :lg="{'offset':0, 'span':1}"
          :sm="4"
          style="padding-top: 5px"
        >
          <el-avatar src="https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png" size="small" />
        </el-col>
        <el-col
          :md="{'offset':0, 'span':1}"
          :lg="{'offset':0, 'span':1}"
          :sm="4"
          style="padding-top: 10px"
        >
          <i class="el-icon-arrow-down" />
        </el-col>
        <el-col
          :md="{'offset':0, 'span':1}"
          :lg="{'offset':0, 'span':1}"
          :sm="4"
          style="padding-top: 10px"
        >
          <el-divider direction="vertical" />
        </el-col>
        <el-col
          :md="{'offset':0, 'span':1}"
          :lg="{'offset':0, 'span':1}"
          :sm="4"
        >
          <el-badge class="item" :value="12">
            <el-button style="background-color: #f0f2f5; border-color: #f0f2f5" class="share-button" icon="el-icon-shopping-bag-1" size="medium" type="primary" />
          </el-badge>
        </el-col>
      </el-row>
    </div>
    <div>
      <el-row
        justify="space-between"
        :gutter="20"
      >
        <el-col
          :md="{'offset':4, 'span':16}"
          :lg="{'offset':4, 'span':16}"
          :sm="21"
        >
          <el-tabs v-model="activeName" @tab-click="handleClick">
            <el-tab-pane label="CAMPAIGNS" name="first" disabled="" />
            <el-tab-pane label="PERSONAL CARE" name="second" disabled="">PERSONAL CARE</el-tab-pane>
            <el-tab-pane label="SKIN CARE" name="third" disabled="">SKIN CARE</el-tab-pane>
            <el-tab-pane label="MAKE-UP" name="fourth" disabled="">MAKE-UP</el-tab-pane>
            <el-tab-pane label="MOTHER & BABY" name="fifth" disabled="">MOTHER & BABY</el-tab-pane>
            <el-tab-pane label="MEN CARE" name="sixth" disabled="">MEN CARE</el-tab-pane>
            <el-tab-pane label="HEALTY LIFE" name="seventh" disabled="">HEALTY LIFE</el-tab-pane>
            <el-tab-pane label="BRANDS" name="eighth" disabled="">BRANDS</el-tab-pane>
          </el-tabs>
        </el-col>
      </el-row>

    </div>
    <div>
      <el-row
        justify="space-between"
        :gutter="20"
        style="padding-top: 30px; background-color: rgba(236, 236, 236, 0.3);"
      >
        <el-col

          :md="{'offset':3, 'span':24}"
          :lg="{'offset':3, 'span':24}"
        >
          <el-breadcrumb separator-class="el-icon-arrow-right">
            <el-breadcrumb-item style="font-size: 10px" :to="{ path: '/dashboard' }">Homepage</el-breadcrumb-item>
            <el-breadcrumb-item style="font-size: 10px">Shopping Chart</el-breadcrumb-item>
            <el-breadcrumb-item style="font-size: 10px">Checkout</el-breadcrumb-item>
          </el-breadcrumb>
        </el-col>
        <el-col
          style="padding-top: 20px; padding-bottom: 20px"
          :md="{'offset':3, 'span':21}"
          :lg="{'offset':3, 'span':21}"
        >
          <span style="font-weight: bolder; font-size: 40px"> Checkout</span>
        </el-col>
      </el-row>
    </div>
    <div>
      <el-row
        justify="space-between"
        :gutter="20"
        style="padding-top: 20px; padding-bottom: 20px"
      >
        <el-col
          :md="{'offset':3, 'span':12}"
          :lg="{'offset':3, 'span':12}"
        >
          <span><i class="el-icon-shopping-bag-1" /><strong>Shipping Details</strong></span>
        </el-col>
        <el-col
          :md="{'offset':0, 'span':6}"
          :lg="{'offset':0, 'span':6}"
        >
          <span><strong>Shopping chart summary</strong></span>
        </el-col>
      </el-row>
    </div>
    <div>
      <el-row
        justify="space-between"
        :gutter="20"
        style="padding-top: 5px; padding-bottom: 20px"
      >
        <el-col
          :md="{'offset':3, 'span':12}"
          :lg="{'offset':3, 'span':12}"
        >
          <shipping />
        </el-col>
        <el-col
          :md="{'offset':0, 'span':7}"
          :lg="{'offset':0, 'span':7}"
        >
          <shopping />
        </el-col>

      </el-row>

    </div>
    <el-divider />
    <div>
      <el-row
        justify="space-between"
        :gutter="20"
        style="padding-top: 20px; padding-bottom: 20px"
      >
        <el-col
          :md="{'offset':3, 'span':4}"
          :lg="{'offset':3, 'span':4}"
        >
          <info />
        </el-col>
        <el-col
          :md="{'offset':0, 'span':4}"
          :lg="{'offset':0, 'span':4}"
        >
          <info2 />
        </el-col>
        <el-col
          :md="{'offset':0, 'span':4}"
          :lg="{'offset':0, 'span':4}"
        >
          <info3 />
        </el-col>
        <el-col
          :md="{'offset':0, 'span':4}"
          :lg="{'offset':0, 'span':4}"
        >
          <info4 />
        </el-col>
        <el-col
          :md="{'offset':0, 'span':4}"
          :lg="{'offset':0, 'span':4}"
        >
          <info5 />
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>

import Shipping from '@/views/dashboard/admin/components/shipping'
import Shopping from '@/views/dashboard/admin/components/shopping'
import Info from '@/views/documentation/components/info'
import Info2 from '@/views/documentation/components/info2'
import Info3 from '@/views/documentation/components/info3'
import Info4 from '@/views/documentation/components/info4'
import Info5 from '@/views/documentation/components/info5'
export default {
  name: 'Documentation',
  components: { Info, Info2, Info3, Info4, Info5, Shopping, Shipping },
  data() {
    return {
      name: '',
      lastName: '',
      email: '',
      phone: '',
      input: '',
      input2: '',
      activeName: '',
      fits: 'scale-down',
      url: 'https://www.watsons.com.tr/medias/sys_master/root/h66/hce/8992832847902/1300x500/1300x500.png'
    }
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event)
    },
    search() {
      fetch('https://dummyjson.com/products/search?q=' + this.input2)
        .then(res => res.json())
        .then(this.$message({
          message: this.input2 + ' searched.',
          type: 'success'
        }))
      this.input2 = ''
    }
  }
}
</script>

<style lang="scss" scoped>
.documentation-container {
  margin: 50px;
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;

  .document-btn {
    flex-shrink: 0;
    display: block;
    cursor: pointer;
    background: black;
    color: white;
    height: 60px;
    padding: 0 16px;
    margin: 16px;
    line-height: 60px;
    font-size: 20px;
    text-align: center;
  }
}

.dashboard-editor-container {
  padding: 32px;
  background-color: white;
  position: relative;

  .github-corner {
    position: absolute;
    top: 0px;
    border: 0;
    right: 0;
  }

  .chart-wrapper {
    background: #fff;
    padding: 16px 16px 0;
    margin-bottom: 32px;
  }
}

.el-button--medium {
  color: black;
}

.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #f2f0ff;
}

.el-carousel__item:nth-child(2n+1) {
  background-color: #f2f0ff;
}

@media (max-width: 1024px) {
  .chart-wrapper {
    padding: 8px;
  }
}

.el-divider__text {
  color: #0099A8;
  background-color: white;
  font-weight: bolder;
}

.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
}

.image {
  width: 100%;
  display: block;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}

.clearfix:after {
  clear: both
}
</style>
