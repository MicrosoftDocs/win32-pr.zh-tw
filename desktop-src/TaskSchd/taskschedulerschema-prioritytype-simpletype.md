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
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025339"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構簡單類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





