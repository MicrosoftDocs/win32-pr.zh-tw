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
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317459"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





