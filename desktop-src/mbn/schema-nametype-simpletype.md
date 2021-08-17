---
description: 定義 Mobile 寬頻設定檔的字串類型。
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: 'nameType 簡單類型 (行動寬頻) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: 9b07bfb62e23b0c82ef69bc924147675caad10d61258a5c49edc906c4b6bf2a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881402"
---
# <a name="nametype-simple-type-mobile-broadband"></a>nameType 簡單類型 (行動寬頻) 

**NameType** simple type 會定義 Mobile 寬頻設定檔的字串類型。 這個字串的長度至少要有一個字元，且長度最多為255個字元。

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



 

 




