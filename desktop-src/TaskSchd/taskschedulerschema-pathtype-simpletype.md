---
title: pathType 簡單類型
description: 定義定義檔案路徑之字串的最小和最大字元數。
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- pathType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970461"
---
# <a name="pathtype-simple-type"></a>pathType 簡單類型

定義定義檔案路徑之字串的最小和最大字元數。 路徑不可以是空字串，而且必須少於260個字元。

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





