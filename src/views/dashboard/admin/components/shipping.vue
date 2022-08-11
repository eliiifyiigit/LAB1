<template>
  <div>
    <el-row
      justify="space-between"
      :gutter="20"
    >
      <el-col
        :md="{'offset':0, 'span':12}"
        :lg="{'offset':0, 'span':12}"
        :sm="4"
      >
        <span style="font-size: 10px">First Name*</span>
        <el-input v-model="form.name" />
      </el-col>
      <el-col
        :md="{'offset':0, 'span':12}"
        :lg="{'offset':0, 'span':12}"
        :sm="4"
      >
        <span style="font-size: 10px">Last Name*</span>
        <el-input v-model="form.surname" />
      </el-col>
      <el-col
        :md="{'offset':0, 'span':12}"
        :lg="{'offset':0, 'span':12}"
        :sm="4"
        style="padding-top: 10px"
      >
        <span style="font-size: 10px">Email Address*</span>
        <el-input v-model="form.email" />
      </el-col>
      <el-col
        :md="{'offset':0, 'span':12}"
        :lg="{'offset':0, 'span':12}"
        :sm="4"
        style="padding-top: 10px"
      >
        <span style="font-size: 10px">Phone Number*</span>
        <el-input v-model="form.phone" />
      </el-col>
      <el-col
        :md="{'offset':0, 'span':12}"
        :lg="{'offset':0, 'span':12}"
        :sm="12"
        style="padding-top: 10px"
      >
        <span style="font-size: 10px">City*</span>
        <el-select v-model="form.value1" style="width: 100%" placeholder="Select" @change="city">
          <el-option
            v-for="item in options"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          />
        </el-select>
      </el-col>
      <el-col
        :md="{'offset':0, 'span':12}"
        :lg="{'offset':0, 'span':12}"
        :sm="12"
        style="padding-top: 10px"
      >
        <span style="font-size: 10px">District*</span>
        <el-select v-model="form.value2" style="width: 100%" placeholder="Select" :disabled="disabled">
          <el-option
            v-for="item in options2"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          />
        </el-select>
      </el-col>
      <el-col
        :md="{'offset':0, 'span':24}"
        :lg="{'offset':0, 'span':24}"
        :sm="4"
        style="padding-top: 10px"
      >
        <span style="font-size: 10px">Address*</span>
        <el-input
          v-model="form.address"
          type="textarea"
          placeholder="Enter neighborhood, street, avenue and other information"
        />
      </el-col>
    </el-row>
    <el-row
      justify="space-between"
      :gutter="20"
    >
      <el-col
        :md="{'offset':0, 'span':24}"
        :lg="{'offset':0, 'span':24}"
        style="padding-top: 20px"
      >
        <span><i class="el-icon-bank-card" /><strong>Payment Details</strong></span>
      </el-col>
      <el-col
        :md="{'offset':1, 'span':24}"
        :lg="{'offset':1, 'span':24}"
        :sm="4"
        style="padding-top: 20px; width: 50%"
      >
        <span style="font-size: 10px">Card Holder Name*</span>
        <el-input v-model="form.cardName" />
        <span style="font-size: 8px">Full name on card</span>
      </el-col>

      <el-col
        :md="{'offset':1, 'span':24}"
        :lg="{'offset':1, 'span':24}"
        :sm="4"
        style="padding-top: 20px; width: 50%"
      >
        <span style="font-size: 10px">Card Number*</span>
        <el-input v-model="form.cardNumber" />
        <span style="font-size: 8px">Enter digits without spaces</span>
      </el-col>

      <el-col
        :md="{'offset':1, 'span':11}"
        :lg="{'offset':1, 'span':11}"
        :sm="4"
        style="padding-top: 20px"
      >
        <span style="font-size: 10px">Expiry Date*</span><br>
        <el-date-picker
          v-model="form.date1"
          type="date"
          placeholder="MM/YY"
        />
      </el-col>
      <el-col
        :md="{'offset':0, 'span':3}"
        :lg="{'offset':0, 'span':3}"
        :sm="4"
        style="padding-top: 20px; margin-right: 180px"
      >
        <span style="font-size: 10px">CVV*</span>
        <el-tooltip class="item" effect="dark" content="CVV" placement="right">
          <el-input v-model="form.cvv" />
        </el-tooltip>
        <span style="font-size: 8px">* Required fields</span>
      </el-col>
      <el-col
        :md="{'offset':1, 'span':11}"
        :lg="{'offset':1, 'span':11}"
        :sm="4"
        style="padding-top: 20px"
      >
        <el-button style="width: 100%; background-color: rgba(255, 39, 173, 0.5); color: white">PAY NOW</el-button>
      </el-col>
    </el-row>

  </div>
</template>

<script>
export default {
  name: 'Shipping',
  data() {
    return {
      disabled: true,
      form: {
        name: '',
        cvv: '',
        cardName: '',
        cardNumber: '',
        surname: '',
        email: '',
        phone: '',
        date1: '',
        value1: '',
        value2: '',
        address: ''
      },
      options: [{
        value: 'Istanbul',
        label: 'Istanbul'
      }, {
        value: 'Ankara',
        label: 'Ankara'
      }, {
        value: 'Izmir',
        label: 'Izmir'
      }],
      options2: []

    }
  },
  mounted() {
  },
  methods: {
    city() {
      if (this.form.value1 === 'Istanbul') {
        this.form.value2 = ''
        this.options2 = []
        this.disabled = false
        this.options2.push({
          value: 'Umraniye',
          label: 'Umraniye'
        })
      }
      if (this.form.value1 === 'Ankara') {
        this.form.value2 = ''
        this.options2 = []
        this.disabled = false
        this.options2.push({
          value: 'Kızılay',
          label: 'Kızılay'
        })
      }
      if (this.form.value1 === 'Izmir') {
        this.form.value2 = ''
        this.options2 = []
        this.disabled = true
      }
    }
  }
}
</script>

<style scoped>

</style>
