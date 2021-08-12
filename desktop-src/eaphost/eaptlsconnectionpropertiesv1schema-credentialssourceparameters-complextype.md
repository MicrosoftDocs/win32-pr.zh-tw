---
title: CredentialsSourceParameters 複雜類型
description: 定義所需的元素，以指定要與 EAP-TLS 驗證搭配使用的憑證來源。
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- CredentialsSourceParameters 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 881cd4225c0e7e2f557ad7206176224a0b3929cdac7398b29f30382506f816ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274005"
---
# <a name="credentialssourceparameters-complex-type"></a>CredentialsSourceParameters 複雜類型

**CredentialsSourceParameters** 複雜型別會定義必要的元素，以指定要與 eap-tls 驗證搭配使用的憑證來源。

[**智慧卡**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)元素或 [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)元素之間有一個選擇。

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                                             | 類型                                                                                  | 描述                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | 指出 EAP-TLS 應該從使用者的 [我的存放區] 或正在驗證的電腦讀取憑證。 <br/> |
| [**智慧卡**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [**emptyString**](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | 表示 EAP-TLS 應該從智慧卡讀取憑證。 <br/>                                          |



## <a name="remarks"></a>備註

[**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)和 [**智慧卡**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)元素不能同時使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構複雜類型](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





