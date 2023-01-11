<template>
  <view class="content">
    <view>
      <van-button type="primary">主要按钮</van-button>
      <van-button type="info">信息按钮</van-button>
      <van-button type="default">默认按钮</van-button>
      <van-button type="warning">警告按钮</van-button>
      <van-button type="danger">危险按钮</van-button>
      <van-checkbox v-model="checked">复选框</van-checkbox>
      <van-cell-group inset>
        <van-icon name="chat" dot />

        <van-cell title="单元格" value="内容" />
        <van-cell title="单元格" value="内容" label="描述信息" />
      </van-cell-group>
      <view>小程序</view>
      <van-icon name="chat" info="9" />
      <van-icon name="chat" info="99+" />
      <van-icon name="bag" />
      <van-icon name="chat" color="red" />
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      date: "",
      show: true,
      radio: "1",
      checked: true,
      num: 2222,
    };
  },
  methods: {
    formatDate(date) {
      return `${date.getMonth() + 1}/${date.getDate()}`;
    },
    onConfirm(date) {
      this.show = false;
      this.date = this.formatDate(date);
    },
  },
};
</script>

<style lang="scss">
::v-deep .van-icon-bag {
  margin-left: 50px;
  color: red;
  font-size: 140px;
}
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200rpx;
  width: 200rpx;
  margin: 200rpx auto 50rpx auto;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36rpx;
  color: #8f8f94;
}
</style>
