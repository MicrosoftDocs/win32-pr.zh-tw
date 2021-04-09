---
title: CounterItem. GetStatistics 方法
description: 抓取計數器的平均值、最大值和最小值。
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- GetStatistics 方法 SysMon
- GetStatistics 方法 SysMon、CounterItem 類別
- CounterItem 類別 SysMon，GetStatistics 方法
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934504"
---
# <a name="counteritemgetstatistics-method"></a>CounterItem. GetStatistics 方法

抓取計數器的平均值、最大值和最小值。

## <a name="syntax"></a>語法


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*最大值* \[擴展\]
</dt> <dd>

計數器的最大值。

</dd> <dt>

*最小值* \[擴展\]
</dt> <dd>

計數器的最小值。

</dd> <dt>

*平均* \[擴展\]
</dt> <dd>

計數器的平均值。

</dd> <dt>

*狀態* \[擴展\]
</dt> <dd>

指出值是否有效。



| 值                                                                                              | 意義                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>0</dt> </dl>                       | 值有效。<br/>     |
| <dl> <dt>0xC0000BBA (3221228474) </dt> </dl> | 值無效。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

只有在圖形視窗中顯示的計數器值會用來計算統計值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**CounterItem.GetDataAt**](counteritem-getdataat.md)
</dt> <dt>

[**CounterItem**](counteritem-getvalue.md)
</dt> </dl>

 

 





