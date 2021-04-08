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
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685465"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





