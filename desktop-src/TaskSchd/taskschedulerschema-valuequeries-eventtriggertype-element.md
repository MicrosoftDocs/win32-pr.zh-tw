---
title: ValueQueries (eventTriggerType) 元素
description: 包含一系列的元素，其中每個專案都包含名稱和 XPath 查詢值。
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- ValueQueries 元素工作排程器
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fecf58696618f1f0f359754bc29aa10680dd1717fe55ffe9fc3e87d0b361b76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355341"
---
# <a name="valuequeries-eventtriggertype-element"></a>ValueQueries (eventTriggerType) 元素

包含一系列的元素，其中每個專案都包含名稱和 XPath 查詢值。 查詢會套用至從 [**訂**](taskschedulerschema-subscription-eventtriggertype-element.md) 用帳戶元素中指定之事件訂閱傳回的事件。 XPath 查詢值的名稱可用來做為工作的 [動作] 區段中的變數。

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

**ValueQueries** 元素是由 [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                      | 衍生自                                                                 | Description                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger (triggerGroup)**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | 指定在發生系統事件時啟動工作的觸發程式。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEventTrigger 的 ValueQueries 屬性**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries)。

如需腳本開發，請參閱 [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md)。

## <a name="examples"></a>範例

如需使用此專案指定事件觸發程式之工作的完整 XML 範例，請參閱 [事件觸發程式範例 (XML) ](/previous-versions//aa446889(v=vs.85))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

