---
description: PageBlackGenerationProcessingGrayComponentReplacementExtent 參數會將超出 neutrals 的範圍描述為 GCR 套用的彩色色彩。
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3bd5e4fdbafba97884a7aed608b23e4c26ce1c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408501"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="c43f0-103">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="c43f0-103">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="c43f0-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="c43f0-104">This topic is not current.</span></span> <span data-ttu-id="c43f0-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="c43f0-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c43f0-106">描述延伸超過 neutrals (進入 GCR 適用的彩色色彩) 。</span><span class="sxs-lookup"><span data-stu-id="c43f0-106">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="c43f0-107">0% = 統一元件取代，100% = 灰色元件取代。</span><span class="sxs-lookup"><span data-stu-id="c43f0-107">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="c43f0-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c43f0-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c43f0-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="c43f0-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c43f0-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c43f0-110">Element Information</span></span>



| <span data-ttu-id="c43f0-111">Name</span><span class="sxs-lookup"><span data-stu-id="c43f0-111">Name</span></span> | <span data-ttu-id="c43f0-112">值</span><span class="sxs-lookup"><span data-stu-id="c43f0-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="c43f0-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="c43f0-113">Element Type</span></span> <br/>   | <span data-ttu-id="c43f0-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c43f0-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="c43f0-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="c43f0-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c43f0-116">頁面</span><span class="sxs-lookup"><span data-stu-id="c43f0-116">Page</span></span><br/>                                            |
| <span data-ttu-id="c43f0-117">備註</span><span class="sxs-lookup"><span data-stu-id="c43f0-117">Notes</span></span> <br/>          | <span data-ttu-id="c43f0-118">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="c43f0-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c43f0-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="c43f0-119">Structure Content</span></span>

<span data-ttu-id="c43f0-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="c43f0-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="c43f0-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="c43f0-121">Structure Properties</span></span>

<span data-ttu-id="c43f0-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="c43f0-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c43f0-123">屬性</span><span class="sxs-lookup"><span data-stu-id="c43f0-123">Property</span></span>                | <span data-ttu-id="c43f0-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c43f0-124">xsi:type</span></span>           | <span data-ttu-id="c43f0-125">值</span><span class="sxs-lookup"><span data-stu-id="c43f0-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c43f0-126">DataType</span><span class="sxs-lookup"><span data-stu-id="c43f0-126">DataType</span></span><br/>     | <span data-ttu-id="c43f0-127">字串</span><span class="sxs-lookup"><span data-stu-id="c43f0-127">string</span></span><br/>  | <span data-ttu-id="c43f0-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c43f0-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="c43f0-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c43f0-129">DefaultValue</span></span><br/> | <span data-ttu-id="c43f0-130">字串</span><span class="sxs-lookup"><span data-stu-id="c43f0-130">string</span></span><br/>  | <span data-ttu-id="c43f0-131">未定義</span><span class="sxs-lookup"><span data-stu-id="c43f0-131">undefined</span></span><br/>       |
| <span data-ttu-id="c43f0-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c43f0-132">MaxValue</span></span><br/>     | <span data-ttu-id="c43f0-133">整數</span><span class="sxs-lookup"><span data-stu-id="c43f0-133">integer</span></span><br/> | <span data-ttu-id="c43f0-134">100</span><span class="sxs-lookup"><span data-stu-id="c43f0-134">100</span></span><br/>             |
| <span data-ttu-id="c43f0-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="c43f0-135">MinValue</span></span><br/>     | <span data-ttu-id="c43f0-136">整數</span><span class="sxs-lookup"><span data-stu-id="c43f0-136">integer</span></span><br/> | <span data-ttu-id="c43f0-137">0</span><span class="sxs-lookup"><span data-stu-id="c43f0-137">0</span></span><br/>               |
| <span data-ttu-id="c43f0-138">多個</span><span class="sxs-lookup"><span data-stu-id="c43f0-138">Multiple</span></span><br/>     | <span data-ttu-id="c43f0-139">整數</span><span class="sxs-lookup"><span data-stu-id="c43f0-139">integer</span></span><br/> | <span data-ttu-id="c43f0-140">1</span><span class="sxs-lookup"><span data-stu-id="c43f0-140">1</span></span><br/>               |
| <span data-ttu-id="c43f0-141">強制性</span><span class="sxs-lookup"><span data-stu-id="c43f0-141">Mandatory</span></span><br/>    | <span data-ttu-id="c43f0-142">string</span><span class="sxs-lookup"><span data-stu-id="c43f0-142">string</span></span><br/>  | <span data-ttu-id="c43f0-143">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="c43f0-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c43f0-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="c43f0-144">UnitType</span></span><br/>     | <span data-ttu-id="c43f0-145">string</span><span class="sxs-lookup"><span data-stu-id="c43f0-145">string</span></span><br/>  | <span data-ttu-id="c43f0-146">percent</span><span class="sxs-lookup"><span data-stu-id="c43f0-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="c43f0-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="c43f0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c43f0-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="c43f0-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




