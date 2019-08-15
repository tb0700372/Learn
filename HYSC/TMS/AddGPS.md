# GPS 绑定温度计

```sql
select * from TMF_GPS where SHIPMENTID='1207169891'


select * from TMF_GPS where DEVICEID='Y0004ELJ'

-- update TMF_GPS set TT='25',TB='2' where SHIPMENTID='1207169891' and DEVICEID='Y0004EEL'

INSERT INTO [JYLTMS].[dbo].[TMF_GPS]
      (
      [SHIPMENTID]       -- 订单号
      ,[DEVICEID]        -- 温度计编号
      ,[TT]              -- 温度上限
      ,[TB]              -- 温度下限
      ,[LOGTIME]         -- 提货时间
      ,[SHIPMENTIDREF]   -- 单号
      ,[PODFLG]          -- 默认0
      ,[LASTUPDATE]      -- 升级时间
      )
VALUES
      (
      '1207169891'
      ,'Y0004EEL'
      ,'-20'
      ,'-80'
      ,'2019-08-13 17:00'
      ,'1207169891'
      ,'0'
      ,GETDATE()
      )
GO
```
