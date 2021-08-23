---
title: UInt8Type 簡單類型
description: 定義不帶正負號的位元組類型。
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- UInt8Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a48c21e34edecbf4dfb4f9c2e87c85a77e3f500ec42b8607f1de004e7679ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511308"
---
# <a name="uint8type-simple-type"></a>UInt8Type 簡單類型

定義不帶正負號的位元組類型。 值可以指定為0到255範圍內的1位元組整數或十六進位值。

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





