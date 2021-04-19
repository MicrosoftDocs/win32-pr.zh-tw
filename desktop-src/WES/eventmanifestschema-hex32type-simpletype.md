---
title: 'HexInt32Type 簡單類型 (EventManifest 架構) '
description: '定義4位元組的十六進位型別。 |HexInt32Type 簡單類型 (EventManifest 架構) '
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
keywords:
- HexInt32Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4630bc4d7d513a0fedad2191c63ca71571ce655a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992263"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a>HexInt32Type 簡單類型 (EventManifest 架構) 

定義4位元組的十六進位型別。

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**HexInt32Type** 簡單類型是以下列模式限制的 **字串**：

-   `0[xX][0-9A-Fa-f]{1,8}`

    值可以包含一到八個十六進位字元 (例如0xa 或 0xac7bd361) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





