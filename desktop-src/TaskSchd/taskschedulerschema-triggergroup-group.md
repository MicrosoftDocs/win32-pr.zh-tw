---
title: triggerGroup 群組
description: 定義觸發程式群組。
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- triggerGroup 工作排程器
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74ae14f6e22245e49b2c2d0136fd297b35c9c5ed1f5126cc0914e97f42c8488f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610999"
---
# <a name="triggergroup-group"></a>triggerGroup 群組

定義觸發程式群組。

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                                 | 類型                                                                                                   | 描述                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                             | 啟動系統時啟動工作的觸發程式。<br/>                                                |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)                     | 根據每日、每週、每月或每月星期幾啟動工作的觸發程式 (DOW) 排程。<br/> |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)                           | 當系統事件發生時啟動工作的觸發程式。<br/>                                               |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                             | 當電腦進入閒置狀態時啟動工作的觸發程式。<br/>                                |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)                           | 當使用者登入時啟動工作的觸發程式。<br/>                                                      |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)             | 在註冊工作時啟動工作的觸發程式。<br/>                                              |
| [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | 當終端機伺服器會話變更狀態時，啟動工作的觸發程式。<br/>                             |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                             | 啟動觸發程式時啟動工作的觸發程式。<br/>                                            |



## <a name="remarks"></a>備註

讀取或寫入 XML 時，此群組所定義的元素是 [**觸發**](taskschedulerschema-triggers-tasktype-element.md) 程式元素的子項目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





