---
description: " (NAI) 領域識別碼的網路存取識別碼清單。"
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: NAIRealm (Hotspot2) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAIRealm
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a7c8fcf85bd23c13f0e7501d59c3db62c2bf82f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512521"
---
# <a name="nairealm-hotspot2-element"></a><span data-ttu-id="253fa-103">NAIRealm (Hotspot2) 元素</span><span class="sxs-lookup"><span data-stu-id="253fa-103">NAIRealm (Hotspot2) Element</span></span>

<span data-ttu-id="253fa-104"> (NAI) 領域識別碼的網路存取識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="253fa-104">A list of Network Access Identifier (NAI) Realm identifiers.</span></span> <span data-ttu-id="253fa-105">這份清單中的專案通常是表單 `user@domain` 。</span><span class="sxs-lookup"><span data-stu-id="253fa-105">Entries in this list are usually of the form `user@domain`.</span></span> <span data-ttu-id="253fa-106">[NAI 領域] 清單是識別大部分非行動運算子（例如 Mso、有線操作員和公用場地）的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="253fa-106">The NAI Realm list is the preferred method to identify most non-mobile operators like MSOs, wireline operators, and public venues.</span></span>

``` syntax
<xs:element name="NAIRealm"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                maxOccurs="256"
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="253fa-107">元素是由 [**Hotspot2**](wlan-profileschema-hotspot2-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="253fa-107">The element is defined by the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="253fa-108">子元素</span><span class="sxs-lookup"><span data-stu-id="253fa-108">Child elements</span></span>



| <span data-ttu-id="253fa-109">元素</span><span class="sxs-lookup"><span data-stu-id="253fa-109">Element</span></span> | <span data-ttu-id="253fa-110">類型</span><span class="sxs-lookup"><span data-stu-id="253fa-110">Type</span></span> | <span data-ttu-id="253fa-111">描述</span><span class="sxs-lookup"><span data-stu-id="253fa-111">Description</span></span>                                                   |
|---------|------|---------------------------------------------------------------|
| <span data-ttu-id="253fa-112">NAME</span><span class="sxs-lookup"><span data-stu-id="253fa-112">name</span></span>    |      | <span data-ttu-id="253fa-113">單一領域識別碼。</span><span class="sxs-lookup"><span data-stu-id="253fa-113">A single realm identifier.</span></span> <span data-ttu-id="253fa-114">通常是表單 `user@domain` 。</span><span class="sxs-lookup"><span data-stu-id="253fa-114">Usually of the form `user@domain`.</span></span> |



 

 



