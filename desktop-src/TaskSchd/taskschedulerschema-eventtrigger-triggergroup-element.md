---
title: EventTrigger (triggerGroup) 元素
description: 指定在發生系統事件時啟動工作的觸發程式。
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- 事件觸發程式工作排程器，元素
- EventTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 555c8683933b2242d119fc00f29c6d0a33188f6404ca48a00e8a127dd59aa791
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424468"
---
# <a name="eventtrigger-triggergroup-element"></a>EventTrigger (triggerGroup) 元素

指定在發生系統事件時啟動工作的觸發程式。

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

**EventTrigger** 元素是由 [**triggerGroup**](taskschedulerschema-triggergroup-group.md)定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | 描述                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**觸發程序**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | 指定啟動工作的觸發程式。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                              | 類型                                                                     | 描述                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**延遲 (eventTriggerType)**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                 | 指定事件發生時間和工作啟動時間之間的時間量。<br/>                                |
| [**已啟用 (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)             | boolean                                                                  | 指定啟用觸發程序。<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)     | dateTime                                                                 | 指定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/> |
| [**重複 (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)       | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | 指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md) | dateTime                                                                 | 指定啟動觸發程式的日期和時間。<br/>                                                              |
| [**訂用帳戶 (eventTriggerType)**](taskschedulerschema-subscription-eventtriggertype-element.md) | string                                                                   | 指定 XPath 查詢，以識別引發觸發程式的事件。<br/>                                             |



## <a name="attributes"></a>屬性



| 名稱 | 類型 | 描述                           |
|------|------|---------------------------------------|
| 識別碼   | 識別碼   | 觸發程式的識別碼。<br/> |



## <a name="remarks"></a>備註

您可以建立最多500個具有事件訂閱的工作。 針對各種事件進行查詢的事件訂閱，可以用來觸發使用相同動作來回應所記錄事件的工作。

針對腳本開發，事件觸發程式是由 [**EventTrigger**](eventtrigger.md) 物件所定義。

針對 c + + 開發，事件觸發程式是由 [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) 介面所定義。

## <a name="examples"></a>範例

如需使用事件觸發程式之 XML 的完整範例，請參閱 [事件觸發程式範例 (xml) ](/previous-versions//aa446889(v=vs.85))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

