---
description: 裝置家用網路提供者的功能變數名稱，識別網路的操作員。
ms.assetid: 7676e1d8-a414-401f-989c-9f60068b92d8
title: DomainName (Hotspot2) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DomainName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 670fc91771ee0a47cd7f16f617d052df2e567b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972882"
---
# <a name="domainname-hotspot2-element"></a>DomainName (Hotspot2) 元素

裝置家用網路提供者的功能變數名稱，識別網路的操作員。

``` syntax
<xs:element name="DomainName"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="255"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

元素是由 [**Hotspot2**](wlan-profileschema-hotspot2-element.md) 元素所定義。

 

 



