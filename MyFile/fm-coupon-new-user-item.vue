<template>
  <div class="wrapper">
    <div class="coupon-merchant">
      <img class="merchant-icon" :src="merchantIcon" />
      <div class="merchant-tip">{{merchantName}}</div>
    </div>

    <div class="coupon-wrapper">
      <img class="coupon-container-img" :src="couponBg" />

      <div class="coupon-container">
        <div class="coupon-box">
          <div class="coupon-box-left">
            <div class="coupon-amount">
              <div class="price-symbol">{{i18n.bill.priceSymbol}}</div>
              <div class="amount">{{preferentialAmount}}</div>
              <div class="price-decimal">{{preferentialAmountDecimal}}</div>
            </div>

            <div class="coupon-content-date">
              <div class="coupon-content">{{preferentialContent}}</div>
            </div>
          </div>

          <div class="coupon-box-right">
            <div class="coupon-name">{{couponName}}</div>
            <div class="coupon-middle">
              <div>
                <div :class="['coupon-date']">{{expireTime}}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Utils from '@/utils/utils'
import baseURLConfig from '@/utils/baseURLConfig'

export default {
  name: 'coupon-new-user-item',
  props: {
    // 优惠券数据
    coupon: {
      type: Object,
      default: () => {}
    }
  },
  data () {
    return {
      couponBg: baseURLConfig.STATICPATH + '/coupon/new_user_coupon_bg.png',
      merchantIcon: baseURLConfig.STATICPATH + '/coupon/merchant_icon.png',
    }
  },

  computed: {
    i18n () {
      return this.$t('index')
    },
    // 优惠券金额整数
    preferentialAmount () {
      return parseInt(Number(this.coupon.preferentialAmount))
    },
    // 优惠券金额小数
    preferentialAmountDecimal () {
      let preferentialAmount = Number(this.coupon.preferentialAmount)

      if (('' + preferentialAmount).indexOf(".") === -1) {
        return ''
      }

      return ('' + preferentialAmount).substr(('' + preferentialAmount).indexOf("."))
    },
    // 商家名称
    merchantName () {
      return this.i18n.coupon.limitBuy + this.coupon.merchantName +this.i18n.coupon.merchant || ''
    },
    // 优惠券名称
    couponName () {
      return this.coupon.name || ''
    },
    // 过期时间文案
    expireTime () {
      let time = Number(this.serverTimeStamp)
      let expireTime = this.coupon.usingEndTime
      let receivingUsingDays = this.coupon.receivingUsingDays
      let usingStartTime = this.coupon.usingStartTime
      let result = ''

      if (receivingUsingDays) {
        result =  '领取当日起' + receivingUsingDays + '天内使用'
      } else if (usingStartTime >= time) {
        let start = Utils.formatDate(usingStartTime ? new Date(usingStartTime) : new Date(), 'yyyy.MM.dd')
        let end = Utils.formatDate(expireTime ? new Date(expireTime) : new Date(), 'yyyy.MM.dd')

        result = start + '-' + end
      } else {
        let end = Utils.formatDate(expireTime ? new Date(expireTime) : new Date(), 'yyyy.MM.dd')

        result =  this.i18n.coupon.effectiveDateTo + this.i18n.coupon.colon + end
      }

      return result
    },
    // 满减文案
    preferentialContent () {
      let fullReduction = '满' + Number(this.coupon.orderAmountThreshold) + '元可用'

      return fullReduction
    }
  }
}
</script>

<style scoped>
.coupon-container-img {
  width: 708rpx;
  height: 251rpx;
}
.coupon-wrapper {
  position: relative;
}

.coupon-merchant {
  display: flex;
  align-items: center;
  margin: 5rpx 0 17rpx 9rpx;
}
.merchant-icon {
  width: 30rpx;
  height: 30rpx;
  margin-right: 9rpx;
}
.merchant-tip {
  font-size: 24rpx;
  font-weight: 400;
  color: #666666;
}

.coupon-container {
  width: 100%;
  position: absolute;
  top: 0;
}

.coupon-box {
  display: flex;
  justify-content: space-between;
}
.coupon-box-left {
  width: 225rpx;
  height: 230rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  position: relative;
}
.coupon-amount {
  margin-top: 60rpx;
  display: flex;
  align-items: baseline;
  justify-content: center;
  color: #FFFFFF;
  font-weight: 400;
}
.price-symbol {
  font-size: 28rpx;
}
.amount {
  font-size: 50rpx;
}
.price-decimal {
  font-size: 30rpx;
}
.coupon-content-date {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
}
.coupon-content {
  margin-top: 15rpx;
  font-size: 24rpx;
  font-weight: 400;
  color: #FFFFFF;
}

.coupon-box-right {
  width: 463rpx;
  height: 155rpx;
  margin-left: 20rpx;
  padding-top: 35rpx;
  padding-bottom: 35rpx;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.coupon-name {
  font-size: 32rpx;
  font-weight: 500;
  color: #343434;
}
.coupon-middle {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  flex-grow: 2;
}
.coupon-date {
  margin-top: 7rpx;
  font-size: 22rpx;
  font-weight: 400;
  color: #9A9A9A;
}
.warn {
  color: #E4402F;
}
</style>