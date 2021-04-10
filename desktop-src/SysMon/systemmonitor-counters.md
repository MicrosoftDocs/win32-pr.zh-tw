---
title: SystemMonitor 計數器屬性
description: 抓取包含 CounterItem 物件集合的計數器。
ms.assetid: eab21e1f-c8fb-474c-83e3-5ef56483d525
keywords:
- 計數器屬性 SysMon
- 計數器屬性 SysMon，SystemMonitor 類別
- SystemMonitor 類別 SysMon，計數器屬性
topic_type:
- apiref
api_name:
- SystemMonitor.Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e09cc797c09033e90ba4d584ee63336a52cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103991"
---
# <a name="systemmonitorcounters-property"></a>SystemMonitor 計數器屬性

抓取包含 [**CounterItem**](counteritem.md)物件集合的 **計數器**。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property Counters As ICounters
```



## <a name="property-value"></a>屬性值

包含 [**CounterItem**](counteritem.md)物件集合的 **計數器** 物件。

## <a name="remarks"></a>備註

這是 [**SystemMonitor**](systemmonitor.md) 物件的預設屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





