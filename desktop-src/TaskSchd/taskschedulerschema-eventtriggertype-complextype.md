---
title: eventTriggerType 複雜類型
description: 定義 EventTrigger 元素的子項目和排序資訊。
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- eventTriggerType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0acd4bafa6033e461b69180862a8302e76f363b581d7f06b0812824f2031780b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612051"
---
# <a name="eventtriggertype-complex-type"></a>eventTriggerType 複雜類型

定義 [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) 元素的子項目和排序資訊。

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                           | 類型                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**延遲**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                | 指定事件發生時間和工作啟動時間之間的時間量。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**訂用帳戶**](taskschedulerschema-subscription-eventtriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | 指定 XPath 查詢，以識別引發觸發程式的事件。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md)      | 指定每個專案的序列，其中每個元素都包含名稱和 XPath 查詢值。 查詢會套用至從 [**訂**](taskschedulerschema-subscription-eventtriggertype-element.md) 用帳戶元素中指定之事件訂閱傳回的事件。 XPath 查詢值的名稱可做為工作的 [ [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md)動作] 區段中的 [ [**Body**](taskschedulerschema-body-showmessagetype-element.md) ] 元素中的變數。 <br/> |



## <a name="remarks"></a>備註

除了這裡定義的子項目之外， [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) 元素也會使用 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜類型所定義的子專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





