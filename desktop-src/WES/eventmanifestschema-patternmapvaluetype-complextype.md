---
title: PatternMapValueType 複雜類型
description: 未使用。 定義用來在訊息字串中尋找相符字串的正則運算式，並加以修改。
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- PatternMapValueType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc36564aefd4d2f3d19f3b216d785faad888612621386037ae0e5539ce511169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136161"
---
# <a name="patternmapvaluetype-complex-type"></a>PatternMapValueType 複雜類型

未使用。 定義用來在訊息字串中尋找相符字串的正則運算式，並加以修改。

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>屬性



| 名稱  | 類型   | 描述                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| NAME  | 字串 | 用來在訊息字串中尋找相符字串的正則運算式。<br/>                   |
| value | 字串 | 用來改變在訊息字串中找到之相符字串的正則運算式。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





