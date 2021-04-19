---
description: 由 IEEE 指派 (OUI) 的組織唯一識別碼清單。
ms.assetid: 4a9885b6-2e57-4a16-8e1d-b5b0797e09db
title: RoamingConsortium (Hotspot2) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RoamingConsortium
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5e53fa274cbc56de6be026ef0e466ec501cf9124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971685"
---
# <a name="roamingconsortium-hotspot2-element"></a><span data-ttu-id="f8e36-103">RoamingConsortium (Hotspot2) 元素</span><span class="sxs-lookup"><span data-stu-id="f8e36-103">RoamingConsortium (Hotspot2) Element</span></span>

<span data-ttu-id="f8e36-104">由 IEEE 指派 (OUI) 的組織唯一識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="f8e36-104">A list of Organizationally Unique Identifiers (OUI) assigned by IEEE.</span></span>

``` syntax
<xs:element name="RoamingConsortium"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:minLength
                            value="3"
                         />
                        <xs:maxLength
                            value="5"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="f8e36-105">元素是由 [**Hotspot2**](wlan-profileschema-hotspot2-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="f8e36-105">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f8e36-106">子元素</span><span class="sxs-lookup"><span data-stu-id="f8e36-106">Child elements</span></span>



| <span data-ttu-id="f8e36-107">元素</span><span class="sxs-lookup"><span data-stu-id="f8e36-107">Element</span></span> | <span data-ttu-id="f8e36-108">類型</span><span class="sxs-lookup"><span data-stu-id="f8e36-108">Type</span></span> | <span data-ttu-id="f8e36-109">Description</span><span class="sxs-lookup"><span data-stu-id="f8e36-109">Description</span></span>                                                               |
|---------|------|---------------------------------------------------------------------------|
| <span data-ttu-id="f8e36-110">OUI</span><span class="sxs-lookup"><span data-stu-id="f8e36-110">OUI</span></span>     |      | <span data-ttu-id="f8e36-111">單一的 OUI，格式為可變大小的十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="f8e36-111">A single OUI, formatted as a variable size hexadecimal number.</span></span><br/> |



 

 




