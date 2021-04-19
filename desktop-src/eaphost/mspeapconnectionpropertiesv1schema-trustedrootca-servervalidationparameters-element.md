---
title: 'TrustedRootCA (ServerValidationParameters) 元素 (v1) '
description: 捕捉用戶端信任的根憑證授權單位 (Ca) 的 thumb 列印。 |TrustedRootCA (ServerValidationParameters) 元素
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
keywords:
- TrustedRootCA 元素 EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e1b81e080d48ac8fae4f082c3cf4b46bac858e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106995983"
---
# <a name="trustedrootca-servervalidationparameters-element"></a>TrustedRootCA (ServerValidationParameters) 元素

**TrustedRootCA (ServerValidationParameters)** 元素元素會捕捉用戶端所信任之根憑證授權單位 (ca) 的 thumb 列印。

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

**TrustedRootCA** 元素是由 [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)複雜型別定義。

## <a name="remarks"></a>備註

Thumb 列印是包含憑證之 SHA-1 雜湊的十六進位字串。 **TrustedRootCA** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**架構實例中可能的直接父元素**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構元素](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





