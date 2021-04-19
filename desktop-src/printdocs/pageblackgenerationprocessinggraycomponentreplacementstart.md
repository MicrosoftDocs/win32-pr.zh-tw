---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dedf425cd31dd83bce877358c456d1cd16183fa
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106993801"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="3796e-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="3796e-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="3796e-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="3796e-105">This topic is not current.</span></span> <span data-ttu-id="3796e-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="3796e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3796e-107">描述「反白顯示陰影」範圍中的點，其中 GCR 應開始 (100% 的最深陰影) 。</span><span class="sxs-lookup"><span data-stu-id="3796e-107">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="3796e-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3796e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3796e-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="3796e-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3796e-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3796e-110">Element Information</span></span>



| <span data-ttu-id="3796e-111">Name</span><span class="sxs-lookup"><span data-stu-id="3796e-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="3796e-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="3796e-112">Element Type</span></span> <br/>   | <span data-ttu-id="3796e-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3796e-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="3796e-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="3796e-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3796e-115">頁面</span><span class="sxs-lookup"><span data-stu-id="3796e-115">Page</span></span><br/>                                            |
| <span data-ttu-id="3796e-116">備註</span><span class="sxs-lookup"><span data-stu-id="3796e-116">Notes</span></span> <br/>          | <span data-ttu-id="3796e-117">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="3796e-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3796e-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="3796e-118">Structure Content</span></span>

<span data-ttu-id="3796e-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="3796e-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3796e-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="3796e-120">Structure Properties</span></span>

<span data-ttu-id="3796e-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="3796e-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3796e-122">屬性</span><span class="sxs-lookup"><span data-stu-id="3796e-122">Property</span></span>                | <span data-ttu-id="3796e-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3796e-123">xsi:type</span></span>           | <span data-ttu-id="3796e-124">值</span><span class="sxs-lookup"><span data-stu-id="3796e-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3796e-125">DataType</span><span class="sxs-lookup"><span data-stu-id="3796e-125">DataType</span></span><br/>     | <span data-ttu-id="3796e-126">字串</span><span class="sxs-lookup"><span data-stu-id="3796e-126">string</span></span><br/>  | <span data-ttu-id="3796e-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3796e-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="3796e-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3796e-128">DefaultValue</span></span><br/> | <span data-ttu-id="3796e-129">字串</span><span class="sxs-lookup"><span data-stu-id="3796e-129">string</span></span><br/>  | <span data-ttu-id="3796e-130">未定義</span><span class="sxs-lookup"><span data-stu-id="3796e-130">undefined</span></span><br/>       |
| <span data-ttu-id="3796e-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="3796e-131">MaxValue</span></span><br/>     | <span data-ttu-id="3796e-132">整數</span><span class="sxs-lookup"><span data-stu-id="3796e-132">integer</span></span><br/> | <span data-ttu-id="3796e-133">100</span><span class="sxs-lookup"><span data-stu-id="3796e-133">100</span></span><br/>             |
| <span data-ttu-id="3796e-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="3796e-134">MinValue</span></span><br/>     | <span data-ttu-id="3796e-135">整數</span><span class="sxs-lookup"><span data-stu-id="3796e-135">integer</span></span><br/> | <span data-ttu-id="3796e-136">0</span><span class="sxs-lookup"><span data-stu-id="3796e-136">0</span></span><br/>               |
| <span data-ttu-id="3796e-137">多個</span><span class="sxs-lookup"><span data-stu-id="3796e-137">Multiple</span></span><br/>     | <span data-ttu-id="3796e-138">整數</span><span class="sxs-lookup"><span data-stu-id="3796e-138">integer</span></span><br/> | <span data-ttu-id="3796e-139">1</span><span class="sxs-lookup"><span data-stu-id="3796e-139">1</span></span><br/>               |
| <span data-ttu-id="3796e-140">強制性</span><span class="sxs-lookup"><span data-stu-id="3796e-140">Mandatory</span></span><br/>    | <span data-ttu-id="3796e-141">字串</span><span class="sxs-lookup"><span data-stu-id="3796e-141">string</span></span><br/>  | <span data-ttu-id="3796e-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="3796e-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3796e-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="3796e-143">UnitType</span></span><br/>     | <span data-ttu-id="3796e-144">字串</span><span class="sxs-lookup"><span data-stu-id="3796e-144">string</span></span><br/>  | <span data-ttu-id="3796e-145">percent</span><span class="sxs-lookup"><span data-stu-id="3796e-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="3796e-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="3796e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3796e-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="3796e-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




