---
description: 定義4位元組的十六進位型別。
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: 'HexInt32Type 簡單類型 (效能計數器) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08b9ea7e483f6580e3f896a6a3f54a65e9117597538564889df8a5afb2fe795f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033478"
---
# <a name="hexint32type-simple-type-performance-counters"></a>HexInt32Type 簡單類型 (效能計數器) 

定義4位元組的十六進位型別。

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**HexInt32Type** 簡單類型是以下列模式限制的 **xs： string** ：

-   `0[xX][0-9A-Fa-f]{1,8}`

    值可以包含一到八個十六進位字元 (例如0xa 或 0xac7bd361) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 




