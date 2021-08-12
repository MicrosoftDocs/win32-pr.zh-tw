---
description: 指定是否封鎖對所有基礎結構網路的存取。
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: denyAllESS (networkFilter) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5057f94dd91e2d7090c4f147ba987324e369dda706031ecebb8a79b165214414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619863"
---
# <a name="denyalless-networkfilter-element"></a>denyAllESS (networkFilter) 元素

DenyAllESS (networkFilter) 元素會指定是否封鎖對所有基礎結構網路的存取。 當 **denyAllESS** 的值為 TRUE 時，電腦無法連線到基礎結構網路。否則，機器可能會連接到基礎結構網路。

此元素的預設值為 FALSE。 如果設定檔中未指定 **denyAllESS** ，則根據預設，電腦會連線到基礎結構網路。

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

**DenyAllESS** 元素是由 [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




