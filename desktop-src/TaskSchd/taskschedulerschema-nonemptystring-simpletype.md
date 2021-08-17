---
title: nonEmptyStringType 簡單類型
description: 定義用於非空白文字字串的值。
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- nonEmptyString 簡單類型工作排程器
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6359240c2baba14460ab4478c31c490725646130ea2181efdcb8e92a94090d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758414"
---
# <a name="nonemptystringtype-simple-type"></a>nonEmptyStringType 簡單類型

定義用於非空白文字字串的值。

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>列舉值

**NonEmptyString** 簡單類型會定義下列值。



| 值 | 描述                                            |
|-------|--------------------------------------------------------|
| 1     | 字串至少包含一個字元。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





