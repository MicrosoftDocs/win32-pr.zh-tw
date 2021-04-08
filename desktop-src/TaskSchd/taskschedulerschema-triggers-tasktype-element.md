---
title: 觸發程式 (taskType) 元素
description: 指定啟動工作的觸發程式。
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- 觸發程式元素工作排程器
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06994c395fbfbc5b0c6244c9d17930bc4afac885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686555"
---
# <a name="triggers-tasktype-element"></a>觸發程式 (taskType) 元素

指定啟動工作的觸發程式。

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

**觸發** 程式元素是由 [**triggersType**](taskschedulerschema-triggerstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                          | 衍生自                                                 | Description                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | 定義工作排程器服務所執行的工作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                     | 類型                                                                                       | Description                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | 指定啟動系統時啟動工作的觸發程式。<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | 指定每日、每週、每月或每週 (DOW) 觸發程式。<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | 指定在發生系統事件時啟動工作的觸發程式。<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | 指定當電腦進入閒置狀態時啟動工作的觸發程式。<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | 指定當使用者登入時啟動工作的觸發程式。<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | 指定在註冊工作時啟動工作的觸發程式。<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | 指定啟動觸發程式時啟動工作的觸發程式。<br/>             |



## <a name="remarks"></a>備註

您可以依任何順序加入上列的子項目。

針對 c + + 開發，會使用 [**ITaskDefinition 的 trigger 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers)來指定工作的觸發程式。

針對開發腳本，會使用 [**TaskDefinition**](taskdefinition-triggers.md) 屬性來指定工作的觸發程式。

## <a name="examples"></a>範例

如需指定觸發程式之工作的完整 XML 範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。

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

 

 





