---
title: 智慧卡 (CredentialsSourceParameters) 元素
description: 表示 EAP-TLS 應該從智慧卡讀取憑證。
ms.assetid: 0755b0bf-520a-4ae6-a8fc-2f69ae12b066
keywords:
- 智慧卡元素 EAPHost
topic_type:
- apiref
api_name:
- SmartCard
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14581a06064a242a0f66e763e0b848d7d74bce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966514"
---
# <a name="smartcard-credentialssourceparameters-element"></a>智慧卡 (CredentialsSourceParameters) 元素

**智慧卡 (CredentialsSourceParameters)** 元素表示 eap-tls 應該從智慧卡讀取憑證。

``` syntax
<xs:element name="SmartCard"
    type="emptyString"
 />
```

**智慧卡** 元素是由 [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)複雜型別定義。

## <a name="remarks"></a>備註

[**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)和 **智慧卡** 元素不能同時使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



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

 

 





