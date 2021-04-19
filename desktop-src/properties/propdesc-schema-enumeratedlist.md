---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將屬性的值格式化為字串。
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: enumeratedList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001718"
---
# <a name="enumeratedlist"></a><span data-ttu-id="fca16-103">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="fca16-103">enumeratedList</span></span>

<span data-ttu-id="fca16-104">指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。</span><span class="sxs-lookup"><span data-stu-id="fca16-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="fca16-105">它也會影響屬性的分組方式，或者，如果 "editControl" 是 listblox，則會顯示要在清單中顯示的值。</span><span class="sxs-lookup"><span data-stu-id="fca16-105">It also influences how the property may be grouped, or what values to show in the list if the "editControl" is a listblox.</span></span> <span data-ttu-id="fca16-106">這僅適用于 <displayInfo displayType="Enumerated"> 。</span><span class="sxs-lookup"><span data-stu-id="fca16-106">This is applicable only if <displayInfo displayType="Enumerated">.</span></span> <span data-ttu-id="fca16-107">每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[enumeratedList]()元素。</span><span class="sxs-lookup"><span data-stu-id="fca16-107">There should be only one [enumeratedList]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="fca16-108">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="fca16-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="fca16-109">如果未提供任何 [enumeratedList]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="fca16-109">If no [enumeratedList]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="fca16-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fca16-110">Syntax</span></span>


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="fca16-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="fca16-111">Element Information</span></span>



| <span data-ttu-id="fca16-112">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="fca16-112">Parent Element</span></span>                                   | <span data-ttu-id="fca16-113">子元素</span><span class="sxs-lookup"><span data-stu-id="fca16-113">Child Elements</span></span>                               |
|--------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="fca16-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="fca16-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | [<span data-ttu-id="fca16-115">枚舉</span><span class="sxs-lookup"><span data-stu-id="fca16-115">enum</span></span>](./propdesc-schema-enum.md)           |
|                                                  | [<span data-ttu-id="fca16-116">enumRange</span><span class="sxs-lookup"><span data-stu-id="fca16-116">enumRange</span></span>](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a><span data-ttu-id="fca16-117">屬性</span><span class="sxs-lookup"><span data-stu-id="fca16-117">Attributes</span></span>



| <span data-ttu-id="fca16-118">屬性</span><span class="sxs-lookup"><span data-stu-id="fca16-118">Attribute</span></span>          | <span data-ttu-id="fca16-119">描述</span><span class="sxs-lookup"><span data-stu-id="fca16-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fca16-120">defaultText</span><span class="sxs-lookup"><span data-stu-id="fca16-120">defaultText</span></span>        | <span data-ttu-id="fca16-121">公用。</span><span class="sxs-lookup"><span data-stu-id="fca16-121">Public.</span></span> <span data-ttu-id="fca16-122">選擇性。</span><span class="sxs-lookup"><span data-stu-id="fca16-122">Optional.</span></span> <span data-ttu-id="fca16-123">如果將值指定給 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) ，但未對應至清單中的其中一個列舉元素，請指定要使用的預設文字。</span><span class="sxs-lookup"><span data-stu-id="fca16-123">Specify default text to use if a value is given to [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) that does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="fca16-124">語法允許直接顯示字串或間接顯示字串參考;使用參考，讓它可以當地語系化。</span><span class="sxs-lookup"><span data-stu-id="fca16-124">The syntax allows for a direct display string or an indirect display string reference; use the reference, so it can be localized.</span></span>                              |
| <span data-ttu-id="fca16-125">useValueForDefault</span><span class="sxs-lookup"><span data-stu-id="fca16-125">useValueForDefault</span></span> | <span data-ttu-id="fca16-126">公用。</span><span class="sxs-lookup"><span data-stu-id="fca16-126">Public.</span></span> <span data-ttu-id="fca16-127">選擇性。</span><span class="sxs-lookup"><span data-stu-id="fca16-127">Optional.</span></span> <span data-ttu-id="fca16-128">將此值設定為 "true" 會通知 IPropertyDescription：： FormatForDisplay 如果值未對應到清單中的其中一個列舉元素，則會通知 [**：：**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 使用此值。</span><span class="sxs-lookup"><span data-stu-id="fca16-128">Setting this to "true" will inform [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) to use the value as-is if the value does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="fca16-129">若為 **IPropertyDescription：： FormatForDisplay**，將此值設定為 "true" 會優先于設定 "defaultText"。</span><span class="sxs-lookup"><span data-stu-id="fca16-129">For **IPropertyDescription::FormatForDisplay**, setting this to "true" takes precedence over setting the "defaultText".</span></span> <span data-ttu-id="fca16-130">預設值為 "false"。</span><span class="sxs-lookup"><span data-stu-id="fca16-130">The default is "false".</span></span> |



 

 

 
