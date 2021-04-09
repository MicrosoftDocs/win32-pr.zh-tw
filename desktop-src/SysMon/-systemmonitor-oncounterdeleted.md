---
title: SystemMonitor. OnCounterDeleted 事件
description: 從計數器集合刪除計數器之前通知您。
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- OnCounterDeleted 事件 SysMon
- OnCounterDeleted 事件 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，OnCounterDeleted 事件
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934429"
---
# <a name="systemmonitoroncounterdeleted-event"></a>SystemMonitor. OnCounterDeleted 事件

從 [**計數器**](counters.md) 集合刪除計數器之前通知您。

## <a name="syntax"></a>語法


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

要從 [**計數器**](counters.md) 集合物件中刪除之計數器的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

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

[**SystemMonitor.OnCounterSelected**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





