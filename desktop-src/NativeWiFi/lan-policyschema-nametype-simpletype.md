---
description: 針對有線區域網路原則設定檔的名稱或描述定義字串類型。
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
title: 'nameType 簡單類型 (LAN_policy) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3b3d558717777c9b2bead2fd7e141dee38b22491af4142d4948c7f1f76aadfd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065108"
---
# <a name="nametype-simple-type-lan_policy"></a>nameType 簡單類型 (LAN_policy) 

NameType 簡單類型會針對有線區域網路原則設定檔的名稱或描述定義字串類型。 名稱和描述是長度至少為1個字元且長度最多為255個字元的字串。

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 




