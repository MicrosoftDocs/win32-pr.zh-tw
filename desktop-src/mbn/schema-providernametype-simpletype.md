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
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511341"
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



 

 




