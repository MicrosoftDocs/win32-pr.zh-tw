---
description: 指定電腦不得連接的無線區域網路網路清單。
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: 封鎖清單 (networkFilter) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e852286d00d93904bd185fef6c2f3444bb5987f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936587"
---
# <a name="blocklist-networkfilter-element"></a>封鎖清單 (networkFilter) 元素

封鎖清單 (networkFilter) 元素會指定電腦不得連接的無線區域網路網路清單。

``` syntax
<xs:element name="blockList">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="network"
                type="networkItemType"
                maxOccurs="unbounded"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**封鎖清單** 元素是由 [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)元素定義。

## <a name="child-elements"></a>子元素



| 元素                                                        | 類型                                                                     | Description                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [**network**](wlan-policyschema-network-blocklist-element.md) | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | 封鎖的網路。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



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

 

 




