---
description: 描述單一唯一的標準屬性。
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: propertyDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943853"
---
# <a name="propertydescription"></a><span data-ttu-id="4b44a-103">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="4b44a-103">propertyDescription</span></span>

<span data-ttu-id="4b44a-104">描述單一唯一的標準屬性。</span><span class="sxs-lookup"><span data-stu-id="4b44a-104">Describes a single unique canonical property.</span></span> <span data-ttu-id="4b44a-105">要在系統中使用的每個這類屬性都必須有對應的 [propertyDescription]() 元素。</span><span class="sxs-lookup"><span data-stu-id="4b44a-105">Every such property intended to be available in the system must have a corresponding [propertyDescription]() element.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="4b44a-106">Windows 7 的語法</span><span class="sxs-lookup"><span data-stu-id="4b44a-106">Syntax for Windows 7</span></span>


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a><span data-ttu-id="4b44a-107">Vista 的語法</span><span class="sxs-lookup"><span data-stu-id="4b44a-107">Syntax for Vista</span></span>


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="4b44a-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4b44a-108">Element Information</span></span>



| <span data-ttu-id="4b44a-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="4b44a-109">Parent Element</span></span>                                                           | <span data-ttu-id="4b44a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4b44a-110">Child Elements</span></span>                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="4b44a-111">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="4b44a-111">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md) | [<span data-ttu-id="4b44a-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="4b44a-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [<span data-ttu-id="4b44a-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="4b44a-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [<span data-ttu-id="4b44a-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="4b44a-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [<span data-ttu-id="4b44a-115">System.management.automation.aliasinfo</span><span class="sxs-lookup"><span data-stu-id="4b44a-115">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [<span data-ttu-id="4b44a-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4b44a-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [<span data-ttu-id="4b44a-117">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="4b44a-117">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a><span data-ttu-id="4b44a-118">屬性</span><span class="sxs-lookup"><span data-stu-id="4b44a-118">Attributes</span></span>



| <span data-ttu-id="4b44a-119">屬性</span><span class="sxs-lookup"><span data-stu-id="4b44a-119">Attribute</span></span> | <span data-ttu-id="4b44a-120">描述</span><span class="sxs-lookup"><span data-stu-id="4b44a-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b44a-121">NAME</span><span class="sxs-lookup"><span data-stu-id="4b44a-121">name</span></span>      | <span data-ttu-id="4b44a-122">必要。</span><span class="sxs-lookup"><span data-stu-id="4b44a-122">Required.</span></span> <span data-ttu-id="4b44a-123">標準屬性名稱，對系統而言是唯一的;例如， `System.Rating` 。</span><span class="sxs-lookup"><span data-stu-id="4b44a-123">The canonical property name, unique to the system; for example, `System.Rating`.</span></span> <span data-ttu-id="4b44a-124">這個字串的型別是標準型別，而且限制為64個字元。</span><span class="sxs-lookup"><span data-stu-id="4b44a-124">This string is of type canonical-type and is limited to 64 characters.</span></span> <span data-ttu-id="4b44a-125">名稱區分大小寫，而且應該使用下列語法： PropertyName。</span><span class="sxs-lookup"><span data-stu-id="4b44a-125">The name is case-sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="4b44a-126">[**IPropertyDescription：： GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) 會傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="4b44a-126">[**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) returns this value.</span></span> |
| <span data-ttu-id="4b44a-127">formatID</span><span class="sxs-lookup"><span data-stu-id="4b44a-127">formatID</span></span>  | <span data-ttu-id="4b44a-128">必要。</span><span class="sxs-lookup"><span data-stu-id="4b44a-128">Required.</span></span> <span data-ttu-id="4b44a-129">屬性的格式識別碼 (FMTID) 。</span><span class="sxs-lookup"><span data-stu-id="4b44a-129">The property's format identifier (FMTID).</span></span> <span data-ttu-id="4b44a-130">值必須包含括住的括弧;例如， `{64440492-4C8B-11D1-8B70-080036B11A03}` 。</span><span class="sxs-lookup"><span data-stu-id="4b44a-130">The value must include enclosing braces; for example, `{64440492-4C8B-11D1-8B70-080036B11A03}`.</span></span> <span data-ttu-id="4b44a-131">[**IPropertyDescription：： GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) 會傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="4b44a-131">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span>                                                                                                                       |
| <span data-ttu-id="4b44a-132">propID</span><span class="sxs-lookup"><span data-stu-id="4b44a-132">propID</span></span>    | <span data-ttu-id="4b44a-133">必要。</span><span class="sxs-lookup"><span data-stu-id="4b44a-133">Required.</span></span> <span data-ttu-id="4b44a-134">屬性識別碼 (PID) ;例如， `9` 。</span><span class="sxs-lookup"><span data-stu-id="4b44a-134">The property identifier (PID); for example, `9`.</span></span> <span data-ttu-id="4b44a-135">[**IPropertyDescription：： GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) 會傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="4b44a-135">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span> <span data-ttu-id="4b44a-136">此值必須大於或等於2。</span><span class="sxs-lookup"><span data-stu-id="4b44a-136">This value must be greater than or equal to 2.</span></span> <span data-ttu-id="4b44a-137">值0和1是由系統所保留。</span><span class="sxs-lookup"><span data-stu-id="4b44a-137">The values 0 and 1 are reserved by the system.</span></span>                                                                                                                  |



 

 

 
