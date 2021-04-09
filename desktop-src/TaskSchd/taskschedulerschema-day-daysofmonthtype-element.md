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
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024824"
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



| 元素                                                                            | 衍生自                                                               | Description                                                            |
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





