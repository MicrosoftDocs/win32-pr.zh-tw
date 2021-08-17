---
description: 識別行動電話通訊網路的名稱和提供者識別碼。
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: 提供者 (DataRoamingPartners) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: d5ce12ddf15ad57071f2717e5801fbd05f8e2925ea474345f7c376bc2445cd02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347158"
---
# <a name="provider-dataroamingpartners-element"></a>提供者 (DataRoamingPartners) 元素

**提供者 (DataRoamingPartners)** 元素會識別行動電話網路的名稱和提供者識別碼。

此元素具有下列子項目。

-   [**ProviderID**](schema-providerid-providertype-element.md)
-   [**ProviderName**](schema-providername-providertype-element.md)

可以在 [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) 元素內多次定義這個元素。 至少必須定義一次。

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

**Provider** 元素是由 [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**DataRoamingPartners (MBNProfile)**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




