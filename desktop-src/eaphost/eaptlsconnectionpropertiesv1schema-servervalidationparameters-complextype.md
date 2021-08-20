---
title: " (TLS) 的 ServerValidationParameters 複雜類型"
description: 瞭解 ServerValidationParameters 複雜類型。 此類型包含如何執行伺服器驗證的相關資訊。 | (TLS) 的 ServerValidationParameters 複雜類型
ms.assetid: 7a35c7f5-4cab-43d5-87dc-a4020811d3a9
keywords:
- ServerValidationParameters 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5678a4f7cc585dd004b6755732a214ca95301cc39e8879779b9776a967851870
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720306"
---
# <a name="servervalidationparameters-complex-type-tls"></a> (TLS) 的 ServerValidationParameters 複雜類型

**ServerValidationParameters** 複雜類型包含如何執行伺服器驗證的相關資訊。

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="string"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                                                                                    | 類型      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | boolean   | 指出是否應要求使用者進行伺服器驗證。 <br/> 如果 [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) 為 TRUE，則 eap-tls 會執行伺服器驗證，而不需要使用者輸入;如果驗證失敗，則 EAP-TLS 會驗證失敗。 <br/> 如果 [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) 為 FALSE，則會提示使用者輸入已驗證的伺服器憑證或名稱，或 (CA) 的根憑證授權單位。<br/> [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md)元素是選擇性的。<br/> |
| [**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | 字串    | 代表用戶端信任的伺服器清單。 每個伺服器名稱會以分號分隔，而且可以使用正則運算式來表示。<br/> [**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)元素是選擇性的。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | hexBinary | 捕捉用戶端信任的根憑證授權單位 (Ca) 的 thumb 列印。 <br/> Thumb 列印是包含憑證 SHA-1 雜湊的十六進位字串<br/> [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)元素是選擇性的。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構複雜類型](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





