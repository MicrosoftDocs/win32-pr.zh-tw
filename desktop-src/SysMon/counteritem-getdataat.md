---
title: CounterItem. GetDataAt 方法
description: 從圖形中的特定點抓取指定的計數器值。
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- GetDataAt 方法 SysMon
- GetDataAt 方法 SysMon，CounterItem 物件
- CounterItem 物件 SysMon，GetDataAt 方法
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508671"
---
# <a name="counteritemgetdataat-method"></a>CounterItem. GetDataAt 方法

從圖形中的特定點抓取指定的計數器值。

## <a name="syntax"></a>語法


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

您要取得其值之圖形點的以零為基底的索引。 有效值的範圍是從0到 ([**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md) -1) 。

</dd> <dt>

*哪* \[ 一個在\]
</dt> <dd>

要抓取的計數器數值型別，例如，在圖形視窗中顯示的計數器平均值。 如需可能的值，請參閱 [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)。

</dd> <dt>

*變異* \[擴展\]
</dt> <dd>

已取出的計數器值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

只有在下列情況下才使用這個方法

-   [**SystemMonitor**](systemmonitor-displaytype.md) 會設定為 sysmonLineGraph
-   [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) 設定為 SysmonLogFiles 或 sysmonSqlLog

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**CounterItem.GetStatistics**](counteritem-getstatistics.md)
</dt> <dt>

[**CounterItem**](counteritem-getvalue.md)
</dt> </dl>

 

 





