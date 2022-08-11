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
          />
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
      <el-col
        :md="{'offset':4, 'span':16}"
        :lg="{'offset':4, 'span':16}"
        :sm="21"
      >
        <el-tabs v-model="activeName" @tab-click="handleClick">
          <el-tab-pane label="CAMPAIGNS" name="first" />
          <el-tab-pane label="PERSONAL CARE" name="second" disabled="">PERSONAL CARE</el-tab-pane>
          <el-tab-pane label="SKIN CARE" name="third" disabled="">SKIN CARE</el-tab-pane>
          <el-tab-pane label="MAKE-UP" name="fourth" disabled="">MAKE-UP</el-tab-pane>
          <el-tab-pane label="MOTHER & BABY" name="fifth" disabled="">MOTHER & BABY</el-tab-pane>
          <el-tab-pane label="MEN CARE" name="sixth" disabled="">MEN CARE</el-tab-pane>
          <el-tab-pane label="HEALTY LIFE" name="seventh" disabled="">HEALTY LIFE</el-tab-pane>
          <el-tab-pane label="BRANDS" name="eighth" disabled="">BRANDS</el-tab-pane>
        </el-tabs>
      </el-col>
    </div>
    <div>
      <el-row
        justify="space-between"
        :gutter="20"
      >
        <el-col
          :md="{'offset':0, 'span':24}"
          :lg="{'offset':0, 'span':24}"
          :sm="24"
        >
          <el-carousel>
            <el-carousel-item style="width: 100%">
              <el-image
                style="width: 1000px;margin-left: 200px"
                :src="url"
                :fit="fits"
              />
            </el-carousel-item>
          </el-carousel>
        </el-col>
      </el-row>
    </div>
    <div style="background-color: white">
      <el-divider>Featured products</el-divider>
    </div>
    <div style="background-color: white; padding-bottom: 40px">
      <el-row>
        <el-col
          :md="{'offset':2, 'span':4}"
          :lg="{'offset':2, 'span':4}"
          :sm="4"
        >
          <el-card>
            <img src="https://www.watsons.com.tr/medias/sys_master/prd-images/hac/hb7/8973480198174/prd-front-BP_1295728_195x195/prd-front-BP-1295728-195x195.png" class="image" @click="basket">
            <div>
              <span><strong>44,95 TL</strong></span>
              <div class="bottom clearfix">
                <time class="time">Herbal Science Boom Butter Hair Care Oil 190 ml</time>
              </div>
            </div>
          </el-card>
        </el-col>
        <el-col
          :md="{'offset':1, 'span':4}"
          :lg="{'offset':1, 'span':4}"
          :sm="4"
        >
          <el-card>
            <img src="https://www.watsons.com.tr/medias/sys_master/prd-images/h31/h2b/8910625734686/prd-front-170364_195x195/prd-front-170364-195x195.png" class="image">
            <div>
              <span><strong>42,25 TL</strong></span>
              <div class="bottom clearfix">
                <time class="time">Diadermine Lift + Serum Booster Vitamin C</time>
              </div>
            </div>
          </el-card>
        </el-col>
        <el-col
          :md="{'offset':1, 'span':4}"
          :lg="{'offset':1, 'span':4}"
          :sm="4"
        >
          <el-card>
            <img src="https://www.watsons.com.tr/medias/sys_master/prd-images/h26/hfd/8887254810654/prd-front-BP_168000_195x195/prd-front-BP-168000-195x195.jpeg" class="image">
            <div>
              <span><strong>29,95 TL</strong></span>
              <div class="bottom clearfix">
                <time class="time">Ashley Joy Strengthening Shampoo 400ml</time>
              </div>
            </div>
          </el-card>
        </el-col>
        <el-col
          :md="{'offset':1, 'span':4}"
          :lg="{'offset':1, 'span':4}"
          :sm="4"
        >
          <el-card>
            <img src="https://www.watsons.com.tr/medias/sys_master/prd-images/h07/h78/8894925307934/prd-front-BP_145841_195x195/prd-front-BP-145841-195x195.jpeg" class="image">
            <div>
              <span><strong>28,95 TL</strong></span>
              <div class="bottom clearfix">
                <time class="time">Herbal Extract Refreshing Shampoo 400ml</time>
              </div>
            </div>
          </el-card>
        </el-col>
      </el-row>
    </div>
    <div style="background-color: #f2f0ff; padding-top: 30px; padding-bottom: 30px">
      <el-row
        justify="space-between"
        :gutter="20"
      >
        <el-col
          :md="{'offset':2, 'span':10}"
          :lg="{'offset':2, 'span':10}"
          :sm="12"
        >
          <span>
            <strong>Sign up to our newsletter</strong><br><br>
            Be the first to hear about the latest offers.
          </span>
        </el-col>
        <el-col
          :md="{'offset':0, 'span':7}"
          :lg="{'offset':0, 'span':7}"
          :sm="12"
        >
          <el-input v-model="input" placeholder="Your email address" @keyup.enter.native="subscribe" />
        </el-col>
        <el-col
          :md="{'offset':0, 'span':3}"
          :lg="{'offset':0, 'span':3}"
          :sm="12"
        >
          <el-button style="background-color: #f1129c; color:white">SUBSCRIBE</el-button>
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

import Info from '@/views/documentation/components/info'
import Info2 from '@/views/documentation/components/info2'
import Info3 from '@/views/documentation/components/info3'
import Info4 from '@/views/documentation/components/info4'
import Info5 from '@/views/documentation/components/info5'
export default {
  name: 'DashboardAdmin',
  components: {
    Info, Info2, Info3, Info4, Info5
  },
  data() {
    return {
      input: '',
      input2: '',
      activeName: '',
      fits: 'scale-down',
      url: 'https://www.watsons.com.tr/medias/sys_master/root/h66/hce/8992832847902/1300x500/1300x500.png',
      subMenu: []
    }
  },
  mounted() {

  },
  methods: {
    basket() {
      fetch('https://dummyjson.com/carts/add', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({
          userId: 1,
          products: [
            {
              id: 1,
              quantity: 1
            }
          ]
        })
      })
        .then(res => res.json())
        .then(this.$message({
          message: 'Added to the chart.',
          type: 'success'
        }))
    },
    search() {
      fetch('https://dummyjson.com/products/search?q=' + this.input2)
        .then(res => res.json())
        .then(this.$message({
          message: this.input2 + ' searched.',
          type: 'success'
        }))
      this.input2 = ''
    },
    subscribe() {
      fetch('https://dummyjson.com/users/search?q=' + this.input)
        .then(res => res.json())
        .then(this.$message({
          message: this.input + ' added our newsletter group.',
          type: 'success'
        }))
      this.input = ''
    },
    handleClick() {
      // console.log(this.subMenu);
      fetch('https://dummyjson.com/products/categories').then(response =>
        response.json().then(data => ({
          data: data
        })
        ).then(res => {
          this.subMenu.push(res.data)
        }))
      console.log(this.subMenu)
    }

  }
}
</script>

<style lang="scss" scoped>
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
.el-button--medium{
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

@media (max-width:1024px) {
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
