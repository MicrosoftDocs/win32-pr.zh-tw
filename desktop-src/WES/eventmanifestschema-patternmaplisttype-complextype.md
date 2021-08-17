---
title: PatternMapListType 複雜類型
description: 未使用。 定義用來改變訊息字串的正則運算式組清單。
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- PatternMapListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbf96f7033f353662578e477fb8e35e0bfcda6db390f6492e29840e5e1faa5cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136201"
---
# <a name="patternmaplisttype-complex-type"></a>PatternMapListType 複雜類型

未使用。 定義用來改變訊息字串的正則運算式組清單。

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                         | 類型                                                                     | 描述                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**patternMap**](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [**PatternMapType**](eventmanifestschema-patternmaptype-complextype.md) | 定義兩個正則運算式之間的對應。 其中一個運算式可用來在訊息字串中尋找相符的字串，而另一個運算式則是用來在服務將字串放回訊息字串之前變更字串。 使用符合的第一個模式對應，且不會嘗試其他模式。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





