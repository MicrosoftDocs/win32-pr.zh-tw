---
title: priorityType 簡單類型
description: 定義 Priority (settingsType) 元素的最小值和最大值。
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- priorityType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 71bdf8b87a641247ce2064ccf44ee861d79aab0593229e4cd7b38035c5c7c124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424428"
---
# <a name="prioritytype-simple-type"></a>priorityType 簡單類型

定義 [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) 元素的最小值和最大值。

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>列舉值

**PriorityType** 簡單類型會定義下列值。



| 值 | 描述                         |
|-------|-------------------------------------|
| 0     | 允許的最小整數。<br/> |
| 10    | 允許的最大整數。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構簡單類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





