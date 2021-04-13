---
title: TimeTrigger (triggerGroup) 元素
description: 指定啟動觸發程式時啟動工作的觸發程式。
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- TimeTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466272"
---
# <a name="timetrigger-triggergroup-element"></a>TimeTrigger (triggerGroup) 元素

指定啟動觸發程式時啟動工作的觸發程式。

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

**TimeTrigger** 元素是由 [**triggerGroup**](taskschedulerschema-triggergroup-group.md)定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | Description                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**觸發程序**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | 指定啟動工作的觸發程式。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                                        | 類型                                                                     | Description                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**已啟用 (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | 指定啟用觸發程序。<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | 指定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | 指定觸發程式可啟動工作的最大時間量。<br/>                                   |
| [**重複 (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | 指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | 指定啟動觸發程式的日期和時間。 這個元素是必要的。<br/>                                    |



## <a name="attributes"></a>屬性



| 名稱 | 類型       | Description                               |
|------|------------|-------------------------------------------|
| 識別碼   | **string** | 觸發程式的識別碼。<br/> |



## <a name="remarks"></a>備註

[**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)元素是時間和行事曆觸發程式的必要元素， (**TimeTrigger** 和 [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)) 。

針對開發腳本，會使用 [**TimeTrigger**](timetrigger.md) 物件來指定時間觸發程式。

針對 c + + 開發，會使用 [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) 介面來指定時間觸發程式。

上方所列的子專案是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜元素類型所定義。 這些專案必須加入如下所示的順序中。

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**已啟用 (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**重複 (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a>範例

如需指定時間觸發程式之 XML 的完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





