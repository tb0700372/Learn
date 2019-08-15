# UserScanRole

```sql
TABLE SEC_USERCLIENT
 PROC spWebRpt_ALL_ShipTrack
```

| USERID     | USERCLIENTID | AUTOID |
|------------|--------------|--------|
| siemens_od | XMZ          | 1      |

>> 添加表 `SEC_USERCLIENT` 与相关值

```json
      USERID : 用户标识
USERCLIENTID : 客户ID
      AUTOID : 自动增长序号
```

| USERID     | USERCLIENTID | AUTOID |
|------------|--------------|--------|
| siemens_od | XMZ          | 1      |

>> 修改存储过程 `spWebRpt_ALL_ShipTrack`

功能添加

```sql
--No.20190802111834
  DECLARE @USERCLIENT TABLE(USERCLIENTID VARCHAR(30))
  IF EXISTS(SELECT * FROM SEC_USERCLIENT WHERE USERID=@UserID)
    INSERT @USERCLIENT
    SELECT USERCLIENTID FROM dbo.SEC_USERCLIENT WHERE USERID=@UserID
  ELSE
    INSERT @USERCLIENT
      SELECT CUSTOMER FROM #TEMP_QUERY
-- 结果增加条件判断
  WHERE CUSTOMER IN (SELECT * FROM @USERCLIENT)
```

补充:
&emsp;本功能仅在为 SEC_USERCLIENT 表内插入用户与用户对应的客户ID后生效, 添加后进能查看对应客户ID的信息
