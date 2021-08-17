---
title: Day (daysOfMonthType) 元素
description: 指定執行工作的月份日期。
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Day 元素工作排程器
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c238ee5bd873c33f3acd2207ba9ad31869b151924dd20f082669b782d207c59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857951"
---
# <a name="day-daysofmonthtype-element"></a>Day (daysOfMonthType) 元素

指定執行工作的月份日期。

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

**Day** 元素是由 [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                            | 衍生自                                                               | 描述                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | 指定工作執行的當月天數。<br/> |



## <a name="examples"></a>範例

下列 XML 會定義每月日曆的日部分，其會在該月的1日和15日執行工作。


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





