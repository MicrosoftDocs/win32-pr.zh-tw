---
title: SimpleCertSelection (CertSelection) 元素
description: 瞭解 SimpleCertSelection (CertSelection) 元素。 此元素決定使用者選取憑證的方式。
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- SimpleCertSelection 元素 EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024105"
---
# <a name="simplecertselection-certselection-element"></a>SimpleCertSelection (CertSelection) 元素

**SimpleCertSelection (CertSelection)** 元素會決定使用者選取憑證的方式。

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

**SimpleCertSelection** 元素是由 [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)複雜型別定義。

## <a name="remarks"></a>備註

依預設， **SimpleCertSelection** 為 TRUE。 如果 **SimpleCertSelection** 為 TRUE，則 eap-tls 會執行簡單的憑證搜尋，而不需要選取憑證的任何下拉式清單。 如果 **SimpleCertSelection** 為 FALSE，則 eap-tls 會向使用者說明要選取的適當憑證。

## <a name="requirements"></a>規格需求



| 角色 | 支援 OS 的最低版本 |
|------|----------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**CertificateStore (CredentialsSourceParameters)**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構元素](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





