---
title: LengthType 簡單類型
description: 定義長度類型，這個類型會用來指定變數長度資料項目（例如二進位資料或 ANSI 或 Unicode 字串）中的位元組或字元數目。
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- LengthType 簡單類型 EventLog
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9ded861e3e46cd5e4fc6c069d95bba9f0ab3457559bf319aef41cdf906e193b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997858"
---
# <a name="lengthtype-simple-type"></a>LengthType 簡單類型

定義長度類型，這個類型會用來指定變數長度資料項目（例如二進位資料或 ANSI 或 Unicode 字串）中的位元組或字元數目。 值可以指定為 xs： unsignedShort 值，或指定為參考包含不帶正負號短值之資料項目節點名稱的字串。

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





