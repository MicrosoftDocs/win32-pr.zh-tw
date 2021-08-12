---
title: triggersType 複雜類型
description: 定義所有觸發程式元素的群組 (triggerGroup) 。
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- triggersType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c2bd6fa4011841958ad08239640024f9878528aecb1307487c3354ac74e31db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610535"
---
# <a name="triggerstype-complex-type"></a>triggersType 複雜類型

定義所有觸發程式元素的群組 ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) 。 [**TriggerGroup**](taskschedulerschema-triggergroup-group.md)群組包含可在工作中使用的觸發程式清單。

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





