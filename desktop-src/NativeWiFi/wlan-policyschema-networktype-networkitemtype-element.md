---
description: 指定網路類型。
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: networkType (networkItemType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 57616d6701ab4663fa6757ddec5df4886ec02faaf5088f61b6cb466ca834ec81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684388"
---
# <a name="networktype-networkitemtype-element"></a>networkType (networkItemType) 元素

NetworkType (networkItemType) 元素會指定網路類型。 網路類型有兩種：基礎結構網路 (ESS) 和臨機操作網路 (IBSS) 。

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

**NetworkType** 元素是由 [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)複雜型別定義。

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

 

 




