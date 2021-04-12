---
description: 定義包含 Margin 元素之 Type 屬性有效值的型別。
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: MarginTypeType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194788"
---
# <a name="margintypetype-simple-type"></a>MarginTypeType 簡單類型

定義包含 [Margin 元素](margin-element.md)之 **type** 屬性有效值的型別。

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**MarginTypeType** 簡單類型是以下列模式限制的 **字串**：

-   `Left|Right`

## <a name="remarks"></a>備註

[Margin 元素](margin-element.md)的 **Type** 屬性有效值為 "Left" 和 "Right"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                     |



 

 




