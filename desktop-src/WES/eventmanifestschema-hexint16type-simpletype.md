---
title: UInt16Type 簡單類型
description: 定義不帶正負號的短型別。
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- UInt16Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3398b0ad92724c8b7f415bd85e8101d7c74cc6a9391e1f95349f6ef629dff0c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343717"
---
# <a name="uint16type-simple-type"></a>UInt16Type 簡單類型

定義不帶正負號的短型別。 值可以指定為0到65535範圍內的2位元組整數或十六進位值。

``` syntax
<xs:simpleType name="UInt16Type">
    <xs:union
        memberValues="unsignedShort HexInt16Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





