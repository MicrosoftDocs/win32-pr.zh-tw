---
title: 'IdentityPrivacy (PeapExtensionsType) 元素 (v1) '
description: IdentityPrivacy (PeapExtensionsType) 元素指出是否在 mspeapconnectionpropertiesv1 架構中傳送使用者的真實身分識別。
ms.assetid: 1ae5b6e8-b1f8-45a7-ad22-fdb57cc756a2
keywords:
- 元素 EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7195ce43fb3f1a1f1710fe7aee3f5f74e18f3786
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989213"
---
# <a name="identityprivacy-peapextensionstype-element"></a>IdentityPrivacy (PeapExtensionsType) 元素

**IdentityPrivacy (PeapExtensionsType)** 元素指出是否傳送使用者的真實身分識別或匿名身分識別。

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

元素是由 [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) 元素所定義。

## <a name="remarks"></a>備註

**IdentityPrivacy** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構元素](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[**IdentityPrivacy (PeapExtensionsType)**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





