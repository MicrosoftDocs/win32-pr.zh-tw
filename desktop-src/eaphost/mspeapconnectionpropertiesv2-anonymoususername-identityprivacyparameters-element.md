---
title: AnonymousUserName (IdentityPrivacyParameters) 元素
description: 包含用來取代使用者真正識別的匿名身分識別。 當身分識別以純文字傳送時，會在 PEAP 驗證的第一個階段傳送。
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- AnonymousUserName 元素 EAPHost
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
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384945"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a>AnonymousUserName (IdentityPrivacyParameters) 元素

**AnonymousUserName (IdentityPrivacyParameters)** 元素包含用來取代使用者真正識別的匿名身分識別。 當身分 **識別** 以純文字傳送時，會在 PEAP 驗證的第一個階段傳送。

匿名身分識別的使用方式取決於 [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) 元素。

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

**AnonymousUserName** 元素是由 [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)定義。

## <a name="remarks"></a>備註

**AnonymousUserName** 元素是選擇性的。

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

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv2 架構](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv2 架構元素](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





