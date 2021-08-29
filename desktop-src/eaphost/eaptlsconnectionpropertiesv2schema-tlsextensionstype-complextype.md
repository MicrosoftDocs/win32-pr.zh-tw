---
title: TLSExtensionsType 複雜類型
description: 瞭解 TLSExtensionsType 複雜類型。 此類型可讓架構的未來增強功能。
ms.assetid: 5e4f8ef8-1adb-4683-8001-ba7d2d392523
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ac12ad6d3b1229f4fcb75506a9e7ae7655db0287ad58fa9a8079ba12c14e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984099"
---
# <a name="tlsextensionstype-complex-type"></a>TLSExtensionsType 複雜類型

**TLSExtensionsType** 複雜型別可讓架構的未來增強功能。


```XML
<xs:complexType name="TLSExtensionsType">
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

**TLSExtensionsType** 元素是選擇性的。

## <a name="related-topics"></a>相關主題

<dl> <dt>


</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2 複雜類型](eaptlsconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**TLSExtensions (TLSExtensionsType)**](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 




