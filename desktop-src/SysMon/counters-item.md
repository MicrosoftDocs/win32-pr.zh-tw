---
title: 計數器。 Item 屬性
description: 從集合中抓取指定的 CounterItem 實例。
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- 專案屬性 SysMon
- Item 屬性 SysMon，計數器類別
- 計數器類別 SysMon，Item 屬性
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464713"
---
# <a name="countersitem-property"></a>計數器。 Item 屬性

從集合中抓取指定的 [**CounterItem**](counteritem.md) 實例。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a>屬性值

對應至指定之索引值的 [**CounterItem**](counteritem.md)實例。

## <a name="exceptions"></a>例外狀況



| 例外狀況類型                                  | 條件                         |
|-------------------------------------------------|-----------------------------------|
| **System.runtime.interopservices.outattribute. COMException** | 指定的索引無效。 |



 

## <a name="remarks"></a>備註

這是 [**計數器**](counters.md) 物件的預設屬性。

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

[**計數器**](counters.md)
</dt> </dl>

 

 





