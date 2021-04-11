---
description: 將列舉文字指派給某個範圍的值。 每個 enumRange 元素都會指定最小值，並延伸到下一個元素的最小值，或直到沒有其他 enumRange 元素為止。
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943855"
---
# <a name="enumrange"></a><span data-ttu-id="653b7-104">enumRange</span><span class="sxs-lookup"><span data-stu-id="653b7-104">enumRange</span></span>

<span data-ttu-id="653b7-105">將列舉文字指派給某個範圍的值。</span><span class="sxs-lookup"><span data-stu-id="653b7-105">Assigns enumeration text to a range of values.</span></span> <span data-ttu-id="653b7-106">每個 [enumRange]() 元素都會指定最小值，並延伸到下一個元素的最小值，或直到沒有其他 enumRange 元素為止。</span><span class="sxs-lookup"><span data-stu-id="653b7-106">Each [enumRange]() element specifies a minimum value, and extends until the next element minimum value, or until there are no more enumRange elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="653b7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="653b7-107">Syntax</span></span>

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="653b7-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="653b7-108">Element Information</span></span>



| <span data-ttu-id="653b7-109">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="653b7-109">Parent Element</span></span>                                         | <span data-ttu-id="653b7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="653b7-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="653b7-111">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="653b7-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="653b7-112">無</span><span class="sxs-lookup"><span data-stu-id="653b7-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="653b7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="653b7-113">Attributes</span></span>



| <span data-ttu-id="653b7-114">屬性</span><span class="sxs-lookup"><span data-stu-id="653b7-114">Attribute</span></span> | <span data-ttu-id="653b7-115">描述</span><span class="sxs-lookup"><span data-stu-id="653b7-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="653b7-116">minValue</span><span class="sxs-lookup"><span data-stu-id="653b7-116">minValue</span></span>  | <span data-ttu-id="653b7-117">公用。</span><span class="sxs-lookup"><span data-stu-id="653b7-117">Public.</span></span> <span data-ttu-id="653b7-118">必要。</span><span class="sxs-lookup"><span data-stu-id="653b7-118">Required.</span></span> <span data-ttu-id="653b7-119">範圍中的最小值。</span><span class="sxs-lookup"><span data-stu-id="653b7-119">The minimum value in the range.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="653b7-120">setValue</span><span class="sxs-lookup"><span data-stu-id="653b7-120">setValue</span></span>  | <span data-ttu-id="653b7-121">公用。</span><span class="sxs-lookup"><span data-stu-id="653b7-121">Public.</span></span> <span data-ttu-id="653b7-122">選擇性。</span><span class="sxs-lookup"><span data-stu-id="653b7-122">Optional.</span></span> <span data-ttu-id="653b7-123">當使用者從 listbox 屬性控制項選取這個列舉時，此離散值會被指派為屬性值。</span><span class="sxs-lookup"><span data-stu-id="653b7-123">When a user selects this enumeration from a listbox property control, this discrete value is assigned as the property value.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="653b7-124">text</span><span class="sxs-lookup"><span data-stu-id="653b7-124">text</span></span>      | <span data-ttu-id="653b7-125">公用。</span><span class="sxs-lookup"><span data-stu-id="653b7-125">Public.</span></span> <span data-ttu-id="653b7-126">選擇性。</span><span class="sxs-lookup"><span data-stu-id="653b7-126">Optional.</span></span> <span data-ttu-id="653b7-127">用來顯示列舉值的文字。</span><span class="sxs-lookup"><span data-stu-id="653b7-127">The text used to display the enumerated value.</span></span> <span data-ttu-id="653b7-128">語法允許直接顯示字串或間接顯示字串參考;使用間接顯示字串，使其可以當地語系化。</span><span class="sxs-lookup"><span data-stu-id="653b7-128">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="653b7-129">助憶鍵</span><span class="sxs-lookup"><span data-stu-id="653b7-129">mnemonics</span></span> | <span data-ttu-id="653b7-130">**Windows 7 和更新版本。**</span><span class="sxs-lookup"><span data-stu-id="653b7-130">**Windows 7 and later.**</span></span> <span data-ttu-id="653b7-131">公用。</span><span class="sxs-lookup"><span data-stu-id="653b7-131">Public.</span></span> <span data-ttu-id="653b7-132">選擇性。</span><span class="sxs-lookup"><span data-stu-id="653b7-132">Optional.</span></span> <span data-ttu-id="653b7-133">助憶鍵值的清單，可用來參考搜尋查詢中的屬性。</span><span class="sxs-lookup"><span data-stu-id="653b7-133">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="653b7-134">此清單以 ' \| ' 字元分隔。</span><span class="sxs-lookup"><span data-stu-id="653b7-134">The list is delimited with the '\|' character.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="653b7-135">NAME</span><span class="sxs-lookup"><span data-stu-id="653b7-135">name</span></span>      | <span data-ttu-id="653b7-136">必要。</span><span class="sxs-lookup"><span data-stu-id="653b7-136">Required.</span></span> <span data-ttu-id="653b7-137">標準屬性名稱，對系統而言是唯一的;例如，系統評等。</span><span class="sxs-lookup"><span data-stu-id="653b7-137">The canonical property name, unique to the system; for example, System.Rating.</span></span> <span data-ttu-id="653b7-138">這個屬性的限制為64個字元。</span><span class="sxs-lookup"><span data-stu-id="653b7-138">This attribute is limited to 64 characters.</span></span> <span data-ttu-id="653b7-139">名稱區分大小寫，且應使用下列語法： PropertyName。</span><span class="sxs-lookup"><span data-stu-id="653b7-139">The name is case sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="653b7-140">下列方法會傳回這個值： [**IExplorerCommand：： GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname)、 [**IPropertyDescription：： GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname)、 [**IPropertyDescription2：： GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)和 [**IPropertyUI：： GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="653b7-140">The following methods return this value: [**IExplorerCommand::GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2::GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2), and [**IPropertyUI::GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span></span> |



 

 

 
