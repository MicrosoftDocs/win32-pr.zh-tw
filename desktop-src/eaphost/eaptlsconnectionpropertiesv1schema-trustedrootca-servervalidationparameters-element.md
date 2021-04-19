---
title: TrustedRootCA (ServerValidationParameters) 元素-連接
description: 捕捉用戶端信任的根憑證授權單位 (Ca) 的列印經驗。 |TrustedRootCA (ServerValidationParameters) 元素
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
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
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106992759"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a>連接屬性的 TrustedRootCA (ServerValidationParameters) 元素

**TrustedRootCA (ServerValidationParameters)** 專案會捕捉用戶端所信任之根憑證授權單位 (ca) 的 thumb 列印。

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

**TrustedRootCA** 元素是由 [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)複雜型別定義。

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

[**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**架構實例中可能的直接父元素**
</dt> <dt>

[**ServerValidation (EapType)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構元素](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





