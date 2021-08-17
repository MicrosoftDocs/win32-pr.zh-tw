---
title: WeeksType) 元素 (周
description: 指定當月的特定周。
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Week 元素工作排程器
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a999eaa5ec7d4ed36b86fc292f4c0d5e8c474fd1df8f5f4b9da5b90f2dcca641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758204"
---
# <a name="week-weekstype-element"></a>WeeksType) 元素 (周

指定當月的特定周。

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

Week 元素是由 [**weeksType**](taskschedulerschema-weekstype-complextype.md)複雜型 **別** 定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                                        | 衍生自                                                   | 描述                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MonthlyDayOfWeekScheduleType)  (周**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [**weeksType**](taskschedulerschema-weekstype-complextype.md) | 指定執行工作的月份周數。<br/> |



## <a name="remarks"></a>備註

指定月中的周數時，請在當月的前四個星期使用數位1-4，或使用 "Last" 字串來指出當月的最後一周。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





