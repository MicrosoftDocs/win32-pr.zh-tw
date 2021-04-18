---
title: QueryListType 複雜類型
description: 定義查詢清單，其中可包含一組選取器和 suppressors，用來在結果集中包含或排除事件。
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- QueryListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968761"
---
# <a name="querylisttype-complex-type"></a>QueryListType 複雜類型

定義查詢清單，其中可包含一組選取器和 suppressors，用來在結果集中包含或排除事件。

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                  | 類型                                                   | Description                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**查詢**](queryschema-query-querylisttype-element.md) | [**QueryType**](queryschema-querytype-complextype.md) | 定義一組選取器和 suppressors，用來在結果集中包含或排除事件。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





