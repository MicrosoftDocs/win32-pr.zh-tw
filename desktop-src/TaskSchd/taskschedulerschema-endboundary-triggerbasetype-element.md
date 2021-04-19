---
title: EndBoundary (triggerBaseType) 元素
description: 指定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- EndBoundary 元素工作排程器
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d687655498301595c1ab888fcc179ec0694f0aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969757"
---
# <a name="endboundary-triggerbasetype-element"></a>EndBoundary (triggerBaseType) 元素

指定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

**EndBoundary** 元素是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                     | 衍生自                                                                               | Description                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | 指定啟動系統時啟動工作的觸發程式。<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | 指定每日、每週、每月或每週 (DOW) 觸發程式。<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | 指定在發生系統事件時啟動工作的觸發程式。<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | 指定當電腦進入閒置狀態時啟動工作的觸發程式。<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | 指定當使用者登入時啟動工作的觸發程式。<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | 指定在註冊工作時啟動工作的觸發程式。<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | 指定啟動觸發程式時啟動工作的觸發程式。<br/>             |



## <a name="remarks"></a>備註

針對開發腳本，會使用所有觸發程式物件所繼承的 [**EndBoundary**](trigger-endboundary.md) 屬性來指定結束界限。

若是 c + + 開發，則會使用所有觸發程式介面所繼承的 [**ITrigger：： EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) 屬性來指定結束界限。

## <a name="examples"></a>範例

下列 XML 定義的開機觸發程式元素，定義2007年1月1日的結束界限： 8:00 AM。


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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





