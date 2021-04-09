---
title: ScheduleByDay (calendarTriggerType) 元素
description: 指定每日排程。
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- XML 元素工作排程器每日觸發程式
- ScheduleByDay 元素工作排程器
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934866"
---
# <a name="schedulebyday-calendartriggertype-element"></a>ScheduleByDay (calendarTriggerType) 元素

指定每日排程。 例如，工作會在每天上午8:00、每天、每隔三天開始，依此類推。

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

**ScheduleByDay** 元素是由 [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                             | 衍生自                                                                       | Description                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | 指定每日、每週、每月或每週 (DOW) 觸發程式。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                            | 類型             | Description                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | **unsignedByte** | 指定排程中天數之間的間隔。<br/> |



## <a name="remarks"></a>備註

先前所列的子項目是由 [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) 複雜元素類型所定義。

工作開始的當日時間是由 [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) 元素設定。

針對開發腳本，會使用 [**DailyTrigger**](weeklytrigger.md) 物件指定每日觸發程式。

針對 c + + 開發，會使用 [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) 介面指定每日觸發程式。

## <a name="examples"></a>範例

下列 XML 會定義每日啟動工作的每日行事曆觸發程式。


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



如需指定每日排程之工作的 XML 完整範例，請參閱 [ (XML) 的每日觸發程式範例 ](daily-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





