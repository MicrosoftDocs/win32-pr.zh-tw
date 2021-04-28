---
description: CSymbolType 簡單類型 (效能計數器) -定義有效的 C/c + + 符號名稱。
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: 'CSymbolType 簡單類型 (效能計數器) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0771bb1dffc006abf8e02e6c391278f7d0b03f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084226"
---
# <a name="csymboltype-simple-type-performance-counters"></a>CSymbolType 簡單類型 (效能計數器) 

定義有效的 C/c + + 符號名稱。

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**CSymbolType** 簡單類型是以下列模式限制的 **xs： string** ：

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    符號名稱可以是空的，或包含英數位元和底線。 如果您指定名稱，則名稱必須以底線 (開頭 \_) 或字母字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 




