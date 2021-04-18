---
title: 'CSymbolType 簡單類型 (Windows 事件記錄檔) '
description: 定義有效的 C/c + + 符號名稱。
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- CSymbolType 簡單類型 EventLog
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67b0ccb7c573aa4d71c038f9133cea7c95cdfbd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968762"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>CSymbolType 簡單類型 (Windows 事件記錄檔) 

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

    符號名稱可以是空的，或包含英數位元和底線。 如果名稱是空的，訊息編譯器將會產生符號名稱。 如果您指定名稱，則名稱必須以底線 (開頭 \_) 或字母字元。

## <a name="remarks"></a>備註

如果符號名稱是空的，訊息編譯器會使用您定義之專案的 **name** 屬性來產生符號名稱。 編譯器會以底線取代任何非英數位元和前置數位。 例如，如果通道的 **名稱** 屬性是 Microsoft-Windows-SampleProvider/Operational，編譯器會使用 Microsoft \_ Windows \_ SampleProvider 作業 \_ 做為符號名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 





