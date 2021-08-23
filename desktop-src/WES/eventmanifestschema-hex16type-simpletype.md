---
title: HexInt16Type 簡單類型
description: 定義2個位元組的十六進位型別。
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- HexInt16Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5f441071daa84f162a1dacbd16513fe2550b99d34d24ed90205ff4d8d184493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055957"
---
# <a name="hexint16type-simple-type"></a>HexInt16Type 簡單類型

定義2個位元組的十六進位型別。

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**HexInt16Type** 簡單類型是以下列模式限制的 **字串**：

-   `0[xX][0-9A-Fa-f]{1,4}`

    值可以包含一到四個十六進位字元 (例如0xa 或 0xac7b) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





