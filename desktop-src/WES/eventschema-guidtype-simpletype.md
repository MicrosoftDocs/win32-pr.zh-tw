---
title: 'GUIDType 簡單類型 (事件架構) '
description: '以登錄格式定義全域唯一識別碼型別。 |GUIDType 簡單類型 (事件架構) '
ms.assetid: dbc305ef-6f07-4a70-9013-b89ccec889ea
keywords:
- GUIDType 簡單類型 EventLog
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2fb7c0cd759b8b58b0db801819ed365f5b25fdb5abdcf886430e8bb2582cbde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750620"
---
# <a name="guidtype-simple-type-event-schema"></a>GUIDType 簡單類型 (事件架構) 

以登錄格式定義全域唯一識別碼型別。

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**GUIDType** 簡單類型是以下列模式限制的字串：

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    此值必須是登錄格式的全域唯一識別碼類型。 例如，{5b2fc63a-8af4-44cb-960c-aefdced908d6}。 使用 GUIDGen.exe 或 UUIDGen.exe 建立 GUID。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





