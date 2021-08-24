---
description: 針對機器定義允許和拒絕的網路清單。
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: networkFilter (WLANPolicy) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1fff0738b8497bd52bee02a04402c77e959e2689c66e47519be20c95a58d56a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684378"
---
# <a name="networkfilter-wlanpolicy-element"></a>networkFilter (WLANPolicy) 元素

NetworkFilter (WLANPolicy) 元素會定義電腦允許和拒絕的網路清單。

``` syntax
<xs:element name="networkFilter">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="allowList"
                minOccurs="0"
            >
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
            <xs:element name="blockList"
                minOccurs="0"
            >
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
            <xs:element name="denyAllIBSS"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="denyAllESS"
                type="boolean"
                minOccurs="0"
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

**NetworkFilter** 元素是由 [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)元素定義。

## <a name="child-elements"></a>子元素



| 元素                                                                    | 類型                                                                     | 描述                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**允許清單**](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | 必須允許任何電腦連接的無線區域網路網路清單。 <br/> |
| [**封鎖清單**](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | 電腦不能連線的無線區域網路網路清單。<br/>              |
| [**denyAllESS**](wlan-policyschema-denyalless-networkfilter-element.md)   | boolean                                                                  | 指定是否封鎖對所有基礎結構網路的存取。 <br/>                     |
| [**denyAllIBSS**](wlan-policyschema-denyallibss-networkfilter-element.md) | boolean                                                                  | 指定是否封鎖對所有特定網路的存取。 <br/>                             |
| [**網路**](wlan-policyschema-network-allowlist-element.md)             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | 允許的網路。 <br/>                                                                |
| [**網路**](wlan-policyschema-network-blocklist-element.md)             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | 封鎖的網路。 <br/>                                                                 |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




