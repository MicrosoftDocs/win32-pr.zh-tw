---
title: 計數器。 Remove 方法
description: 從集合中移除 CounterItem 實例。
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- 移除方法 SysMon
- Remove 方法 SysMon，計數器類別
- 計數器類別 SysMon，Remove 方法
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934245"
---
# <a name="countersremove-method"></a>計數器。 Remove 方法

從集合中移除 [**CounterItem**](counteritem.md) 實例。

## <a name="syntax"></a>語法


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

要從集合中移除之 [**CounterItem**](counteritem.md) 物件的索引。 索引是以一為基礎。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="exceptions"></a>例外狀況



| 例外狀況類型                                  | 條件                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| **System.runtime.interopservices.outattribute. COMException** | 指定的索引無效。 Err 值為???。 |



 

## <a name="remarks"></a>備註

若要從集合中移除所有計數器，您可以呼叫 [**SystemMonitor。**](systemmonitor-reset.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**計數器**](counters.md)
</dt> <dt>

[**SystemMonitor 重設**](systemmonitor-reset.md)
</dt> </dl>

 

 





