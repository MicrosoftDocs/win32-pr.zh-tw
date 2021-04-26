---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1b43d8d9ee366fc742dc3d7b1617f6297fc96e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995665"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="846f3-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="846f3-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="846f3-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="846f3-105">This topic is not current.</span></span> <span data-ttu-id="846f3-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="846f3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="846f3-107">描述以灰色元件比例 (的彩色筆墨數量) 要加入至 GCR/UCR 產生 "BlackInkLimit" (或 UCAStart 的區域（如果指定的) 在深色 neutrals 和近中立的區域中）。</span><span class="sxs-lookup"><span data-stu-id="846f3-107">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="846f3-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="846f3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="846f3-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="846f3-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="846f3-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="846f3-110">Element Information</span></span>



| <span data-ttu-id="846f3-111">Name</span><span class="sxs-lookup"><span data-stu-id="846f3-111">Name</span></span> | <span data-ttu-id="846f3-112">值</span><span class="sxs-lookup"><span data-stu-id="846f3-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="846f3-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="846f3-113">Element Type</span></span> <br/>   | <span data-ttu-id="846f3-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="846f3-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="846f3-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="846f3-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="846f3-116">頁面</span><span class="sxs-lookup"><span data-stu-id="846f3-116">Page</span></span><br/>                                            |
| <span data-ttu-id="846f3-117">備註</span><span class="sxs-lookup"><span data-stu-id="846f3-117">Notes</span></span> <br/>          | <span data-ttu-id="846f3-118">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="846f3-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="846f3-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="846f3-119">Structure Content</span></span>

<span data-ttu-id="846f3-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="846f3-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="846f3-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="846f3-121">Structure Properties</span></span>

<span data-ttu-id="846f3-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="846f3-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="846f3-123">屬性</span><span class="sxs-lookup"><span data-stu-id="846f3-123">Property</span></span>                | <span data-ttu-id="846f3-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="846f3-124">xsi:type</span></span>           | <span data-ttu-id="846f3-125">值</span><span class="sxs-lookup"><span data-stu-id="846f3-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="846f3-126">DataType</span><span class="sxs-lookup"><span data-stu-id="846f3-126">DataType</span></span><br/>     | <span data-ttu-id="846f3-127">字串</span><span class="sxs-lookup"><span data-stu-id="846f3-127">string</span></span><br/>  | <span data-ttu-id="846f3-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="846f3-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="846f3-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="846f3-129">DefaultValue</span></span><br/> | <span data-ttu-id="846f3-130">字串</span><span class="sxs-lookup"><span data-stu-id="846f3-130">string</span></span><br/>  | <span data-ttu-id="846f3-131">未定義</span><span class="sxs-lookup"><span data-stu-id="846f3-131">undefined</span></span><br/>       |
| <span data-ttu-id="846f3-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="846f3-132">MaxValue</span></span><br/>     | <span data-ttu-id="846f3-133">整數</span><span class="sxs-lookup"><span data-stu-id="846f3-133">integer</span></span><br/> | <span data-ttu-id="846f3-134">100</span><span class="sxs-lookup"><span data-stu-id="846f3-134">100</span></span><br/>             |
| <span data-ttu-id="846f3-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="846f3-135">MinValue</span></span><br/>     | <span data-ttu-id="846f3-136">整數</span><span class="sxs-lookup"><span data-stu-id="846f3-136">integer</span></span><br/> | <span data-ttu-id="846f3-137">0</span><span class="sxs-lookup"><span data-stu-id="846f3-137">0</span></span><br/>               |
| <span data-ttu-id="846f3-138">多個</span><span class="sxs-lookup"><span data-stu-id="846f3-138">Multiple</span></span><br/>     | <span data-ttu-id="846f3-139">整數</span><span class="sxs-lookup"><span data-stu-id="846f3-139">integer</span></span><br/> | <span data-ttu-id="846f3-140">1</span><span class="sxs-lookup"><span data-stu-id="846f3-140">1</span></span><br/>               |
| <span data-ttu-id="846f3-141">強制性</span><span class="sxs-lookup"><span data-stu-id="846f3-141">Mandatory</span></span><br/>    | <span data-ttu-id="846f3-142">字串</span><span class="sxs-lookup"><span data-stu-id="846f3-142">string</span></span><br/>  | <span data-ttu-id="846f3-143">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="846f3-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="846f3-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="846f3-144">UnitType</span></span><br/>     | <span data-ttu-id="846f3-145">字串</span><span class="sxs-lookup"><span data-stu-id="846f3-145">string</span></span><br/>  | <span data-ttu-id="846f3-146">percent</span><span class="sxs-lookup"><span data-stu-id="846f3-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="846f3-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="846f3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="846f3-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="846f3-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




