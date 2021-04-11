---
title: weekType 簡單類型
description: 定義可以在 Week 元素中使用的值。
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- weekType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6513efe0fe0ef4fcbf6b849627d09ec9da6feb82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094227"
---
# <a name="weektype-simple-type"></a>weekType 簡單類型

定義可以在 [**Week**](taskschedulerschema-week-weekstype-element.md) 元素中使用的值。

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**WeekType** 簡單類型是以下列模式限制的 **字串**：

-   `[1-4]|Last`

    指定月中第四周的第一個 (1-4) 或一律是當月的最後一周。

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

 

 





