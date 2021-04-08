---
title: PeapExtensionsType 複雜類型
description: 包含在 Windows 7 中所做的架構增強功能。 未來的架構增強功能將由 PeapExtensionsTypeV2 處理。
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
keywords:
- PeapExtensionsType 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cb8c698122c5a466ae95f728838425a5f10c665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686243"
---
# <a name="peapextensionstype-complex-type"></a>PeapExtensionsType 複雜類型

**PeapExtensionsType** 複雜類型包含在 Windows 7 中所做的架構增強功能。 未來的架構增強功能將由 [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md)處理。

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                                                               | 類型 | Description                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [**extendedPeap:PerformServerValidation**](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | Windows 7 和更新版本：指出是否執行伺服器驗證。<br/>                          |
| [**extendedPeap:AcceptServerName**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | Windows 7 和更新版本：指出是否已讀取伺服器的名稱。<br/>                            |
| [**extendedPeap:IdentityPrivacy**](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | Windows 7 和更新版本：指出是否傳送使用者的真實身分識別或匿名身分識別。<br/> |
| [**extendedPeap:PeapExtensionsV2**](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | Windows 7 和更新版本：讓架構的未來增強功能。<br/>                                 |



## <a name="remarks"></a>備註

**PeapExtensionsType** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構複雜類型](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





