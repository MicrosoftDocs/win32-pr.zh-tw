---
title: dayOfMonthType 簡單類型
description: 定義指定月份日期的可能值。
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- dayOfMonthType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a8428688ff429809c7509bae42adb156efe00ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508392"
---
# <a name="dayofmonthtype-simple-type"></a>dayOfMonthType 簡單類型

定義指定月份日期的可能值。

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**DayOfMonthType** 簡單類型是以下列模式限制的 **字串**：

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    指定一個月的第1個到第31天，或一律是當月的最後一天。

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

 

 





