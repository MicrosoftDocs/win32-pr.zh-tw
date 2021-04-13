---
title: EnableIdentityPrivacy (IdentityPrivacyParameters) 元素
description: 指出是否傳送使用者的真實身分識別或匿名身分識別。 |EnableIdentityPrivacy (IdentityPrivacyParameters) 元素
ms.assetid: 7751e5fa-895e-47f7-99d9-aa7ef2451eb1
keywords:
- EnableIdentityPrivacy 元素 EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a96b49fe462f4ef8cedad550d1a6c87d680939
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322484"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a>EnableIdentityPrivacy (IdentityPrivacyParameters) 元素

**EnableIdentityPrivacy (IdentityPrivacyParameters)** 元素指出是否傳送使用者的真實身分識別或匿名身分識別。

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

**EnableIdentityPrivacy** 元素是由 [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)定義。

## <a name="remarks"></a>備註

**EnableIdentityPrivacy** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv2 架構](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv2 架構元素](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





