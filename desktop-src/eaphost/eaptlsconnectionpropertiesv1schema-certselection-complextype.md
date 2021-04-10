---
title: CertSelection 複雜類型
description: 瞭解 CertSelection 複雜類型。 此類型會決定使用者選取憑證的方式。
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- CertSelection 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316474"
---
# <a name="certselection-complex-type"></a>CertSelection 複雜類型

**CertSelection** 複雜型別決定使用者選取憑證的方式。

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                                     | 類型    | Description                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | boolean | 預設為 TRUE。 如果 [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) 為 TRUE，則 eap-tls 會執行簡單的憑證搜尋，而不需要選取憑證的任何下拉式清單。 如果 **SimpleCertSelection** 為 FALSE，則 eap-tls 會向使用者說明要選取的適當憑證。<br/> |



## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構複雜類型](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





