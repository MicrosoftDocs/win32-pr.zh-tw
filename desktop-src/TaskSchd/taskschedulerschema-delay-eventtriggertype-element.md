---
title: 延遲 (eventTriggerType) 元素
description: 指定事件發生時間和工作啟動時間之間的時間量。
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- Delay 元素工作排程器
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de1117ff4f7e0f823b1b213721521e1b526125bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965534"
---
# <a name="delay-eventtriggertype-element"></a>延遲 (eventTriggerType) 元素

指定事件發生時間和工作啟動時間之間的時間量。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。 如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

**Delay** 元素是由 [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                       | 衍生自                                                                 | Description                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | 指定在發生系統事件時啟動工作的觸發程式。<br/> |



## <a name="remarks"></a>備註

針對腳本開發，事件觸發程式延遲是由 [**EventTrigger**](eventtrigger-delay.md) 屬性所指定。

針對 c + + 開發，事件觸發程式延遲是由 [**IEventTrigger：:D elay**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) 屬性所指定。

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

 

 





