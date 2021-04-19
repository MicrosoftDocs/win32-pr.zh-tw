---
description: 公開 Land Mobile Network (PLMN) 識別碼的清單。
ms.assetid: 2e5e23c0-e98f-48f8-97b8-c5f88c80c51e
title: Network3GPP (Hotspot2) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network3GPP
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7e19a7ccbc1579eb02ed47da82afe1eeaf8fed53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985421"
---
# <a name="network3gpp-hotspot2-element"></a>Network3GPP (Hotspot2) 元素

公開 Land Mobile Network (PLMN) 識別碼的清單。

``` syntax
<xs:element name="Network3GPP"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="PLMNID"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="5"
                         />
                        <xs:maxLength
                            value="6"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

元素是由 [**Hotspot2**](wlan-profileschema-hotspot2-element.md) 元素所定義。

## <a name="child-elements"></a>子元素



| 元素 | 類型 | Description                                                                                                             |
|---------|------|-------------------------------------------------------------------------------------------------------------------------|
| PLMNID  |      | 個別的 PLMN 識別碼。 這是與3GPP 網路的 MCC/MNC 對應的5或6位數的十進位數。<br/> |



 

 




