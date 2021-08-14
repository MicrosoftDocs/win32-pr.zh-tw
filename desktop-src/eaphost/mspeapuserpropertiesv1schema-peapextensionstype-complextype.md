---
title: " (連接屬性的 PeapExtensionsType 複雜類型) "
description: 瞭解 PeapExtensionsType 複雜類型。 此類型可讓架構的未來增強功能。
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- PeapExtensionsType 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a72fa87b3f1cf5ba4a65c179895c22e5a208616ed8c9b2ffb9f046e5de9b92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983918"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a> (連接屬性的 PeapExtensionsType 複雜類型) 

**PeapExtensionsType** 複雜型別可讓架構的未來增強功能。

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>備註

**PeapExtensionsType** 複雜類型是選擇性的。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapuserpropertiesv1 架構](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





