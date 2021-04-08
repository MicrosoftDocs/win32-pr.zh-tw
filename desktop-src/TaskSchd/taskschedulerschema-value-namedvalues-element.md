---
title: 值 (namedValues) 元素
description: 包含與名稱/值配對中的名稱相關聯的值。
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- 值元素工作排程器
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686362"
---
# <a name="value-namedvalues-element"></a>值 (namedValues) 元素

包含與名稱/值配對中的名稱相關聯的值。

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

**Value** 元素是由 [**namedValues**](taskschedulerschema-namedvalues-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                              | 衍生自                                                       | Description                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ValueQueries (eventTriggerType)**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md) | 指定命名的 XPath 查詢集合。 集合中的每個查詢都會套用至從 [**訂**](taskschedulerschema-subscription-eventtriggertype-element.md) 用帳戶元素中指定之訂閱查詢傳回的最後一個相符事件 XML。 查詢的名稱可以當做 ShowMessage 動作訊息中的變數使用。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**ITaskNamedValuePair 的 Value 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value)。

如需腳本開發，請參閱 [**TaskNamedValuePair。**](tasknamedvaluepair-value.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





