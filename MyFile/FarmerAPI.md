V2.3.0
/v1/orders/member-discount-summary          ��ȡ��ԱʡǮ��¼����
/v1/orders/member-discount-list                     ��ȡ��ԱʡǮ��¼�б�

�йػ�Ա�ۿ���Ʒ��ص�API --
1. /query- ��������isMemberGoods�� ����ֵ���� is_member_goods
2. ����������ص�API �����������ֵmemberGoods�� �����API©���˻���ȱʧ��Ϣ�� �����ٵ�������

��ȡ��Ա��Ʒ�ۿۼ۵��߼���PC��
1. /v1/member-product/general-discount - ��ȡ��Ա��Ʒ�ۿ��ʣ�memberDiscount- ��Ա�ۿۣ�memberAdditionalDiscount-������
2. �жϵ�ǰ��Ʒ�Ƿ�μӻ(ֱ������ʱ�ۿ�)
3. ���μӻ�����Ա��Ʒ�ۿۼ� = ��� * ������
4. ��û�вμӻ�� ���Ա��Ʒ�ۿۼ� = ԭ�� * ��Ա�ۿ�



36��ҵ����
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


QA��ҵ����
SELECT x.* FROM enterprise_purchase.labour_union x
WHERE id in (1,30,63,64)

SELECT x.* FROM enterprise_purchase.welfare_area x
WHERE labour_union_id in (1,30,63,64)

SELECT x.* FROM enterprise_purchase.goods_spec_new x
WHERE goods_id in (26,27,29,378)