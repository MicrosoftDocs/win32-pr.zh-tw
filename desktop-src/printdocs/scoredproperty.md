---
description: 尋找 ScoredProperty 元素的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb93fbdaeb6101cbd1ff75d6c0b3a829afe0d317
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119113"
---
# <a name="scoredproperty"></a><span data-ttu-id="28b30-105">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="28b30-105">ScoredProperty</span></span>

<span data-ttu-id="28b30-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="28b30-106">This topic is not current.</span></span> <span data-ttu-id="28b30-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="28b30-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="28b30-108">ScoredProperty 元素會宣告選項定義內建的屬性。</span><span class="sxs-lookup"><span data-stu-id="28b30-108">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="28b30-109">當評估要求的選項符合裝置支援的選項時，應該比較這類屬性。</span><span class="sxs-lookup"><span data-stu-id="28b30-109">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="28b30-110">元素標記</span><span class="sxs-lookup"><span data-stu-id="28b30-110">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="28b30-111">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="28b30-111">XML Attributes</span></span>

<span data-ttu-id="28b30-112">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="28b30-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="28b30-113">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="28b30-113">XML Attribute</span></span>   | <span data-ttu-id="28b30-114">詳細資料</span><span class="sxs-lookup"><span data-stu-id="28b30-114">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28b30-115">NAME</span><span class="sxs-lookup"><span data-stu-id="28b30-115">name</span></span><br/> | <span data-ttu-id="28b30-116">保留 ScoredProperty 的 name 屬性，也就是標準屬性或私用定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="28b30-116">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="28b30-117">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="28b30-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="28b30-118">項目資訊</span><span class="sxs-lookup"><span data-stu-id="28b30-118">Element Information</span></span>

<span data-ttu-id="28b30-119">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="28b30-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="28b30-120">類別</span><span class="sxs-lookup"><span data-stu-id="28b30-120">Category</span></span>                   | <span data-ttu-id="28b30-121">詳細資料</span><span class="sxs-lookup"><span data-stu-id="28b30-121">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28b30-122">父元素</span><span class="sxs-lookup"><span data-stu-id="28b30-122">Parent elements</span></span><br/> | <span data-ttu-id="28b30-123">*選項*</span><span class="sxs-lookup"><span data-stu-id="28b30-123">*Option*</span></span><br/> <span data-ttu-id="28b30-124">*ScoredProperty*</span><span class="sxs-lookup"><span data-stu-id="28b30-124">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="28b30-125">子元素</span><span class="sxs-lookup"><span data-stu-id="28b30-125">Child elements</span></span><br/>  | <span data-ttu-id="28b30-126">或</span><span class="sxs-lookup"><span data-stu-id="28b30-126">Either</span></span><br/> <span data-ttu-id="28b30-127">*ParameterRef* (一) </span><span class="sxs-lookup"><span data-stu-id="28b30-127">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="28b30-128">或</span><span class="sxs-lookup"><span data-stu-id="28b30-128">or</span></span><br/> <span data-ttu-id="28b30-129">*值* (一) </span><span class="sxs-lookup"><span data-stu-id="28b30-129">*Value* (one)</span></span><br/> <span data-ttu-id="28b30-130">*屬性* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="28b30-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="28b30-131">*ScoredProperty* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="28b30-131">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="28b30-132">這個元素</span><span class="sxs-lookup"><span data-stu-id="28b30-132">This element</span></span><br/>    | <span data-ttu-id="28b30-133">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="28b30-133">No character data is permitted.</span></span><br/> <span data-ttu-id="28b30-134">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="28b30-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="28b30-135">設定相依性</span><span class="sxs-lookup"><span data-stu-id="28b30-135">Configuration Dependencies</span></span>

<span data-ttu-id="28b30-136">ScoredProperty 元素可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="28b30-136">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="28b30-137">範例</span><span class="sxs-lookup"><span data-stu-id="28b30-137">Example</span></span>

<span data-ttu-id="28b30-138">宣告名為 MediaSizeWidth 的 ScoredProperty 元素，其值為11。</span><span class="sxs-lookup"><span data-stu-id="28b30-138">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="28b30-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="28b30-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28b30-140">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="28b30-140">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




