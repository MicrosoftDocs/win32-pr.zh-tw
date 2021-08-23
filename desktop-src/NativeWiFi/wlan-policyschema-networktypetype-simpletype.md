---
description: 定義無線網路類型。
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: networkTypeType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 40184bb027f80826baa3ad56090755a2cd9ec630f9eb105e402d30a6ecf2661c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800108"
---
# <a name="networktypetype-simple-type"></a>networkTypeType 簡單類型

NetworkTypeType 簡單類型會定義無線網路類型。 網路類型有兩種：基礎結構網路 (ESS) 和臨機操作網路 (IBSS) 。

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>列舉值

**NetworkTypeType** 簡單類型會定義下列值。



| 值 | 描述 |
|-------|-------------|
| IBSS  |             |
| ESS   |             |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 




