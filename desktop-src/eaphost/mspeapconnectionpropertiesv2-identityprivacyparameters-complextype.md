---
title: IdentityPrivacyParameters 複雜類型
description: 包含在 PEAP 驗證期間匿名身分識別使用方式的相關資訊。
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 18bef3eb69ab2799f7139fe2886d89e996fb8fb47d178997694c568450fb8340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983898"
---
# <a name="identityprivacyparameters-complex-type"></a>IdentityPrivacyParameters 複雜類型

**IdentityPrivacyParameters** 複雜類型包含在 PEAP 驗證期間匿名身分識別使用方式的相關資訊。


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| 元素                                                                                                               | 類型    | 描述                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | boolean | 指出是否傳送使用者的真實身分識別或匿名身分識別。                                                                                                                                                                                                                                                                           |
| [**AnonymousUserName**](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | 字串  | 包含用來取代使用者真正識別的匿名身分識別。 當身分 **識別** 以純文字傳送時，會在 PEAP 驗證的第一個階段傳送。 匿名身分識別的使用方式取決於 [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) 元素。 |



 

## <a name="remarks"></a>備註

IdentityPrivacyParameters 元素是選擇性的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv2 架構](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv2 複雜類型](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




