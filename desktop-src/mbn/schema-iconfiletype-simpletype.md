---
description: 定義行動寬頻設定檔中 ICONFilePath 元素的字串類型。
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: iconFileType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: a4ad0c27c40c1b647a15a2c53ed67ffc1deee590006e7e9a514c11f6285c6bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975247"
---
# <a name="iconfiletype-simple-type"></a>iconFileType 簡單類型

**IconFileType** 簡單類型會定義行動寬頻設定檔中 [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md)元素的字串類型。 這個字串的長度至少要有一個字元，且長度最多為1024個字元。

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



 

 




