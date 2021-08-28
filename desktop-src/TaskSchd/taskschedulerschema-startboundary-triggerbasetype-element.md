---
title: StartBoundary (triggerBaseType) 元素
description: 指定啟動觸發程式的日期和時間。
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- StartBoundary 元素工作排程器
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46584659fbd14bc26981e220798a91c03e960e1f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886419"
---
# <a name="startboundary-triggerbasetype-element"></a>StartBoundary (triggerBaseType) 元素

指定啟動觸發程式的日期和時間。

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

**StartBoundary** 元素是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                     | 衍生自                                                                               | 說明                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | 指定啟動系統時啟動工作的觸發程式。<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | 指定每日、每週、每月或每週 (DOW) 觸發程式。<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | 指定在發生系統事件時啟動工作的觸發程式。<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | 指定當電腦進入閒置狀態時啟動工作的觸發程式。<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | 指定當使用者登入時啟動工作的觸發程式。<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | 指定在註冊工作時啟動工作的觸發程式。<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | 指定啟動觸發程式時啟動工作的觸發程式。<br/>             |



## <a name="remarks"></a>備註

**&lt; StartBoundary &gt;** 元素是時間和行事曆觸發程式的必要元素， ([**&lt; TimeTrigger &gt;**](taskschedulerschema-timetrigger-triggergroup-element.md)和 [**&lt; CalendarTrigger &gt;**](taskschedulerschema-calendartrigger-triggergroup-element.md)) 。

針對開發腳本，會使用所有觸發程式物件所繼承的 [**StartBoundary**](trigger-startboundary.md) 屬性來指定結束界限。

若是 c + + 開發，則會使用所有觸發程式介面所繼承的 [**ITrigger：： StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) 屬性來指定結束界限。

## <a name="examples"></a>範例

下列 XML 定義的開機觸發程式元素會定義2005年1月1日的起始界限： 8:00 AM。


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



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

 

 





