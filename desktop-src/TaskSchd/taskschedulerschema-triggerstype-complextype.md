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
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968800"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





