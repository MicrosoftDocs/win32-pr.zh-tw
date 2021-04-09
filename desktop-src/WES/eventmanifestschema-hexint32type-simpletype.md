---
title: 'UInt32Type 簡單類型 (Windows 事件記錄檔) '
description: 定義不帶正負號的整數類型。
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- UInt32Type 簡單類型 EventLog
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2a24326197c72b08032f5144fea1a69fbe68089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934326"
---
# <a name="uint32type-simple-type-windows-event-log"></a>UInt32Type 簡單類型 (Windows 事件記錄檔) 

定義不帶正負號的整數類型。 值可以指定為0到4294967295範圍內的4位元組整數或十六進位值。

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





