---
title: namedValue 複雜類型
description: 定義與名稱/值配對中的值相關聯的名稱。
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- namedValue 複雜類型工作排程器
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f0f92b89114dfedfbfdbc61d476aff99332191317c1f67b2163eb9416ef3a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080418"
---
# <a name="namedvalue-complex-type"></a>namedValue 複雜類型

定義與名稱/值配對中的值相關聯的名稱。

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>屬性



| 名稱 | 類型                                                                    | 描述                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| NAME | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | 指定與名稱/值配對中的值相關聯的名稱。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





