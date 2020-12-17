<!-- <div class="article-title">邀请好友获赠优惠券规则</div>
            <div class="article-content">
1、您邀请的好友为新用户，Ta注册登录完成即可获赠“好友邀请优惠券”。
特别提示：如您邀请的好友已经在益农源选注册，则不属于新用户。
2、您邀请的新用户只要完成了首单交易，您将获得“邀请好友优惠券”。
3、若您邀请的好友，也被其他用户邀请，则优惠券将发放给新用户访问的首个分享页面所属的源选用户；而被邀请的新用户也只能领取一次“好友邀请优惠券”。
            </div>
            <div class="article-title">优惠券的获得和使用规则</div>
            <div class="article-content">
1、若系统判定违反活动规则，优惠券讲不予正常发放，以“邀请有礼”页面中“查看邀请记录”为准。
2、新用户获得的“好友邀请优惠券”有效期7天，适用于全场除少量特殊商品外的其他商品。以兑换的优惠券使用说明为准。
3、您邀请的新用户下单购买后，所获得的“邀请好友优惠券”有效期60天，适用于全场除少量特殊商品外的其他商品。以兑换的优惠券使用说明为准。
            </div>
            <div class="article-title">其他规则</div>
            <div class="article-content">
如果用户出现违规行为（如以不正当手段获取权益、以所获得权益进行盈利、作弊领取、恶意注册、虚假交易、不当使用、违背诚实信用等），益农源选将视情节严重程度按照相关规定对用户进行处罚，包括但不限于取消用户邀请资格、撤销相关违规交易、收回奖励、封禁账号、依法追求其法律责任等。
益农源选可以根据活动的实际举办情况对活动规则进行变动或调整，相关变动或调整将公布在活动页面上，公布后依法生效。
            </div> -->
			
			
      var str="18912341234"
      var pat=/(\d{3})\d*(\d{4})/
      var b=str.replace(pat,'$1****$2');
      console.log(b)
	  
	  
      console.log(couponIds)
      couponIds = [493, 492, 491]
	  

	 
item_id
goodsSpecId
name
image
price
stock
discountStock
noneActivityStock
isInvalid
preheat_time
discount_start_time
discount_end_time
is_discount
discount_price

optimumCouponInfo
discountLimitQuantity
usedDiscount
cartQuantity


{
  "activityGoodsList": [
    {
      "activityId": 241,
      "barCode": "2020070280423940",
      "createdBy": 2,
      "createdTime": 1594091987100,
      "deleted": false,
      "description": "啦啦啦啦啦啦",
      "goodsSpecId": 274,
      "id": 2786,
      "image": "https://zgyn-dev.oss-cn-huhehaote.aliyuncs.com/activity_goods/8afef05779704ef1aa42d2e4cd8b894e.jpg",
      "isDeleted": false,
      "lastModifiedBy": 0,
      "lastModifiedTime": 1594091998129,
      "mustSelect": true,
      "name": "TF产品一号",
      "price": 10,
      "size": "80毫米；90毫米",
      "sort": 1,
      "status": 0,
      "stock": 100,
      "unit": "个"
    }
  ],
  "amountEnd": 1000,
  "amountStart": 10,
  "code": "2020070280423940",
  "contactNumber": "13574044254",
  "createdBy": 2,
  "createdTime": 1594091987100,
  "deleted": false,
  "description": "啦啦啦啦啦啦啦",
  "employeeIdList": [5778,5779,5780,5787],
  "endTime": 1596124800000,
  "freightFee": 10,
  "id": 241,
  "image": "https://zgyn-dev.oss-cn-huhehaote.aliyuncs.com/ep-portal/image/2020-7-7/9d1b3380c00011ea98b85b6f7100b95a-thumb.jpg",
  "isDeleted": false,
  "isTrialVersion": false,
  "labourUnionId": 82,
  "labourUnionName": "TFboys工会",
  "lastModifiedBy": 0,
  "lastModifiedTime": 1594091998129,
  "name": "TF活动二号",
  "shippingTips": "发货提示",
  "shippingType": "DELIVERY",
  "startTime": 1594091953000,
  "status": "ACTIVE",
  "subName": "哈哈哈哈哈哈哈"
}

这是一个很长的活动描述这是一个很长的活动描述这是一个很长的活动描述这是一个很长的活动描述这是一个很长的活动描述这是一个很长的活动描述这是一个很长的活动描述这是一个很长的活动描述这是一个很长的活动描述

小小的年纪，还不懂什么是爱，却被你甜甜的笑给打败，你眨着大大的眼睛，噢 那么可爱，说话的手往哪儿摆，每一天上课下课，都会有你的陪伴，每一秒内容我都很喜欢，解不开的几何图案，和你红的脸，到底有多少个答

我想你也曾有过 在青春里蹒跚跋涉 有着远大的梦 也无情破灭过 我觉得你也像我 是个不愿服输的孩子 很多艰难叵测 心中仍有一团火 滚烫的青春 我自己也恨 在很多时分 怎么这么无能 滚烫的青春 我没有天



H5/APP与企业购的授权逻辑
1. H5/APP需要先登录才能跳转到企业购首页，跳转到企业购首页需要传H5/APP的jwt-token
2. 企业购首页将源选的jwt-token设置到yx-jwt-token中，向源选的API发请求，由源选服务端向企业购服务端获取企业购的jwt-token
3. 将企业购的jwt-token设置到jwt-token中。
企业购H5根据需要向源选或者企业购服务端发请求，传递yx-jwt-token或者jwt-token

源选自动登录企业购流程:
1. 用户角色校验，确定用户是否具有企业购权限，能否登录到企业购
  API: POST /v1/users/roles-check  参数 roles 包含 [enterprise_purchase]
  返回示例: {
  "statusCode": 200,
  "data": {
    "enterprise_purchase": false,
    "buyer": true
  }
}
2. 拥有企业购权限用户，点击跳转企业购相关登录页面，携带 [源选 jwt-token, 源选 refresh_token, 源选 clientType] 三个信息 (token信息在用户登录API返回)
3. 在企业购页面，调用企业购 API: GET /v1/sso/yx-auth
header参数[yx-token, yx-refresh-token, yx-client-type] 此三个信息即从源选平台带来的三个信息。yx-refresh-token 默认非必传，但是从源选带来的 token 有可能接近过期，传递 yx-refresh-token 该 API 将自动通过 yx-refresh-token 刷新 token
该 API 返回示例: {
  "statusCode": 200,
  "data": {
    "yxToken": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJ5bl8zYnMwMDAyd3UwbiIsInVpZCI6OTcwMywicGxhdGZvcm1fdHlwZSI6bnVsbCwiY3JlYXRlZCI6MTU5NDAyMzQwODEzOCwiY2xpZW50X3R5cGUiOiJINSIsImV4cCI6MTU5NTMxOTQwOH0.0cM61ZdhN0gZK4-5jN9v--HwWIkjlAdURaNv44gAh0zww7tIHgO4xXYw2yDQlFsEMxXYfbupFD7TzQWmYerJLg",
    "yxRefreshToken": null,
    "userId": 5788,
    "userCode": "000832",
    "token": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiLmm7nlrocyMjEiLCJ1aWQiOjU3ODgsImNyZWF0ZWQiOjE1OTQwMjM0MTgwMzIsImNsaWVudF90eXBlIjoiUEMiLCJleHAiOjE1OTUzMTk0MTh9.KHrCcPTPD-zGeLdy-GuToTXUWck9Uq3h7EXFPxg01qv0VVi2lc-oMGoNe1VPD170LOiLw0Ms4aqNjSGnErwXOg"
  }
}
userId, userCode, token 即企业购相关登录信息
yxToken, yxRefreshToken 为源选token信息，这里需要判断返回来的和传递到后台的 header 参数是否一致(传递yx-refresh-token的情况下)，如果不一致则表示之前的 yx-token 已经过期，已经重刷了 源选 token
4. 前台保存相应登录信息 ...

源选自动登录与API调用有所改动:
a. 调用源选API GET /v1/users/auth-state 获取 state 校验参数（有效时间30s），参数 thirdAuthClientType = ENTERPRISE_PURCHASE 时会校验用户是否有企业购权限
b. 携带获取的 state 参数页面跳转至企业购登录验证页面
c. 企业购前台调用企业购自己的后台API GET /v1/sso/yx-auth 将 state 传至后台，state校验通过则会获得token信息，例
{
  "statusCode": 200,
  "data": {
    "yx_user_id": "9702",
    "yx_user_name": "yn_b2v000146oe",
    "userId": 5787,
    "userCode": "000831",
    "token": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiLmm7nlrocxMjIiLCJ1aWQiOjU3ODcsImNyZWF0ZWQiOjE1OTQxNzc1OTgzMDAsInl4X3VzZXJfaWQiOiI5NzAyIiwieXhfdXNlcl9uYW1lIjoieW5fYjJ2MDAwMTQ2b2UiLCJjbGllbnRfdHlwZSI6Ikg1IiwiZXhwIjoxNTk1NDczNTk4fQ.mCFHrG5NGCKRyHgXIwZIgqDHHBnnW3FedC14e51hmaBkpuYxMvv_y2oUbil3XHgi17UBkZPSDte_IlVgvuDXcA"
  }
}
d. 企业购前台要调用源选API，不需要用源选token调用源选path，改为调用自己的API
例：源选原API：http://39.104.37.247:8001/v1/proxy/v1/users/current
只需要将 path 指定的IP修改成企业购自己IP并加上 /v1/proxy
即 http://39.104.67.36:8082/v1/proxy/v1/users/current
所有源选API调用都采用 http://39.104.67.36:8082/v1/proxy + [API Path] 的方式调用，且不需要考虑源选token

可用账号 13110000001, 13110000002 / cyril111
http://172.20.56.85:8081/h5-home/activity?state=F4CCNX2I11
http://127.0.0.1:8081/h5-home/activity?state=F4CCNX2I11

        let auth = {
          token: "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiLnjovmupDlkYAgIEN5bnRoaWEiLCJ1aWQiOjU4MTksImNyZWF0ZWQiOjE1OTQ2MjkwNDMwMjAsInl4X3VzZXJfaWQiOiIxMTU3IiwieXhfdXNlcl9uYW1lIjoieW5fc3ExNDI1NHd6bXciLCJjbGllbnRfdHlwZSI6Ikg1IiwiZXhwIjoxNTk1OTI1MDQzfQ.0efK4o3WWnGNDzh7box84cj-ezSSGaVyAjYKNiYmZaNCheaCpD4HETZqqr3GdFNYOkqwZOhxQDA7r6F-c0v2vA",
          userCode: null,
          userId: 5819,
          yx_user_id: "1157",
          yx_user_name: "yn_sq14254wzmw",
        }
        this.$store.commit('setAuth', auth)
        Session.setToken(auth)
        Cookie.set('auth', auth)


企业购下单API:
01106 : 商品下架
01107： 库存不足
01108： 价格变化
01109： 商品不属于活动
1、从活动中移除：商品【商品名称】已下架，刷新，商品移入失效列表（已下架）
2、结算一个下架商品：商品【商品名称】已下架，刷新页面，商品移入失效列表（已下架）
3、结算多个其中包含下架的商品：商品【商品名称】已下架，刷新页面，商品移入失效列表（已下架）
4、商品库存不足：商品【商品名称】库存不足，刷新页面，购物车中显示可购数量
5、商品售罄：商品【商品名称】库存不足，刷新页面，商品移入失效列表（已售罄）



已失效：357
TF活动九号 已失效的

未开始：359
TF活动十号 啦啦啦啦啦啦

无权限：355
TF活动八号啦啦啦啦啦啦



2.1.0的优惠券讨论的细节总结, 后续文档会更新
1.  优惠券上面展示有效日期/有效期至的会包含以下4种情况 @Cindy Yang @Cynthia @Alice 王唯一 @Melissa(唐杰) 
    若未触达优惠券使用开始时间，有效日期展示优惠券使用开始时间和结束时间；（此处比较开始时间， 需要比较年月日时分秒）
    若已触达优惠券使用开始时间，展示有效期至结束时间；
    若已触达优惠券使用开始时间，且结束时间只有1天，展示还剩1天到期；（此处只比较结束时间的年月日， 不比较时分秒）
    若用券时间类型为领券当日起x天内使用，则有效日期展示领券当日起x天内使用

	
1、xxx至xxx领券，yyy至yyy用券
  未领取/继续领取：领取时间xxx-xxx
  达到领取上限：使用时间yyy-yyy
  
  领券中心：
  未领取：使用时间
  继续领取：使用时间
  达到领取上限：使用时间
  
  我的优惠券：
  有效期至：使用时间
  
2、xxx至xxx领券，领券当日起YY天内可使用
  未领取/继续领取：领取时间xxx-xxx
  达到领取上限：领取当日起YY天内使用
  
  领券中心：
  未领取：领取当日起99天内使用
  继续领取：领取当日起99天内使用
  达到领取上限：领取当日起99天内使用
  
  我的优惠券：
  有效期至：2020.10.23
  
3、长期可领取，领券当日起YY天内可使用
  未领取/继续领取：长期有效
  达到领取上限：领取当日起YY天内使用
  
  领券中心：
  未领取：领取当日起199天内使用
  继续领取：领取当日起199天内使用
  达到领取上限：领取当日起199天内使用
  
  我的优惠券：
  有效期至：2021.01.31
  
4、xxx至xxx领取和使用
  未领取/继续领取：领取时间xxx-xxx
  达到领取上限：使用时间xxx-xxx
  
  领券中心：
  未领取：有效期至：2020.07.31
  继续领取：有效期至：2020.07.31
  达到领取上限：有效期至：2020.07.31
  
  我的优惠券：
  有效期至：2021.01.31
  
  
  
1、xxx至xxx领券，yyy至yyy用券
  领券中心：
  未领取：使用时间
  继续领取：使用时间
  达到领取上限：使用时间
  
  我的优惠券：
  使用时间
  
2、xxx至xxx领券，领券当日起YY天内可使用
  领券中心：
  未领取：领取当日起99天内使用
  继续领取：领取当日起99天内使用
  达到领取上限：领取当日起99天内使用
  
  我的优惠券：
  有效期至：2020.10.23
  
3、长期可领取，领券当日起YY天内可使用
  领券中心：
  未领取：领取当日起199天内使用
  继续领取：领取当日起199天内使用
  达到领取上限：领取当日起199天内使用
  
  我的优惠券：
  有效期至：2021.01.31
  
4、xxx至xxx领取和使用
  领券中心：
  未领取：有效期至：2020.07.31
  继续领取：有效期至：2020.07.31
  达到领取上限：有效期至：2020.07.31
  
  我的优惠券：
  有效期至：2021.01.31
  
  
  

availableType: "ALL"
code: "2020071600000004"
couponStock: 992
createBy: 11
createTime: 1594876958092
endTime: 1598803200000
excludedGoods: null
expired: false
expiredRemind: false
expiredRemindDays: 0
expiredRemindTime: null
giveable: true
grantManageId: null
hasReceived: true
id: 213
isDeleted: false
lastModifiedBy: 11
lastModifiedTime: 1594886914000
lastReceivingTime: 1594879640259
merchantId: 18
merchantName: "许嘉零测试企业商家名企业商家名"
name: "TF优惠券xxx至xxx领取用"
orderAmountThreshold: 89.99
platformType: null
preferentialAmount: 89.98
preferentialContent: "满89.99元减89.98元"
public: true
receivingAvailable: true
receivingEndTime: 1598803200000
receivingLimitationNumber: 0
receivingLimitationType: "NONE"
receivingStartTime: 1594876944000
receivingUsingDays: null
receivingUsingType: "RECEIVING_AND_USING_IN_SAME_TIME"
relatedCategories: null
relatedGoods: null
stackable: true
startTime: 1594876944000
status: "PROCESSING"
useDefaultInstructions: false
used: false
userLimitationType: "NONE"
usingEndTime: 1598803200000
usingInstructions: "全部商品可用;可转赠优惠券;可与限时折扣活动叠加使用；TF优惠券xxx至xxx领取用TF优惠券xxx至xxx领取用TF优惠券xxx至xxx领取用TF优惠券xxx至xxx领取用TF优惠券xxx至xxx领"
usingStartTime: 1594876944000

====================================================================================
availableType: "ALL"
code: "2020071600000003"
couponStock: 97
createBy: 11
createTime: 1594876894946
endTime: 33336115200000
excludedGoods: null
expired: false
expiredRemind: false
expiredRemindDays: 0
expiredRemindTime: null
giveable: true
grantManageId: null
hasReceived: true
id: 212
isDeleted: false
lastModifiedBy: 11
lastModifiedTime: 1594886161000
lastReceivingTime: 1594886161752
merchantId: 18
merchantName: "许嘉零测试企业商家名企业商家名"
name: "TF优惠券长期可领取呀呀呀呀呀"
orderAmountThreshold: 8.88
platformType: null
preferentialAmount: 8.87
preferentialContent: "满8.88元减8.87元"
public: true
receivingAvailable: true
receivingEndTime: 32472115200000
receivingLimitationNumber: 0
receivingLimitationType: "NONE"
receivingStartTime: 1594876894946
receivingUsingDays: 10000
receivingUsingType: "LONG_TERM_RECEIVING_THEN_USING_IN_DAYS"
relatedCategories: null
relatedGoods: null
stackable: true
startTime: 1594876894946
status: "PROCESSING"
useDefaultInstructions: false
used: false
userLimitationType: "NONE"
usingEndTime: null
usingInstructions: "全部商品可用;可转赠优惠券;可与限时折扣活动叠加使用；TF优惠券长期可领取呀呀呀呀呀TF优惠券长期可领取呀呀呀呀呀TF优惠券长期可领取呀呀呀呀呀TF优惠券长期可领取呀呀呀呀呀TF优惠券长期可领取呀呀呀"
usingStartTime: null

=============================================================================================
availableType: "ALL"
code: "2020071600000002"
couponStock: 94
createBy: 11
createTime: 1594876842967
endTime: 1682524800000
excludedGoods: null
expired: false
expiredRemind: false
expiredRemindDays: 0
expiredRemindTime: null
giveable: true
grantManageId: null
hasReceived: true
id: 211
isDeleted: false
lastModifiedBy: 11
lastModifiedTime: 1594885182000
lastReceivingTime: 1594877080783
merchantId: 18
merchantName: "许嘉零测试企业商家名企业商家名"
name: "TF优惠券xxx领券当日几天用"
orderAmountThreshold: 9999.99
platformType: null
preferentialAmount: 499.99
preferentialContent: "满9999.99元减499.99元"
public: true
receivingAvailable: true
receivingEndTime: 1596124800000
receivingLimitationNumber: 0
receivingLimitationType: "NONE"
receivingStartTime: 1594876827000
receivingUsingDays: 1000
receivingUsingType: "RECEIVING_IN_TIME_THEN_USING_IN_DAYS"
relatedCategories: null
relatedGoods: null
stackable: true
startTime: 1594876827000
status: "PROCESSING"
useDefaultInstructions: false
used: false
userLimitationType: "NONE"
usingEndTime: null
usingInstructions: "全部商品可用;可转赠优惠券;可与限时折扣活动叠加使用；TF优惠券xxx领券当日几天用TF优惠券xxx领券当日几天用TF优惠券xxx领券当日几天用TF优惠券xxx领券当日几天用TF优惠券xxx领券当日几"
usingStartTime: null

========================================
availableType: "ALL"
code: "2020071600000001"
couponStock: 97
createBy: 11
createTime: 1594876690977
endTime: 1596816000000
excludedGoods: null
expired: false
expiredRemind: false
expiredRemindDays: 0
expiredRemindTime: null
giveable: true
grantManageId: null
hasReceived: true
id: 210
isDeleted: false
lastModifiedBy: 11
lastModifiedTime: 1594886020000
lastReceivingTime: 1594877075490
merchantId: 18
merchantName: "许嘉零测试企业商家名企业商家名"
name: "TF优惠券xxx领券xxx用券"
orderAmountThreshold: 168.88
platformType: null
preferentialAmount: 168.87
preferentialContent: "满168.88元减168.87元"
public: true
receivingAvailable: true
receivingEndTime: 1596124800000
receivingLimitationNumber: 0
receivingLimitationType: "NONE"
receivingStartTime: 1594876650000
receivingUsingDays: null
receivingUsingType: "RECEIVING_IN_TIME_USING_IN_TIME"
relatedCategories: null
relatedGoods: null
stackable: true
startTime: 1594876650000
status: "NOT_STARTED"
useDefaultInstructions: false
used: false
userLimitationType: "NONE"
usingEndTime: 1596816000000
usingInstructions: "全部商品可用;可转赠优惠券;可与限时折扣活动叠加使用;TF优惠券xxx领券xxx用券TF优惠券xxx领券xxx用券TF优惠券xxx领券xxx用券TF优惠券xxx领券xxx用券TF优惠券xxx领券xxx"
usingStartTime: 1596211200000



https://dev.zgyn.net/gitlab/cisdi-yn-farmer/h5-new/commit/eedb33e9080f34d49f8921fa4f422500f4e29721
https://dev.zgyn.net/gitlab/cisdi-yn-farmer/h5-new/commit/0779a7b64edfd5974ee9958e8b064161931c66ed

git commit -m "fix(h5-new): 修复下单页优惠券展示及UI问题，修复商品详情页领券问题  修复 #7913"
 http://39.104.49.247/api/v1/goods/query?pageIndex=1&pageSize=10&supplyChannel=RETAIL&isTop=true

你需要我的傻笑我需要你的拥抱
爱情就需要这样它才不会单调
我知道有时候也需要吵吵闹闹
但始终也知道只有你对我最好
豆浆离不开油条让我爱你爱到老
爱情就需要这样它才幸福美好
我知道都知道你知道你都知道
好不好别偷笑让我知道
好不好别偷笑让我知道就好
我喝完热豆浆眷恋着还想要
你吃完金黄油条爱情又要再发酵

switchDiscountAndStaraightDown：
	isDiscount：no
	isStraightDown：no
	isDiscountPreheat：
	isStraightDownPreheat：1
	isStraightDownGoing：1
isDiscountGoing：1
noneActivityStock：1
activityStock：1

未选任何优惠券：不展示可叠加标签，
选择一张优惠券或者一张运费券，优惠券或运费券展示可叠加标签
选择一张优惠券和一张运费券，不展示可叠加标签


运费券：需要type一致
商品券：

啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊呀呦呀呀呀呀呀呀呀

当前：2
左滑：3变高
右滑：1变高


4594
4668
4853
4980
5049
5104
5248
6081
6226
6447
6691
6801
7059
7338
7562
7840
7960
8039
8084

Cynthia 测试团购 无营销信息
Cynthia 测试团购  有营销信息呀呀呀呀呀呀呀
测试环境一下
测试一下商品库存
测试库存荔枝
磨砂磨砂视频视频视频
益农好吃的芒果呀
测试活动中非活动库存为0


    setFontSize () {
      var docEl = window.documentElement;
      var clientWidth = document.documentElement.clientWidth;
      if(!clientWidth) return;
      //原本对于html的字号设置 我这里用的是750的标准 ，640的也是同理
      docEl.style.fontSize = 100 * (clientWidth / 750) + 'px';
      if(window.getComputedStyle(document.getElementsByTagName("html")[0]).fontSize) {
        var size = window.getComputedStyle(document.getElementsByTagName("html")[0]).fontSize.split('p')[0];
        //这里再取出当前html的font-size，和你想附的值进行比较，
        //这里为什么不直接用size< 原因是正常机型的size也不一定等于你想附的值，尝试了很多机型，除了问题机型外，一般差距很小，另一半完全相等;
        //为什么不直接*1.25 也不解释了 最终比例不一定是1.25
        if(size*1.2 < 100 * (clientWidth / 750)) {
        //如果当前html的font-size 的1.2倍仍然小于 之前想设置的值，就说明是问题机型，给之前想附的值乘1.25倍，这样他会被系统再次除1.25得到的才是我们想附的值
          docEl.style.fontSize = 125 * (clientWidth / 750) + 'px';
        }
      }
    },
	
	
窗外的麻雀在电线杆上多嘴

你说这一句很有夏天的感觉

手中的铅笔在纸上来来回回

我用几行字形容你是我的谁

秋刀鱼的滋味猫跟你都想了解

初恋的香味就这样被我们寻回

那温暖的阳光像刚摘的鲜艳草莓

你说你舍不得吃掉这一种感觉

雨下整夜我的爱溢出就像雨水

院子落叶跟我的思念厚厚一叠

几句是非也无法将我的热情冷却

你出现在我诗的每一页

雨下整夜我的爱溢出就像雨水

窗台蝴蝶像诗里纷飞的美丽章节

我接着写

把永远爱你写进诗的结尾

你是我唯一想要的了解

雨下整夜我的爱溢出就像雨水

院子落叶跟我的思念厚厚一叠

几句是非也无法将我的热情冷却

你出现在我诗的每一页

那饱满的稻穗幸福了这个季节

而你的脸颊像田里熟透的蕃茄

你突然对我说七里香的名字很美

我此刻却只想亲吻你倔强的嘴

雨下整夜我的爱溢出就像雨水

院子落叶跟我的思念厚厚一叠

几句是非也无法将我的热情冷却

你出现在我诗的每一页

整夜我的爱溢出就像雨水

窗台蝴蝶像诗里纷飞的美丽章节

我接着写

把永远爱你写进诗的结尾

你是我唯一想要的了解


进行中，非活动库存>0
	商品列表：原价划线、活动价、商品标签、直降活动标签
	活动列表：活动价、商品标签、直降活动标签
进行中，非活动库存=0
	商品列表：售罄
	活动列表：隐藏
	
	


未进行，非活动库存=0，未进入预热
未进行，非活动库存=0，未进入预热
未进行，非活动库存=0，预热中
	商品列表：原价、商品标签、限时折扣标签
	活动列表：活动价、商品标签、限时折扣标签

进行中，活动库存>0，有限购资格
进行中，活动库存>0，非活动库存>0，无限购资格
进行中，活动库存>0，非活动库存=0，无限购资格
进行中，活动库存=0，非活动库存>0
	商品列表：活动价、原价划线、商品标签、限时折扣标签
	活动列表：活动价、商品标签、限时折扣标签
	
进行中，活动库存=0，非活动库存=0
	商品列表：售罄
	活动列表：售罄



eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImRlOWNkZDRlLTM0YjctNTRiMC04NWM3LTdlZWM2NzA2MjgxOCIsInR5cGUiOiJ1c2VyIiwicm9sZXMiOiIiLCJleHAiOjE2MDQ1NTk3MzAwNjgsImlzcyI6ImFsbHJpZGUuYWkuaW5mcmEucmlkZXNoYXJpbmcifQ.bx0UIWaqaPyI1S3FNhe4NFAR3dqBotftLg_ft6eu5F4


//about.js
import { districtApis, tripApis, pickUpLocationApis } from '../../api/api'
Page({
  data: {
    hideEditUsernamePopup: true
  },
  async onLoad () {
    console.log("===================start=====================");
    let response = await districtApis.list()
    console.log(response);

    let response2 = await districtApis.getByLocation({
      latitude: 30.9510071,
      longitude: 121.4831638
    })
    console.log(response2);

    let response3 = await pickUpLocationApis.query({
      districtId: '8c95dbf9-4624-5d78-b951-dfe6f3b86546'
    })
    console.log(response3);
    console.log("===================end=====================");

    let response21 = await districtApis.getByLocation({
      latitude: 30.90686393,
      longitude: 121.92987652
    })
    console.log(response21, "response21");

    let response31 = await pickUpLocationApis.query({
      districtId: '9c21c474-1a77-5085-bd02-3288968084b9'
    })
    console.log(response31);

    // let response4 = await tripApis.create({
    //   start: '0e33e5f1-df39-5647-8ebc-8d3c377807f3',
    //   desPickupLocIds: ['09ffca6a-23eb-5101-bdba-90dfd02f1eb1', '6a0d4abe-e353-5e7c-9529-8c34d39dd65b', 'bd435e5a-7a1f-5125-afe3-3f011eb94c86'],
    //   destination: {
    //     name: '地铁16号线 滴水湖站',
    //     address: '上海地铁16号线 滴水湖站',
    //     location: {
    //       latitude: 30.91043752945474,
    //       longitude: 121.92457144681258
    //     }
    //   }
    // })
    // console.log(response4);

    // let resp5 = await tripApis.cancel()
    // console.log(resp5);
  },
  jumpPage (event) {
    switch (event.currentTarget.dataset.pagekey) {
      case 'order':
        wx.navigateTo({
          url: '/pages/about/order/order'
        })
        break;
      case 'username':
        this.setData({
          hideEditUsernamePopup: false
        })
        break;
      case 'feedback':
        wx.navigateTo({
          url: '/pages/about/feedback/feedback'
        })
        break;
    }
  },
  confirmEdit () {
    this.setData({
      hideEditUsernamePopup: true
    })
  }
})




    trip.start_destination = {
      address: "K11购物艺术中心",
      location: {
        latitude: 31.223495932,
        longitude: 121.473624036
      },
      name: "K11购物艺术中心"
    }