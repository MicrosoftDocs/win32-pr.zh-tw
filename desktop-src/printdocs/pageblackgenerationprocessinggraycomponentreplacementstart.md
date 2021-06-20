---
description: 深入瞭解 PageBlackGenerationProcessingGrayComponentReplacementStart 元素，其描述 GCR 應開始的位置。
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e7e5a7e22c20b15dc373a2cce2bfe19e3417d4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408461"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="6d462-103">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="6d462-103">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="6d462-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="6d462-104">This topic is not current.</span></span> <span data-ttu-id="6d462-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="6d462-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6d462-106">描述「反白顯示陰影」範圍中的點，其中 GCR 應開始 (100% 的最深陰影) 。</span><span class="sxs-lookup"><span data-stu-id="6d462-106">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="6d462-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6d462-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6d462-108">結構內容</span><span class="sxs-lookup"><span data-stu-id="6d462-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6d462-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6d462-109">Element Information</span></span>



| <span data-ttu-id="6d462-110">Name</span><span class="sxs-lookup"><span data-stu-id="6d462-110">Name</span></span> | <span data-ttu-id="6d462-111">值</span><span class="sxs-lookup"><span data-stu-id="6d462-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="6d462-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="6d462-112">Element Type</span></span> <br/>   | <span data-ttu-id="6d462-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6d462-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="6d462-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="6d462-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6d462-115">頁面</span><span class="sxs-lookup"><span data-stu-id="6d462-115">Page</span></span><br/>                                            |
| <span data-ttu-id="6d462-116">備註</span><span class="sxs-lookup"><span data-stu-id="6d462-116">Notes</span></span> <br/>          | <span data-ttu-id="6d462-117">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="6d462-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6d462-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="6d462-118">Structure Content</span></span>

<span data-ttu-id="6d462-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="6d462-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart">
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

## <a name="structure-properties"></a><span data-ttu-id="6d462-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="6d462-120">Structure Properties</span></span>

<span data-ttu-id="6d462-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="6d462-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6d462-122">屬性</span><span class="sxs-lookup"><span data-stu-id="6d462-122">Property</span></span>                | <span data-ttu-id="6d462-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6d462-123">xsi:type</span></span>           | <span data-ttu-id="6d462-124">值</span><span class="sxs-lookup"><span data-stu-id="6d462-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6d462-125">DataType</span><span class="sxs-lookup"><span data-stu-id="6d462-125">DataType</span></span><br/>     | <span data-ttu-id="6d462-126">字串</span><span class="sxs-lookup"><span data-stu-id="6d462-126">string</span></span><br/>  | <span data-ttu-id="6d462-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6d462-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="6d462-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6d462-128">DefaultValue</span></span><br/> | <span data-ttu-id="6d462-129">字串</span><span class="sxs-lookup"><span data-stu-id="6d462-129">string</span></span><br/>  | <span data-ttu-id="6d462-130">未定義</span><span class="sxs-lookup"><span data-stu-id="6d462-130">undefined</span></span><br/>       |
| <span data-ttu-id="6d462-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6d462-131">MaxValue</span></span><br/>     | <span data-ttu-id="6d462-132">整數</span><span class="sxs-lookup"><span data-stu-id="6d462-132">integer</span></span><br/> | <span data-ttu-id="6d462-133">100</span><span class="sxs-lookup"><span data-stu-id="6d462-133">100</span></span><br/>             |
| <span data-ttu-id="6d462-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="6d462-134">MinValue</span></span><br/>     | <span data-ttu-id="6d462-135">整數</span><span class="sxs-lookup"><span data-stu-id="6d462-135">integer</span></span><br/> | <span data-ttu-id="6d462-136">0</span><span class="sxs-lookup"><span data-stu-id="6d462-136">0</span></span><br/>               |
| <span data-ttu-id="6d462-137">多個</span><span class="sxs-lookup"><span data-stu-id="6d462-137">Multiple</span></span><br/>     | <span data-ttu-id="6d462-138">整數</span><span class="sxs-lookup"><span data-stu-id="6d462-138">integer</span></span><br/> | <span data-ttu-id="6d462-139">1</span><span class="sxs-lookup"><span data-stu-id="6d462-139">1</span></span><br/>               |
| <span data-ttu-id="6d462-140">強制性</span><span class="sxs-lookup"><span data-stu-id="6d462-140">Mandatory</span></span><br/>    | <span data-ttu-id="6d462-141">string</span><span class="sxs-lookup"><span data-stu-id="6d462-141">string</span></span><br/>  | <span data-ttu-id="6d462-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="6d462-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6d462-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="6d462-143">UnitType</span></span><br/>     | <span data-ttu-id="6d462-144">string</span><span class="sxs-lookup"><span data-stu-id="6d462-144">string</span></span><br/>  | <span data-ttu-id="6d462-145">percent</span><span class="sxs-lookup"><span data-stu-id="6d462-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="6d462-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d462-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d462-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="6d462-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




