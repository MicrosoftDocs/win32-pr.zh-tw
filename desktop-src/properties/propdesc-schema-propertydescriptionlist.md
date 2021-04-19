---
description: 一個或多個個別 propertyDescription 元素的容器。
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982346"
---
# <a name="propertydescriptionlist"></a><span data-ttu-id="f16a4-103">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="f16a4-103">propertyDescriptionList</span></span>

<span data-ttu-id="f16a4-104">一個或多個個別 [propertyDescription](./propdesc-schema-propertydescription.md) 元素的容器。</span><span class="sxs-lookup"><span data-stu-id="f16a4-104">Container for one or many individual [propertyDescription](./propdesc-schema-propertydescription.md) elements.</span></span> <span data-ttu-id="f16a4-105">Propdesc 屬性描述架構檔案至少應包含一個 [propertyDescriptionList]() 元素。</span><span class="sxs-lookup"><span data-stu-id="f16a4-105">A .propdesc property description schema file should contain at least one [propertyDescriptionList]() element.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16a4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f16a4-106">Syntax</span></span>


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="f16a4-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f16a4-107">Element Information</span></span>



| <span data-ttu-id="f16a4-108">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="f16a4-108">Parent Element</span></span>                        | <span data-ttu-id="f16a4-109">子元素</span><span class="sxs-lookup"><span data-stu-id="f16a4-109">Child Elements</span></span>                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="f16a4-110">schema</span><span class="sxs-lookup"><span data-stu-id="f16a4-110">schema</span></span>](./propdesc-schema-entry.md) | [<span data-ttu-id="f16a4-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f16a4-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a><span data-ttu-id="f16a4-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f16a4-112">Attributes</span></span>



| <span data-ttu-id="f16a4-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f16a4-113">Attribute</span></span> | <span data-ttu-id="f16a4-114">描述</span><span class="sxs-lookup"><span data-stu-id="f16a4-114">Description</span></span>                                                               |
|-----------|---------------------------------------------------------------------------|
| <span data-ttu-id="f16a4-115">publisher</span><span class="sxs-lookup"><span data-stu-id="f16a4-115">publisher</span></span> | <span data-ttu-id="f16a4-116">公用。</span><span class="sxs-lookup"><span data-stu-id="f16a4-116">Public.</span></span> <span data-ttu-id="f16a4-117">必要。</span><span class="sxs-lookup"><span data-stu-id="f16a4-117">Required.</span></span> <span data-ttu-id="f16a4-118">提供架構之發行者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f16a4-118">The display name of the publisher providing the schema.</span></span> |
| <span data-ttu-id="f16a4-119">product</span><span class="sxs-lookup"><span data-stu-id="f16a4-119">product</span></span>   | <span data-ttu-id="f16a4-120">公用。</span><span class="sxs-lookup"><span data-stu-id="f16a4-120">Public.</span></span> <span data-ttu-id="f16a4-121">必要。</span><span class="sxs-lookup"><span data-stu-id="f16a4-121">Required.</span></span> <span data-ttu-id="f16a4-122">提供架構的產品顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f16a4-122">The display name of the product providing the schema.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="f16a4-123">備註</span><span class="sxs-lookup"><span data-stu-id="f16a4-123">Remarks</span></span>

<span data-ttu-id="f16a4-124">[PropertyDescriptionList]()不應該與「屬性清單」和 [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)（完全分開）混淆。</span><span class="sxs-lookup"><span data-stu-id="f16a4-124">The [propertyDescriptionList]() should not be confused with "property lists" and [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which are completely separate.</span></span>

 

 
