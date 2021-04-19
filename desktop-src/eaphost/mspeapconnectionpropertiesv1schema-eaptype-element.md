---
title: 'EapType 元素 (mspeapconnectionpropertiesv1schema) '
description: 這個元素是 BaseEapConnectionProperties 架構中 EapType 元素的衍生型別。 適用于 mspeapconnectionpropertiesv1schema。
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
keywords:
- EapType 元素 EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106995981"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a>EapType 元素 (mspeapconnectionpropertiesv1schema) 

**EapType** 元素是 [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md)架構中 [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md)元素的衍生型別。

這個衍生的 **EapType** 元素包含下列元素： [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)、 [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)、 [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)、 [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)、 [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)、 [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md)、 [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) 和 [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)。

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                                     | 類型                                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | 描述內部方法和方法設定。 如果 [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) 元素為 TRUE，則必須有 [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) 元素。 如果 [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) 元素為 FALSE， [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) 元素就必須不存在。<br/>           |
| [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | boolean                                                                                                         | 指出是否 (NAP) 檢查來執行網路存取保護。 如果 [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) 元素為 TRUE，則 PEAP 會執行 NAP 檢查;若為 FALSE，則不會執行 NAP 檢查。 [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md)元素是選擇性的。<br/>                                                                                |
| [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | boolean                                                                                                         | 指出是否要執行快速重新連接。 如果 [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) 元素為 TRUE，則 PEAP 會嘗試執行快速重新連線;如果為 FALSE，則 PEAP 會執行完整驗證。 [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)元素是選擇性的。<br/>                                                                                                                       |
| [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [**IdentityPrivacyParameters**](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | Windows 7 或更新版本：指出是否傳送使用者的真實身分識別或匿名身分識別。 [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)元素是選擇性的。<br/>                                                                                                                                                                                                                                                                                 |
| [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | boolean                                                                                                         | 指出是否要執行來賓存取。 如果 [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) 專案是 TRUE，則 [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) 元素必須存在，並且描述內部方法及其設定;若為 FALSE，則 PEAP 會執行來賓存取。 [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)元素是選擇性的。<br/>            |
| [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)元素可讓架構的未來增強功能。 [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)元素是選擇性的。<br/>                                                                                                                                                                                                                                    |
| [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | boolean                                                                                                         | 指出是否要使用支援加密的伺服器進行驗證。 如果 [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) 元素為 TRUE，則 PEAP 會向不支援加密的伺服器進行驗證;若為 FALSE，則 PEAP 只會驗證支援加密的伺服器。 [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)元素是選擇性的。<br/> |
| [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | 包含如何執行伺服器驗證的相關資訊。 [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)元素是選擇性的。<br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構元素](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





