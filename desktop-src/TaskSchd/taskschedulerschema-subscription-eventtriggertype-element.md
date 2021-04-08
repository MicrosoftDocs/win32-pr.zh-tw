---
title: 訂用帳戶 (eventTriggerType) 元素
description: 指定 XPath 查詢，以識別引發觸發程式的事件。
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- 訂用帳戶元素工作排程器
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686560"
---
# <a name="subscription-eventtriggertype-element"></a>訂用帳戶 (eventTriggerType) 元素

指定 XPath 查詢，以識別引發觸發程式的事件。

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

**訂** 用帳戶元素是由 [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)複雜型別所定義。

## <a name="parent-element"></a>父元素



| 元素                                                                       | 衍生自                                                                 | Description                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | 指定在發生系統事件時啟動工作的觸發程式。<br/> |



## <a name="remarks"></a>備註

針對腳本開發，事件訂閱是由 [ [**EventTrigger**](eventtrigger-subscription.md) ] 屬性所指定。

針對 c + + 開發，事件訂閱是由 [**IEventTrigger：：訂**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) 用帳戶屬性所指定。

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

 

 





