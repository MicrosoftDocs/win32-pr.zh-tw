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
# <a name="network3gpp-hotspot2-element"></a><span data-ttu-id="e16b6-103">Network3GPP (Hotspot2) 元素</span><span class="sxs-lookup"><span data-stu-id="e16b6-103">Network3GPP (Hotspot2) Element</span></span>

<span data-ttu-id="e16b6-104">公開 Land Mobile Network (PLMN) 識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="e16b6-104">A list of Public Land Mobile Network (PLMN) IDs.</span></span>

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

<span data-ttu-id="e16b6-105">元素是由 [**Hotspot2**](wlan-profileschema-hotspot2-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="e16b6-105">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e16b6-106">子元素</span><span class="sxs-lookup"><span data-stu-id="e16b6-106">Child elements</span></span>



| <span data-ttu-id="e16b6-107">元素</span><span class="sxs-lookup"><span data-stu-id="e16b6-107">Element</span></span> | <span data-ttu-id="e16b6-108">類型</span><span class="sxs-lookup"><span data-stu-id="e16b6-108">Type</span></span> | <span data-ttu-id="e16b6-109">Description</span><span class="sxs-lookup"><span data-stu-id="e16b6-109">Description</span></span>                                                                                                             |
|---------|------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e16b6-110">PLMNID</span><span class="sxs-lookup"><span data-stu-id="e16b6-110">PLMNID</span></span>  |      | <span data-ttu-id="e16b6-111">個別的 PLMN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="e16b6-111">An individual PLMN ID.</span></span> <span data-ttu-id="e16b6-112">這是與3GPP 網路的 MCC/MNC 對應的5或6位數的十進位數。</span><span class="sxs-lookup"><span data-stu-id="e16b6-112">This is a 5 or 6 digit decimal number corresponding to the MCC/MNC of a 3GPP network.</span></span><br/> |



 

 




