---
title: SystemMonitor 的 OnDblClick 事件
description: 當使用者以滑鼠左鍵按兩下圖形線條、長條圖列或報表專案時，就會通知您。
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- OnDblClick 事件 SysMon
- OnDblClick 事件 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，OnDblClick 事件
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103836"
---
# <a name="systemmonitorondblclick-event"></a>SystemMonitor 的 OnDblClick 事件

當使用者以滑鼠左鍵按兩下圖形線條、長條圖列或報表專案時，就會通知您。

## <a name="syntax"></a>語法


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[in、out\]
</dt> <dd>

[**計數器**](counters.md)集合物件中所選取計數器的索引。 如果未選取任何計數器，則會傳回索引值 0;否則，會傳回所選計數器的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

觸發這個事件時，也會在 [圖例] 窗格中選取使用者在折線圖和長條圖中選取的計數器。 這可讓系統監視器的使用者更輕鬆地查看當顯示多個計數器值時所選取的計數器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



 

 





