---
title: CountType 簡單類型
description: 定義用來指定陣列中元素數目的計數類型。
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- CountType 簡單類型 EventLog
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686596"
---
# <a name="counttype-simple-type"></a>CountType 簡單類型

定義用來指定陣列中元素數目的計數類型。 您可以將此值指定為 xs： unsignedShort 值，或指定為參考包含 unsiged short 值的資料項目節點名稱的字串。

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





