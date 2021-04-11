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
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849281"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 




