V2.3.0
/v1/orders/member-discount-summary          获取会员省钱记录概览
/v1/orders/member-discount-list                     获取会员省钱记录列表

有关会员折扣商品相关的API --
1. /query- 参数加了isMemberGoods， 返回值加了 is_member_goods
2. 其他详情相关的API 加了这个返回值memberGoods， 如果有API漏加了或者缺失信息， 我们再单独加上

获取会员商品折扣价的逻辑（PC）
1. /v1/member-product/general-discount - 获取会员商品折扣率：memberDiscount- 会员折扣；memberAdditionalDiscount-折上折
2. 判断当前商品是否参加活动(直降，限时折扣)
3. 若参加活动，则会员商品折扣价 = 活动价 * 折上折
4. 若没有参加活动， 则会员商品折扣价 = 原价 * 会员折扣



36企业购：
SELECT x.* FROM enterprise_purchase.labour_union x
WHERE id in (82,117,140,141)

SELECT x.* FROM enterprise_purchase.welfare_area x
WHERE labour_union_id in (82,117,140,141)

SELECT x.* FROM enterprise_purchase.goods x
WHERE goods_name like '%tf%'

SELECT x.* FROM enterprise_purchase.goods_spec_new x
WHERE goods_id in (82,83,109,110,112,114,353,373)

SELECT x.* FROM enterprise_purchase.cart x
WHERE employee_id = 5819 and is_deleted = 0

select distinct edb_produce_bar_code, erp_stock from enterprise_purchase.goods_spec_new where erp_stock > 0;


QA企业购：
SELECT x.* FROM enterprise_purchase.labour_union x
WHERE id in (1,30,63,64)

SELECT x.* FROM enterprise_purchase.welfare_area x
WHERE labour_union_id in (1,30,63,64)

SELECT x.* FROM enterprise_purchase.goods_spec_new x
WHERE goods_id in (26,27,29,378)