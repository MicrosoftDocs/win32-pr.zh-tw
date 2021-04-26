---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9a790d66d1f7806a7ef86ee4a85f62225aa836
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997705"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="af877-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="af877-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="af877-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="af877-105">This topic is not current.</span></span> <span data-ttu-id="af877-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="af877-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="af877-107">描述延伸超過 neutrals (進入 GCR 適用的彩色色彩) 。</span><span class="sxs-lookup"><span data-stu-id="af877-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="af877-108">0% = 統一元件取代，100% = 灰色元件取代。</span><span class="sxs-lookup"><span data-stu-id="af877-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="af877-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="af877-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="af877-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="af877-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="af877-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="af877-111">Element Information</span></span>



| <span data-ttu-id="af877-112">Name</span><span class="sxs-lookup"><span data-stu-id="af877-112">Name</span></span> | <span data-ttu-id="af877-113">值</span><span class="sxs-lookup"><span data-stu-id="af877-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="af877-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="af877-114">Element Type</span></span> <br/>   | <span data-ttu-id="af877-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="af877-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="af877-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="af877-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="af877-117">頁面</span><span class="sxs-lookup"><span data-stu-id="af877-117">Page</span></span><br/>                                            |
| <span data-ttu-id="af877-118">備註</span><span class="sxs-lookup"><span data-stu-id="af877-118">Notes</span></span> <br/>          | <span data-ttu-id="af877-119">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="af877-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="af877-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="af877-120">Structure Content</span></span>

<span data-ttu-id="af877-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="af877-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="af877-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="af877-122">Structure Properties</span></span>

<span data-ttu-id="af877-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="af877-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="af877-124">屬性</span><span class="sxs-lookup"><span data-stu-id="af877-124">Property</span></span>                | <span data-ttu-id="af877-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="af877-125">xsi:type</span></span>           | <span data-ttu-id="af877-126">值</span><span class="sxs-lookup"><span data-stu-id="af877-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="af877-127">DataType</span><span class="sxs-lookup"><span data-stu-id="af877-127">DataType</span></span><br/>     | <span data-ttu-id="af877-128">字串</span><span class="sxs-lookup"><span data-stu-id="af877-128">string</span></span><br/>  | <span data-ttu-id="af877-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="af877-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="af877-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="af877-130">DefaultValue</span></span><br/> | <span data-ttu-id="af877-131">字串</span><span class="sxs-lookup"><span data-stu-id="af877-131">string</span></span><br/>  | <span data-ttu-id="af877-132">未定義</span><span class="sxs-lookup"><span data-stu-id="af877-132">undefined</span></span><br/>       |
| <span data-ttu-id="af877-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="af877-133">MaxValue</span></span><br/>     | <span data-ttu-id="af877-134">整數</span><span class="sxs-lookup"><span data-stu-id="af877-134">integer</span></span><br/> | <span data-ttu-id="af877-135">100</span><span class="sxs-lookup"><span data-stu-id="af877-135">100</span></span><br/>             |
| <span data-ttu-id="af877-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="af877-136">MinValue</span></span><br/>     | <span data-ttu-id="af877-137">整數</span><span class="sxs-lookup"><span data-stu-id="af877-137">integer</span></span><br/> | <span data-ttu-id="af877-138">0</span><span class="sxs-lookup"><span data-stu-id="af877-138">0</span></span><br/>               |
| <span data-ttu-id="af877-139">多個</span><span class="sxs-lookup"><span data-stu-id="af877-139">Multiple</span></span><br/>     | <span data-ttu-id="af877-140">整數</span><span class="sxs-lookup"><span data-stu-id="af877-140">integer</span></span><br/> | <span data-ttu-id="af877-141">1</span><span class="sxs-lookup"><span data-stu-id="af877-141">1</span></span><br/>               |
| <span data-ttu-id="af877-142">強制性</span><span class="sxs-lookup"><span data-stu-id="af877-142">Mandatory</span></span><br/>    | <span data-ttu-id="af877-143">字串</span><span class="sxs-lookup"><span data-stu-id="af877-143">string</span></span><br/>  | <span data-ttu-id="af877-144">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="af877-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="af877-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="af877-145">UnitType</span></span><br/>     | <span data-ttu-id="af877-146">字串</span><span class="sxs-lookup"><span data-stu-id="af877-146">string</span></span><br/>  | <span data-ttu-id="af877-147">percent</span><span class="sxs-lookup"><span data-stu-id="af877-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="af877-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="af877-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af877-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="af877-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




