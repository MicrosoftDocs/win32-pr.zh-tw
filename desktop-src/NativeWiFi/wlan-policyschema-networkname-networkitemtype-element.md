---
description: 指定無線網路 (SSID) 的服務組識別元。
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: networkName (networkItemType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8c21d5dac057aaf20461e3b27bf6e23f66ec19ae3515045665d277ea4413566a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779918"
---
# <a name="networkname-networkitemtype-element"></a>networkName (networkItemType) 元素

NetworkName (networkItemType) 元素會指定無線網路 (SSID) 的服務組識別元。

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

**NetworkName** 元素是由 [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)複雜型別定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

**架構實例中可能的直接父元素**
</dt> <dt>

[**network (允許清單)**](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[**network (封鎖清單)**](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




