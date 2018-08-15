<template>
  <div class="counter-warp">
    所属银行
      <div class="weui-cells weui-cells_after-title">
        <div class="weui-cell weui-cell_input">
          <div class="weui-cell__hd">
            <div class="weui-label">当前选择</div>
          </div>
          <div class="weui-cell__bd">
            <picker @click="bindPickerChange" v-model="index" :range="array">
              <div class="weui-input">{{array[index]}}</div>
            </picker>
          </div>
        </div>
      </div>
    所属银行
    所属银行
    账单日
    还款日
  </div>
</template>

<script>
export default {
  data () {
    return {
      array: ['中国', '美国', '巴西', '日本'],
      index: 0,
      date: '2016-09-01',
      time: '12:01'
    }
  },
  methods: {
    bindPickerChange (e) {
      console.log('picker发送选择改变，携带值为', e)
      // this.index = e.value
      // this.setData({
      //   index: e.detail.value
      // })
    }
    // bindDateChange (e) {
    //   this.setData({
    //     date: e.detail.value
    //   })
    // },
    // bindTimeChange (e) {
    //   this.setData({
    //     time: e.detail.value
    //   })
    // }
  }
}
</script>

<style>
.counter-warp {
  text-align: center;
  margin-top: 100px;
}
.home {
  display: inline-block;
  margin: 100px auto;
  padding: 5px 10px;
  color: blue;
  border: 1px solid blue;
}
</style>
