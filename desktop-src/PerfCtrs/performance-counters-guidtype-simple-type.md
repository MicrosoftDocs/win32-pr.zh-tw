---
description: 以登錄格式定義全域唯一識別碼型別。
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: 'GUIDType 簡單類型 (效能計數器) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 305195784a3578242caefc1fb7eb9bcd8dbd5b557d89d8752bc8242f648abbdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119624918"
---
# <a name="guidtype-simple-type-performance-counters"></a>GUIDType 簡單類型 (效能計數器) 

以登錄格式定義全域唯一識別碼型別。

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**GUIDType** 簡單類型是以下列模式限制的 **xs： string** ：

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    此值必須是登錄格式的全域唯一識別碼類型。 例如，{5b2fc63a-8af4-44cb-960c-aefdced908d6}。 使用 GUIDGen.exe 或 UUIDGen.exe 建立 GUID。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 




