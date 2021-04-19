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
ms.openlocfilehash: e3236d7416cbb199037813a8ae870d4f87718081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966309"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





