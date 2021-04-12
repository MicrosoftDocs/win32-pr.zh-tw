---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fb6866dae4eb4a39de5c2b3b5d678a7388d703
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195823"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="ad05d-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="ad05d-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="ad05d-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ad05d-105">This topic is not current.</span></span> <span data-ttu-id="ad05d-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ad05d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ad05d-107">描述以灰色元件比例 (的彩色筆墨數量) 要加入至 GCR/UCR 產生 "BlackInkLimit" (或 UCAStart 的區域（如果指定的) 在深色 neutrals 和近中立的區域中）。</span><span class="sxs-lookup"><span data-stu-id="ad05d-107">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="ad05d-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ad05d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ad05d-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="ad05d-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ad05d-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ad05d-110">Element Information</span></span>



| <span data-ttu-id="ad05d-111">Name</span><span class="sxs-lookup"><span data-stu-id="ad05d-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="ad05d-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="ad05d-112">Element Type</span></span> <br/>   | <span data-ttu-id="ad05d-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ad05d-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="ad05d-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="ad05d-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ad05d-115">頁面</span><span class="sxs-lookup"><span data-stu-id="ad05d-115">Page</span></span><br/>                                            |
| <span data-ttu-id="ad05d-116">備註</span><span class="sxs-lookup"><span data-stu-id="ad05d-116">Notes</span></span> <br/>          | <span data-ttu-id="ad05d-117">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="ad05d-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ad05d-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="ad05d-118">Structure Content</span></span>

<span data-ttu-id="ad05d-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="ad05d-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="ad05d-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="ad05d-120">Structure Properties</span></span>

<span data-ttu-id="ad05d-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="ad05d-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ad05d-122">屬性</span><span class="sxs-lookup"><span data-stu-id="ad05d-122">Property</span></span>                | <span data-ttu-id="ad05d-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ad05d-123">xsi:type</span></span>           | <span data-ttu-id="ad05d-124">值</span><span class="sxs-lookup"><span data-stu-id="ad05d-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ad05d-125">DataType</span><span class="sxs-lookup"><span data-stu-id="ad05d-125">DataType</span></span><br/>     | <span data-ttu-id="ad05d-126">字串</span><span class="sxs-lookup"><span data-stu-id="ad05d-126">string</span></span><br/>  | <span data-ttu-id="ad05d-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ad05d-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="ad05d-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ad05d-128">DefaultValue</span></span><br/> | <span data-ttu-id="ad05d-129">字串</span><span class="sxs-lookup"><span data-stu-id="ad05d-129">string</span></span><br/>  | <span data-ttu-id="ad05d-130">未定義</span><span class="sxs-lookup"><span data-stu-id="ad05d-130">undefined</span></span><br/>       |
| <span data-ttu-id="ad05d-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ad05d-131">MaxValue</span></span><br/>     | <span data-ttu-id="ad05d-132">整數</span><span class="sxs-lookup"><span data-stu-id="ad05d-132">integer</span></span><br/> | <span data-ttu-id="ad05d-133">100</span><span class="sxs-lookup"><span data-stu-id="ad05d-133">100</span></span><br/>             |
| <span data-ttu-id="ad05d-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="ad05d-134">MinValue</span></span><br/>     | <span data-ttu-id="ad05d-135">整數</span><span class="sxs-lookup"><span data-stu-id="ad05d-135">integer</span></span><br/> | <span data-ttu-id="ad05d-136">0</span><span class="sxs-lookup"><span data-stu-id="ad05d-136">0</span></span><br/>               |
| <span data-ttu-id="ad05d-137">多個</span><span class="sxs-lookup"><span data-stu-id="ad05d-137">Multiple</span></span><br/>     | <span data-ttu-id="ad05d-138">整數</span><span class="sxs-lookup"><span data-stu-id="ad05d-138">integer</span></span><br/> | <span data-ttu-id="ad05d-139">1</span><span class="sxs-lookup"><span data-stu-id="ad05d-139">1</span></span><br/>               |
| <span data-ttu-id="ad05d-140">強制性</span><span class="sxs-lookup"><span data-stu-id="ad05d-140">Mandatory</span></span><br/>    | <span data-ttu-id="ad05d-141">字串</span><span class="sxs-lookup"><span data-stu-id="ad05d-141">string</span></span><br/>  | <span data-ttu-id="ad05d-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="ad05d-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ad05d-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="ad05d-143">UnitType</span></span><br/>     | <span data-ttu-id="ad05d-144">字串</span><span class="sxs-lookup"><span data-stu-id="ad05d-144">string</span></span><br/>  | <span data-ttu-id="ad05d-145">percent</span><span class="sxs-lookup"><span data-stu-id="ad05d-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ad05d-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad05d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad05d-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ad05d-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




