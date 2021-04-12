---
title: nonEmptyStringType 簡單類型
description: 定義用於非空白文字字串的值。
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- nonEmptyString 簡單類型工作排程器
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384909"
---
# <a name="nonemptystringtype-simple-type"></a>nonEmptyStringType 簡單類型

定義用於非空白文字字串的值。

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>列舉值

**NonEmptyString** 簡單類型會定義下列值。



| 值 | 描述                                            |
|-------|--------------------------------------------------------|
| 1     | 字串至少包含一個字元。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





