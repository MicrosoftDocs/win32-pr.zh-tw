---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106988116"
---
# <a name="scoredproperty"></a><span data-ttu-id="09089-104">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="09089-104">ScoredProperty</span></span>

<span data-ttu-id="09089-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="09089-105">This topic is not current.</span></span> <span data-ttu-id="09089-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="09089-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="09089-107">ScoredProperty 元素會宣告選項定義內建的屬性。</span><span class="sxs-lookup"><span data-stu-id="09089-107">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="09089-108">當評估要求的選項符合裝置支援的選項時，應該比較這類屬性。</span><span class="sxs-lookup"><span data-stu-id="09089-108">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="09089-109">元素標記</span><span class="sxs-lookup"><span data-stu-id="09089-109">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="09089-110">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="09089-110">XML Attributes</span></span>

<span data-ttu-id="09089-111">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="09089-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="09089-112">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="09089-112">XML Attribute</span></span>   | <span data-ttu-id="09089-113">詳細資料</span><span class="sxs-lookup"><span data-stu-id="09089-113">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09089-114">NAME</span><span class="sxs-lookup"><span data-stu-id="09089-114">name</span></span><br/> | <span data-ttu-id="09089-115">保留 ScoredProperty 的 name 屬性，也就是標準屬性或私用定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="09089-115">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="09089-116">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="09089-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="09089-117">項目資訊</span><span class="sxs-lookup"><span data-stu-id="09089-117">Element Information</span></span>

<span data-ttu-id="09089-118">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="09089-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="09089-119">類別</span><span class="sxs-lookup"><span data-stu-id="09089-119">Category</span></span>                   | <span data-ttu-id="09089-120">詳細資料</span><span class="sxs-lookup"><span data-stu-id="09089-120">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09089-121">父元素</span><span class="sxs-lookup"><span data-stu-id="09089-121">Parent elements</span></span><br/> | <span data-ttu-id="09089-122">*選項*</span><span class="sxs-lookup"><span data-stu-id="09089-122">*Option*</span></span><br/> <span data-ttu-id="09089-123">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="09089-123">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="09089-124">子元素</span><span class="sxs-lookup"><span data-stu-id="09089-124">Child elements</span></span><br/>  | <span data-ttu-id="09089-125">或</span><span class="sxs-lookup"><span data-stu-id="09089-125">Either</span></span><br/> <span data-ttu-id="09089-126">*ParameterRef* (一) </span><span class="sxs-lookup"><span data-stu-id="09089-126">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="09089-127">或</span><span class="sxs-lookup"><span data-stu-id="09089-127">or</span></span><br/> <span data-ttu-id="09089-128">*值* (一) </span><span class="sxs-lookup"><span data-stu-id="09089-128">*Value* (one)</span></span><br/> <span data-ttu-id="09089-129">*屬性* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="09089-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="09089-130">*ScoredProperty* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="09089-130">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="09089-131">這個元素</span><span class="sxs-lookup"><span data-stu-id="09089-131">This element</span></span><br/>    | <span data-ttu-id="09089-132">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="09089-132">No character data is permitted.</span></span><br/> <span data-ttu-id="09089-133">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="09089-133">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="09089-134">設定相依性</span><span class="sxs-lookup"><span data-stu-id="09089-134">Configuration Dependencies</span></span>

<span data-ttu-id="09089-135">ScoredProperty 元素可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="09089-135">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="09089-136">範例</span><span class="sxs-lookup"><span data-stu-id="09089-136">Example</span></span>

<span data-ttu-id="09089-137">宣告名為 MediaSizeWidth 的 ScoredProperty 元素，其值為11。</span><span class="sxs-lookup"><span data-stu-id="09089-137">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="09089-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="09089-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09089-139">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="09089-139">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




