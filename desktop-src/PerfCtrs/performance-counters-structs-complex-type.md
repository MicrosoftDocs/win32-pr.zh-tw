---
description: 定義包含計數器值的結構清單。
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: 結構複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0dfa7f72ee537d857f19301aa4df906d94b0bf7ba9e3f7a76bdb6ab82c84dfd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314418"
---
# <a name="structs-complex-type"></a>結構複雜類型

定義包含計數器值的結構清單。

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素    | 類型                                                           | Description                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| **結構** | [**man： struct**](performance-counters-struct-complex-type.md) | 包含計數器值之結構的名稱。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 




