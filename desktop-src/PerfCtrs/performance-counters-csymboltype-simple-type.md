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
ms.openlocfilehash: e4ebba4d72b7bc79f2aaefccfa2d71e57abd82aa06efb09abc2e83cebdb513f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033528"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 




