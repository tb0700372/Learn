# Question

## 库存管理

**问题**: 库存库位查询结果数量与实际不符(翻倍)  

**原因**: `ITEM_REG` 表内同一产品下存在多条注册证信息,且状态 `DFTFLG` 都是默认 `1`

**验证**:

```sql

WITH a AS
(
  SELECT B.ITEMID,Info=SUM(CAST(B.DFTFLG AS INT))
    FROM(SELECT ITEMID FROM ITEM_REG GROUP BY ITEMID HAVING COUNT(ITEMID)>1)A
    INNER JOIN(SELECT * FROM ITEM_REG)B ON B.ITEMID = A.ITEMID
  GROUP BY B.ITEMID
)SELECT * FROM a WHERE a.Info>1

```

**解决方法**:

相关产品数据交由质量人员更变产品注册信息默认值

## 入库管理

## 出库管理
