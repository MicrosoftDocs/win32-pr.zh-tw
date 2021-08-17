---
description: 在 Mobile 寬頻設定檔中定義 ProviderName 元素的字串類型。
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: providerNameType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: e0a1a0c999eebe8d4ac9922564a28f3b8abce90397fbbda3556bf7726c7355cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744385"
---
# <a name="providernametype-simple-type"></a>providerNameType 簡單類型

**ProviderNameType** simple 型別會在 Mobile 寬頻設定檔中定義 [**ProviderName**](schema-providername-providertype-element.md)元素的字串型別。 這個字串的長度至少要有一個字元，且長度最多為20個字元。

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



 

 




