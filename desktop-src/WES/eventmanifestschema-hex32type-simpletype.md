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
ms.openlocfilehash: 6c78a101ec9854b8820b7c9170ea43f06258528de9fdc9d4b02bb41945ba3a7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248098"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





