---
description: .
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: '影像元素 (屬性描述架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb519d5f8104d114734e1f12676f213312e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969293"
---
# <a name="image"></a><span data-ttu-id="0933a-103">image</span><span class="sxs-lookup"><span data-stu-id="0933a-103">image</span></span>

<span data-ttu-id="0933a-104">每個父元素只能有一個 [image]() 元素。</span><span class="sxs-lookup"><span data-stu-id="0933a-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="0933a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0933a-105">Syntax</span></span>


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="0933a-106">項目資訊</span><span class="sxs-lookup"><span data-stu-id="0933a-106">Element Information</span></span>



| <span data-ttu-id="0933a-107">父項目</span><span class="sxs-lookup"><span data-stu-id="0933a-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="0933a-108">子元素</span><span class="sxs-lookup"><span data-stu-id="0933a-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="0933a-109">[enum](./propdesc-schema-enum.md)、 [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="0933a-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="0933a-110">無</span><span class="sxs-lookup"><span data-stu-id="0933a-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="0933a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0933a-111">Attributes</span></span>



| <span data-ttu-id="0933a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0933a-112">Attribute</span></span> | <span data-ttu-id="0933a-113">描述</span><span class="sxs-lookup"><span data-stu-id="0933a-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="0933a-114">res</span><span class="sxs-lookup"><span data-stu-id="0933a-114">res</span></span>       | <span data-ttu-id="0933a-115">公用。</span><span class="sxs-lookup"><span data-stu-id="0933a-115">Public.</span></span> <span data-ttu-id="0933a-116">必要。</span><span class="sxs-lookup"><span data-stu-id="0933a-116">Required.</span></span> |



 

 

 
