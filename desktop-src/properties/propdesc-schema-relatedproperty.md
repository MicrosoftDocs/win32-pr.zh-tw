---
description: 適用于 Windows 7 的新。 識別與屬性描述檔案中定義之屬性相關的屬性。
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318896"
---
# <a name="relatedproperty"></a><span data-ttu-id="02094-104">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="02094-104">relatedProperty</span></span>

<span data-ttu-id="02094-105">適用于 Windows 7 的新。</span><span class="sxs-lookup"><span data-stu-id="02094-105">New for Windows 7.</span></span> <span data-ttu-id="02094-106">識別與屬性描述檔案中定義之屬性相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="02094-106">Identifies a property that is related to the property defined in the property description file.</span></span> <span data-ttu-id="02094-107">您可以視需要在[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md)中有任意數量的[relatedProperty]()元素。</span><span class="sxs-lookup"><span data-stu-id="02094-107">There can be as many [relatedProperty]() elements within a [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="02094-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="02094-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="02094-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="02094-109">Element Information</span></span>



| <span data-ttu-id="02094-110">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="02094-110">Parent Element</span></span>                                                   | <span data-ttu-id="02094-111">子元素</span><span class="sxs-lookup"><span data-stu-id="02094-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="02094-112">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="02094-112">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) | <span data-ttu-id="02094-113">無</span><span class="sxs-lookup"><span data-stu-id="02094-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="02094-114">屬性</span><span class="sxs-lookup"><span data-stu-id="02094-114">Attributes</span></span>



| <span data-ttu-id="02094-115">屬性</span><span class="sxs-lookup"><span data-stu-id="02094-115">Attribute</span></span>        | <span data-ttu-id="02094-116">描述</span><span class="sxs-lookup"><span data-stu-id="02094-116">Description</span></span>                                                        |
|------------------|--------------------------------------------------------------------|
| <span data-ttu-id="02094-117">relationshipName</span><span class="sxs-lookup"><span data-stu-id="02094-117">relationshipName</span></span> | <span data-ttu-id="02094-118">公用。</span><span class="sxs-lookup"><span data-stu-id="02094-118">Public.</span></span> <span data-ttu-id="02094-119">必要。</span><span class="sxs-lookup"><span data-stu-id="02094-119">Required.</span></span> <span data-ttu-id="02094-120">屬性關聯性的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="02094-120">The canonical name of the property relationship.</span></span> |
| <span data-ttu-id="02094-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="02094-121">propertyName</span></span>     | <span data-ttu-id="02094-122">公用。</span><span class="sxs-lookup"><span data-stu-id="02094-122">Public.</span></span> <span data-ttu-id="02094-123">必要。</span><span class="sxs-lookup"><span data-stu-id="02094-123">Required.</span></span> <span data-ttu-id="02094-124">相關屬性的標準名稱。</span><span class="sxs-lookup"><span data-stu-id="02094-124">The canonical name of the related property.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="02094-125">備註</span><span class="sxs-lookup"><span data-stu-id="02094-125">Remarks</span></span>

<span data-ttu-id="02094-126">此元素可讓您將一個屬性對應至另一個屬性。</span><span class="sxs-lookup"><span data-stu-id="02094-126">This element enables you to map one property to another.</span></span> <span data-ttu-id="02094-127">例如，您可以將自訂屬性（StorageCapacity）的文字對應至 [系統]：</span><span class="sxs-lookup"><span data-stu-id="02094-127">For example, you can map the text of your custom property, Fabrikam.StorageCapacity, to System.Capacity:</span></span>


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
