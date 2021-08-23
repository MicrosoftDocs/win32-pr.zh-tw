---
title: 'UInt64Type 簡單類型 (EventManifest 架構) '
description: 定義不帶正負號的 long 類型。
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- UInt64Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 088cdead48fb62adf816b6065e211afcc994ec618db8b7e9a0597e6f72c1780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511338"
---
# <a name="uint64type-simple-type"></a>UInt64Type 簡單類型

定義不帶正負號的 long 類型。 值可以指定為0到18446744073709551615之間的8位元組整數或十六進位值。

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





