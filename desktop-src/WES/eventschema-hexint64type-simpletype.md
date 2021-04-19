---
title: 'HexInt64Type 簡單類型 (事件架構) '
description: '定義8位元組的十六進位型別。 |HexInt64Type 簡單類型 (事件架構) '
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
keywords:
- HexInt64Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e290c2326415664fbbae3feed9628b86452b10c6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "107001783"
---
# <a name="hexint64type-simple-type-event-schema"></a>HexInt64Type 簡單類型 (事件架構) 

定義8位元組的十六進位型別。

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**HexInt64Type** 簡單類型是以下列模式限制的 **字串**：

-   `0[xX][0-9A-Fa-f]{1,16}`

    值可以包含一到十六個十六進位字元 (例如0xa 或 0xac7bd361004fe190) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





