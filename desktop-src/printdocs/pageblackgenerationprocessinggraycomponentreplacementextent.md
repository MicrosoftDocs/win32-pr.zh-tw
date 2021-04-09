---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c71700b23459c087361e9e28ac0c43120aff90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103853540"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="809cb-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="809cb-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="809cb-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="809cb-105">This topic is not current.</span></span> <span data-ttu-id="809cb-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="809cb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="809cb-107">描述延伸超過 neutrals (進入 GCR 適用的彩色色彩) 。</span><span class="sxs-lookup"><span data-stu-id="809cb-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="809cb-108">0% = 統一元件取代，100% = 灰色元件取代。</span><span class="sxs-lookup"><span data-stu-id="809cb-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="809cb-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="809cb-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="809cb-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="809cb-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="809cb-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="809cb-111">Element Information</span></span>



| <span data-ttu-id="809cb-112">Name</span><span class="sxs-lookup"><span data-stu-id="809cb-112">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="809cb-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="809cb-113">Element Type</span></span> <br/>   | <span data-ttu-id="809cb-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="809cb-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="809cb-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="809cb-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="809cb-116">頁面</span><span class="sxs-lookup"><span data-stu-id="809cb-116">Page</span></span><br/>                                            |
| <span data-ttu-id="809cb-117">備註</span><span class="sxs-lookup"><span data-stu-id="809cb-117">Notes</span></span> <br/>          | <span data-ttu-id="809cb-118">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="809cb-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="809cb-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="809cb-119">Structure Content</span></span>

<span data-ttu-id="809cb-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="809cb-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="809cb-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="809cb-121">Structure Properties</span></span>

<span data-ttu-id="809cb-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="809cb-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="809cb-123">屬性</span><span class="sxs-lookup"><span data-stu-id="809cb-123">Property</span></span>                | <span data-ttu-id="809cb-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="809cb-124">xsi:type</span></span>           | <span data-ttu-id="809cb-125">值</span><span class="sxs-lookup"><span data-stu-id="809cb-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="809cb-126">DataType</span><span class="sxs-lookup"><span data-stu-id="809cb-126">DataType</span></span><br/>     | <span data-ttu-id="809cb-127">字串</span><span class="sxs-lookup"><span data-stu-id="809cb-127">string</span></span><br/>  | <span data-ttu-id="809cb-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="809cb-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="809cb-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="809cb-129">DefaultValue</span></span><br/> | <span data-ttu-id="809cb-130">字串</span><span class="sxs-lookup"><span data-stu-id="809cb-130">string</span></span><br/>  | <span data-ttu-id="809cb-131">未定義</span><span class="sxs-lookup"><span data-stu-id="809cb-131">undefined</span></span><br/>       |
| <span data-ttu-id="809cb-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="809cb-132">MaxValue</span></span><br/>     | <span data-ttu-id="809cb-133">整數</span><span class="sxs-lookup"><span data-stu-id="809cb-133">integer</span></span><br/> | <span data-ttu-id="809cb-134">100</span><span class="sxs-lookup"><span data-stu-id="809cb-134">100</span></span><br/>             |
| <span data-ttu-id="809cb-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="809cb-135">MinValue</span></span><br/>     | <span data-ttu-id="809cb-136">整數</span><span class="sxs-lookup"><span data-stu-id="809cb-136">integer</span></span><br/> | <span data-ttu-id="809cb-137">0</span><span class="sxs-lookup"><span data-stu-id="809cb-137">0</span></span><br/>               |
| <span data-ttu-id="809cb-138">多個</span><span class="sxs-lookup"><span data-stu-id="809cb-138">Multiple</span></span><br/>     | <span data-ttu-id="809cb-139">整數</span><span class="sxs-lookup"><span data-stu-id="809cb-139">integer</span></span><br/> | <span data-ttu-id="809cb-140">1</span><span class="sxs-lookup"><span data-stu-id="809cb-140">1</span></span><br/>               |
| <span data-ttu-id="809cb-141">強制性</span><span class="sxs-lookup"><span data-stu-id="809cb-141">Mandatory</span></span><br/>    | <span data-ttu-id="809cb-142">字串</span><span class="sxs-lookup"><span data-stu-id="809cb-142">string</span></span><br/>  | <span data-ttu-id="809cb-143">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="809cb-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="809cb-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="809cb-144">UnitType</span></span><br/>     | <span data-ttu-id="809cb-145">字串</span><span class="sxs-lookup"><span data-stu-id="809cb-145">string</span></span><br/>  | <span data-ttu-id="809cb-146">percent</span><span class="sxs-lookup"><span data-stu-id="809cb-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="809cb-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="809cb-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="809cb-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="809cb-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




