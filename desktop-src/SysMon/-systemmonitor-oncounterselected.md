---
title: SystemMonitor. OnCounterSelected 事件
description: 在選取計數器時通知您。
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- OnCounterSelected 事件 SysMon
- OnCounterSelected 事件 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，OnCounterSelected 事件
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0174ab2f896a27e44df592ec28b7cb12a03198f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965496"
---
# <a name="systemmonitoroncounterselected-event"></a>SystemMonitor. OnCounterSelected 事件

在選取計數器時通知您。

## <a name="syntax"></a>語法


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

[**計數器**](counters.md)集合物件中所選取計數器的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

您可以在下列情況收到此事件

-   您將 [**CounterItem**](counteritem-selected.md) 設為 True
-   使用者選取圖例中的計數器
-   使用者按兩下圖例中的計數器

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor.OnCounterAdded**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**SystemMonitor.OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





