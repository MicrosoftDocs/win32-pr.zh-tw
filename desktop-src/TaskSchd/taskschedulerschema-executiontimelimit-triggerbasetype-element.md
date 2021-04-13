---
title: ExecutionTimeLimit (triggerBaseType) 元素
description: 指定觸發程式可啟動工作的最大時間量。
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- ExecutionTimeLimit 元素工作排程器
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbe56fb0431ab109b1a19030ae6ba20af55492ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466285"
---
# <a name="executiontimelimit-triggerbasetype-element"></a>ExecutionTimeLimit (triggerBaseType) 元素

指定觸發程式可啟動工作的最大時間量。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。 如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

**ExecutionTimeLimit** 元素是由 [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md)複雜型別定義。

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

針對開發腳本，會使用所有觸發程式物件所繼承的 [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) 屬性來指定執行時間限制。

若是 c + + 開發，則會使用所有觸發程式介面所繼承的 [**ITrigger：： ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) 屬性來指定執行時間限制。

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

 

 





