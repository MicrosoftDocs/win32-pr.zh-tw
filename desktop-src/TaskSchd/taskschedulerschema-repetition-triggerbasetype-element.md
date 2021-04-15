---
title: 重複 (triggerBaseType) 元素
description: 指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- 重複元素工作排程器
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ebd6f9f77998e5e975e24ff752a475e3880c0aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466016"
---
# <a name="repetition-triggerbasetype-element"></a>重複 (triggerBaseType) 元素

指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

**重複** 專案是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md)複雜型別定義。

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



## <a name="child-elements"></a>子元素



| 元素                                                                                   | 類型     | Description                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [**時間**](taskschedulerschema-duration-repetitiontype-element.md)                   | duration | 指定重複模式的時間長度。<br/>                                                              |
| [**間隔**](taskschedulerschema-interval-repetitiontype-element.md)                   | duration | 指定工作每次重新開機之間的時間量。<br/>                                           |
| [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | boolean  | 指定在重複模式期間結束時停止執行中的工作實例。<br/> |



## <a name="remarks"></a>備註

如果您指定工作的重複持續時間，您也必須指定重複間隔。

如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動五次。 您可以使用下列模式來定義五次重複。

1.  工作會在第一分鐘的開頭開始。
2.  下一項工作會在第一分鐘結束時啟動。
3.  下一項工作會在第二分鐘結束時啟動。
4.  下一項工作會從第三分鐘的結尾開始。
5.  下一項工作會在第四分鐘結束時啟動。

**Windows Server 2003、WINDOWS XP 和 windows 2000：** 如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動四次。

**Windows Vista、windows 7、Windows server 2008、Windows 8 和 Windows server 2012：** 通常，將重複期間設定為間隔的確切倍數，會產生上面所述的數位。 不過，在某些繁重的負載狀況下，可能會在 TaskScheduler 可以啟動最後工作間隔之前，讓持續時間超時。

針對開發腳本，會使用觸發程式來指定重複模式。所有觸發程式物件都會繼承 [**重複**](trigger-repetition.md) 的屬性。

若是 c + + 開發，則會使用所有觸發程式介面所繼承的 [**ITRigger：：重複**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) 屬性來指定重複模式。

## <a name="examples"></a>範例

下列 XML 會定義一個開機觸發程式元素，以指定觸發程式的重複模式。


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
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

 

 





