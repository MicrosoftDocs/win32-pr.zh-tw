---
title: 'EapType 元素 (eaptlsconnectionpropertiesv1schema) '
description: 這個元素是 BaseEapConnectionProperties 架構中 EapType 元素的衍生型別。 適用于 eaptlsconnectionpropertiesv1schema。
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
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
ms.openlocfilehash: b74341d9b1fdd9121f1d67e2a941d931be049e0f
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106984916"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a>EapType 元素 (eaptlsconnectionpropertiesv1schema) 

**EapType** 元素是 [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md)架構中 [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md)元素的衍生型別。

這個衍生的 **EapType** 元素包含下列元素： [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)、 [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)、 [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)、 [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md)、 [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)和 [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)。

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
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                                                               | 類型                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**extendedTLS: PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | Windows 7 和更新版本：指出是否執行伺服器驗證。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**extendedTLS: AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | Windows 7 和更新版本：指出是否已讀取伺服器的名稱。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**extendedTLS: TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | Windows 7 和更新版本：讓架構的未來增強功能。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | 包含 EAP 傳輸層級安全性 (EAP-TLS) 憑證位置的相關資訊。 <br/> [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)元素是選擇性的。<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | boolean                                                                                                           | 決定要使用的使用者名稱。 <br/> 如果 [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) 元素為 **TRUE**，則 eap-tls 應該使用憑證上所顯示的名稱以外的使用者名稱。 如果 [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) 元素為 **FALSE**，則 eap-tls 會使用憑證上出現的使用者名稱。<br/> [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)元素是選擇性的。 <br/> |
| [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | 包含如何執行伺服器驗證的相關資訊。 [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)元素是選擇性的。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構元素](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





