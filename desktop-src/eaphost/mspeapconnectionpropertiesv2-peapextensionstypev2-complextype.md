---
title: PeapExtensionsTypeV2 複雜類型
description: 瞭解 PeapExtensionsTypeV2 複雜類型。 此類型可讓架構的未來增強功能。
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baea42ec60fe84085ea5e4541848fd43b786419bedab17e938044ff0a713fa07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086027"
---
# <a name="peapextensionstypev2-complex-type"></a>PeapExtensionsTypeV2 複雜類型

**PeapExtensionsTypeV2** 複雜型別可讓架構的未來增強功能。


```XML
<xs:complexType name="PeapExtensionsTypeV2">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a>備註

**PeapExtensionsTypeV2** 元素是選擇性的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv2 架構](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv2 複雜類型](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




