---
title: CounterItem 選取的屬性
description: 抓取或設定值，這個值會指出是否已選取計數器。
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- 選取的屬性 SysMon
- 選取的屬性 SysMon，CounterItem 物件
- CounterItem 物件 SysMon，選取的屬性
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e5cfcc65c54f882f10e87a0f2aaebad0e1a55c94b6581031b034799987bc6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956957"
---
# <a name="counteritemselected-property"></a>CounterItem 選取的屬性

抓取或設定值，這個值會指出是否已選取計數器。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>屬性值

如果已選取計數器，則為 True;否則為 false。

## <a name="remarks"></a>備註

您可以從計數器集合中選取一個或多個計數器。 選取計數器、選取圖例中的計數器、讓計數器顯示于圖例中，然後產生 [**OnCounterSelected**](-systemmonitor-oncounterselected.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





