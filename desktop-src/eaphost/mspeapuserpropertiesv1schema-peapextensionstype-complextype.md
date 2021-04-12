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
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316486"
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
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapuserpropertiesv1 架構](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





