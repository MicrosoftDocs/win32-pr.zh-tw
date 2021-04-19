---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: 值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a8f8c5bf9e2ec1696d6282b859fc99b7701159
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986026"
---
# <a name="value"></a><span data-ttu-id="bc094-104">值</span><span class="sxs-lookup"><span data-stu-id="bc094-104">Value</span></span>

<span data-ttu-id="bc094-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="bc094-105">This topic is not current.</span></span> <span data-ttu-id="bc094-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="bc094-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bc094-107">值元素會將常值與型別產生關聯。</span><span class="sxs-lookup"><span data-stu-id="bc094-107">A Value element associates a literal with a type.</span></span>

## <a name="element-tag"></a><span data-ttu-id="bc094-108">元素標記</span><span class="sxs-lookup"><span data-stu-id="bc094-108">Element Tag</span></span>

<Value>

## <a name="xml-attributes"></a><span data-ttu-id="bc094-109">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="bc094-109">XML Attributes</span></span>

<span data-ttu-id="bc094-110">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="bc094-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="bc094-111">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="bc094-111">XML Attribute</span></span>       | <span data-ttu-id="bc094-112">詳細資料</span><span class="sxs-lookup"><span data-stu-id="bc094-112">Details</span></span>                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc094-113">xsi:type</span><span class="sxs-lookup"><span data-stu-id="bc094-113">xsi:type</span></span><br/> | <span data-ttu-id="bc094-114">指定值的資料類型，其必須是下列其中一個 XSD 定義類型： string、integer、decimal、QName。</span><span class="sxs-lookup"><span data-stu-id="bc094-114">Specifies the data type of Value, which must be one of the following XSD-defined types: string, integer, decimal, QName.</span></span> <span data-ttu-id="bc094-115">如果遺失，則預設資料類型為 string。</span><span class="sxs-lookup"><span data-stu-id="bc094-115">If missing, the default data type is string.</span></span><br/> |



 

<span data-ttu-id="bc094-116">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="bc094-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="bc094-117">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bc094-117">Element Information</span></span>

<span data-ttu-id="bc094-118">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="bc094-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="bc094-119">類別</span><span class="sxs-lookup"><span data-stu-id="bc094-119">Category</span></span>                   | <span data-ttu-id="bc094-120">詳細資料</span><span class="sxs-lookup"><span data-stu-id="bc094-120">Details</span></span>                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc094-121">父元素</span><span class="sxs-lookup"><span data-stu-id="bc094-121">Parent elements</span></span><br/> | <span data-ttu-id="bc094-122">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="bc094-122">ParameterInit</span></span> <br/> <span data-ttu-id="bc094-123">屬性</span><span class="sxs-lookup"><span data-stu-id="bc094-123">Property</span></span><br/> <span data-ttu-id="bc094-124">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="bc094-124">ScoredProperty</span></span><br/>                                                                                   |
| <span data-ttu-id="bc094-125">子元素</span><span class="sxs-lookup"><span data-stu-id="bc094-125">Child elements</span></span><br/>  | <span data-ttu-id="bc094-126">只允許字元或整數內容。</span><span class="sxs-lookup"><span data-stu-id="bc094-126">Only character or integer content is permitted.</span></span><br/>                                                                                                |
| <span data-ttu-id="bc094-127">這個元素</span><span class="sxs-lookup"><span data-stu-id="bc094-127">This element</span></span><br/>    | <span data-ttu-id="bc094-128">允許 Null 內容。</span><span class="sxs-lookup"><span data-stu-id="bc094-128">Null content is allowed.</span></span> <span data-ttu-id="bc094-129">字元內容必須符合資料類型所定義的語法。</span><span class="sxs-lookup"><span data-stu-id="bc094-129">Character content must conform to syntax defined by data type.</span></span><br/> <span data-ttu-id="bc094-130">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="bc094-130">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="bc094-131">設定相依性</span><span class="sxs-lookup"><span data-stu-id="bc094-131">Configuration Dependencies</span></span>

<span data-ttu-id="bc094-132">出現在 ScoredProperty 元素內的值元素可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="bc094-132">Value elements that appear within ScoredProperty element may not have any configuration dependencies.</span></span> <span data-ttu-id="bc094-133">出現在屬性專案內的值元素可能會對設定有任意的相依性。</span><span class="sxs-lookup"><span data-stu-id="bc094-133">Value elements that appear within Property elements may have arbitrary dependencies on the configuration.</span></span>

## <a name="element-usage"></a><span data-ttu-id="bc094-134">專案使用方式</span><span class="sxs-lookup"><span data-stu-id="bc094-134">Element Usage</span></span>

<span data-ttu-id="bc094-135">值元素可能會出現在屬性或 ScoredProperty 元素中。</span><span class="sxs-lookup"><span data-stu-id="bc094-135">A Value element may appear within a Property or ScoredProperty element.</span></span> <span data-ttu-id="bc094-136">Value 元素的目的是要將值表示為標準 XML 資料類型。</span><span class="sxs-lookup"><span data-stu-id="bc094-136">The purpose of the Value element is to represent a value as a standard XML data type.</span></span> <span data-ttu-id="bc094-137">資料類型會指定為 Value 元素（xsi： type）的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="bc094-137">The data type is specified as an XML attribute of the Value element, xsi:type.</span></span> <span data-ttu-id="bc094-138">請注意，不支援所有 XSD 定義或 XML 定義的類型。</span><span class="sxs-lookup"><span data-stu-id="bc094-138">Note that not all XSD-defined or XML-defined types are supported.</span></span> <span data-ttu-id="bc094-139">如需支援類型的清單，請參閱 [元素類型的摘要](summary-of-element-types.md)。</span><span class="sxs-lookup"><span data-stu-id="bc094-139">For a list of supported types, see [Summary of Element Types](summary-of-element-types.md).</span></span> <span data-ttu-id="bc094-140">值元素只能包含字元內容。</span><span class="sxs-lookup"><span data-stu-id="bc094-140">A Value element can contain only character content.</span></span> <span data-ttu-id="bc094-141">任何其他專案可能會顯示為值元素中的內容。</span><span class="sxs-lookup"><span data-stu-id="bc094-141">Nothing else may appear as content in a Value element.</span></span>

> [!Note]  
> <span data-ttu-id="bc094-142">某些列印架構定義的屬性和 ScoredProperty 元素不包含值元素，因為它們的用途只是子屬性的父系。</span><span class="sxs-lookup"><span data-stu-id="bc094-142">Some Print Schema-defined Property and ScoredProperty elements do not contain a Value element, because their purpose is simply to be parents of subproperties.</span></span> <span data-ttu-id="bc094-143">您不應該將值專案加入至這些屬性（property），這些屬性不包含值元素。</span><span class="sxs-lookup"><span data-stu-id="bc094-143">You should not add a Value element to such properties as these, properties that do not contain a Value element.</span></span>

 

<span data-ttu-id="bc094-144">若要符合 Print Schema Framework （需要值元素或子項目存在於支援值的元素中），則應該將值元素呈現為空白元素來表示不存在或未定義的值。也就是</span><span class="sxs-lookup"><span data-stu-id="bc094-144">To conform to the Print Schema Framework, which requires either a Value element or subelements be present in the elements that support values, an absent or undefined value should be represented by presenting the Value element as an empty element; that is, as</span></span> <Value></Value><span data-ttu-id="bc094-145">.</span><span class="sxs-lookup"><span data-stu-id="bc094-145">.</span></span>

## <a name="example"></a><span data-ttu-id="bc094-146">範例</span><span class="sxs-lookup"><span data-stu-id="bc094-146">Example</span></span>

<span data-ttu-id="bc094-147">定義 decimal 類型的值，並將其初始化為 "128.5"。</span><span class="sxs-lookup"><span data-stu-id="bc094-147">Define a Value of type decimal and initialize it to "128.5".</span></span>

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a><span data-ttu-id="bc094-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc094-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc094-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="bc094-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




