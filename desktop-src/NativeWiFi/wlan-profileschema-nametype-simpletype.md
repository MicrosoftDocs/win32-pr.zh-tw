---
description: 包含無線局域網路設定檔的名稱或描述。
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: 'nameType 簡單類型 (LAN_policy)  (設定檔) '
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
ms.openlocfilehash: e73e8bd013836767e2a943616407aea9f563fea2
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "107001052"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a>針對 profileschema nameType 簡單類型 (LAN_policy) 

NameType 簡單類型可以包含無線局域網路設定檔的名稱或描述。 這個字串值的長度必須介於1到255個字元之間。

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
|-------------------------------------|---------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                 |



 

 




