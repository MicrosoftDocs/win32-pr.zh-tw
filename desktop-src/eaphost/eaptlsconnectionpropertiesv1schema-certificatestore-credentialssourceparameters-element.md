---
title: CertificateStore (CredentialsSourceParameters) 元素
description: 指出 EAP-TLS 應該從使用者的 [我的存放區] 或正在驗證的電腦讀取憑證。
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- CertificateStore 元素 EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fb3d2b5c9d50ea8b63c513e4fd9e7297afe236c5ccd16711d9bf4371e76a8d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274290"
---
# <a name="certificatestore-credentialssourceparameters-element"></a>CertificateStore (CredentialsSourceParameters) 元素

**CertificateStore (CredentialsSourceParameters)** 元素表示 eap-tls 應該從使用者的 [我的存放區] 或正在驗證的電腦讀取憑證。

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

**CertificateStore** 元素是由 [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)複雜型別定義。

## <a name="remarks"></a>備註

**CertificateStore** 和 [**智慧卡**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)元素不能同時使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**CredentialsSource (EapType)**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構元素](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





