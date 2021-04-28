---
description: image
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: '影像元素 (屬性描述架構) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24ecb1b88b8b724ce299a81281f926972180743
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104986"
---
# <a name="image"></a><span data-ttu-id="41ae1-103">image</span><span class="sxs-lookup"><span data-stu-id="41ae1-103">image</span></span>

<span data-ttu-id="41ae1-104">每個父元素只能有一個 [image]() 元素。</span><span class="sxs-lookup"><span data-stu-id="41ae1-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="41ae1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41ae1-105">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="41ae1-106">項目資訊</span><span class="sxs-lookup"><span data-stu-id="41ae1-106">Element Information</span></span>



| <span data-ttu-id="41ae1-107">父項目</span><span class="sxs-lookup"><span data-stu-id="41ae1-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="41ae1-108">子元素</span><span class="sxs-lookup"><span data-stu-id="41ae1-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="41ae1-109">[enum](./propdesc-schema-enum.md)、 [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="41ae1-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="41ae1-110">無</span><span class="sxs-lookup"><span data-stu-id="41ae1-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="41ae1-111">屬性</span><span class="sxs-lookup"><span data-stu-id="41ae1-111">Attributes</span></span>



| <span data-ttu-id="41ae1-112">屬性</span><span class="sxs-lookup"><span data-stu-id="41ae1-112">Attribute</span></span> | <span data-ttu-id="41ae1-113">描述</span><span class="sxs-lookup"><span data-stu-id="41ae1-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="41ae1-114">res</span><span class="sxs-lookup"><span data-stu-id="41ae1-114">res</span></span>       | <span data-ttu-id="41ae1-115">公用。</span><span class="sxs-lookup"><span data-stu-id="41ae1-115">Public.</span></span> <span data-ttu-id="41ae1-116">必要。</span><span class="sxs-lookup"><span data-stu-id="41ae1-116">Required.</span></span> |



 

 

 
