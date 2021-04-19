---
title: CounterItem。 Value 屬性
description: 抓取計數器的最後取樣值。
ms.assetid: c5aeaa00-e185-484d-8a7a-d45a21690e20
keywords:
- 值屬性 SysMon
- Value 屬性 SysMon，CounterItem 類別
- CounterItem 類別 SysMon，Value 屬性
topic_type:
- apiref
api_name:
- CounterItem.Value
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c0d6bd9e1751e34c980bc95f790314017eeb49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968167"
---
# <a name="counteritemvalue-property"></a>CounterItem。 Value 屬性

抓取計數器的最後取樣值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property Value As Double
```



## <a name="property-value"></a>屬性值

計數器的上次取樣值。 如果發生錯誤，此值為-1。

## <a name="remarks"></a>備註

這是 [**CounterItem**](counteritem.md) 物件的預設屬性。

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

[**CounterItem**](counteritem-getvalue.md)
</dt> </dl>

 

 





