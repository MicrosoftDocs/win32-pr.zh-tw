---
description: 識別要用來建立資料連線的 APN 或撥號字串。
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: AccessString (coNtextType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 603c4aa04bb3e86891ec121233474fa96ffd792cbcb6880bad9e76599003d979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975277"
---
# <a name="accessstring-contexttype-element"></a>AccessString (coNtextType) 元素

**AccessString (coNtextType)** 元素會識別要用來建立資料連線的 APN 或撥號字串。

這個元素的最大長度可以是100個字元。

這是選擇性的項目。

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**AccessString** 元素是由 [**coNtextType**](schema-contexttype-complextype.md)複雜型別定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**coNtextType**](schema-contexttype-complextype.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**MBNProfile) 內容 (**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




