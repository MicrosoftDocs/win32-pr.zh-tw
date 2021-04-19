---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07566926c2115855ea7321af90e7d1caebcd0a82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "107000534"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="2b0a1-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="2b0a1-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="2b0a1-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="2b0a1-105">This topic is not current.</span></span> <span data-ttu-id="2b0a1-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="2b0a1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2b0a1-107">指定影像中任何位置的四個筆墨涵蓋範圍最大允許總和。</span><span class="sxs-lookup"><span data-stu-id="2b0a1-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="2b0a1-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2b0a1-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2b0a1-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="2b0a1-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2b0a1-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2b0a1-110">Element Information</span></span>



| <span data-ttu-id="2b0a1-111">Name</span><span class="sxs-lookup"><span data-stu-id="2b0a1-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="2b0a1-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="2b0a1-112">Element Type</span></span> <br/>   | <span data-ttu-id="2b0a1-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2b0a1-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="2b0a1-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="2b0a1-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2b0a1-115">頁面</span><span class="sxs-lookup"><span data-stu-id="2b0a1-115">Page</span></span><br/>                                            |
| <span data-ttu-id="2b0a1-116">備註</span><span class="sxs-lookup"><span data-stu-id="2b0a1-116">Notes</span></span> <br/>          | <span data-ttu-id="2b0a1-117">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="2b0a1-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2b0a1-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="2b0a1-118">Structure Content</span></span>

<span data-ttu-id="2b0a1-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="2b0a1-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">200</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="2b0a1-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="2b0a1-120">Structure Properties</span></span>

<span data-ttu-id="2b0a1-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="2b0a1-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2b0a1-122">屬性</span><span class="sxs-lookup"><span data-stu-id="2b0a1-122">Property</span></span>                | <span data-ttu-id="2b0a1-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2b0a1-123">xsi:type</span></span>           | <span data-ttu-id="2b0a1-124">值</span><span class="sxs-lookup"><span data-stu-id="2b0a1-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="2b0a1-125">DataType</span><span class="sxs-lookup"><span data-stu-id="2b0a1-125">DataType</span></span><br/>     | <span data-ttu-id="2b0a1-126">字串</span><span class="sxs-lookup"><span data-stu-id="2b0a1-126">string</span></span><br/>  | <span data-ttu-id="2b0a1-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2b0a1-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="2b0a1-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2b0a1-128">DefaultValue</span></span><br/> | <span data-ttu-id="2b0a1-129">字串</span><span class="sxs-lookup"><span data-stu-id="2b0a1-129">string</span></span><br/>  | <span data-ttu-id="2b0a1-130">未定義</span><span class="sxs-lookup"><span data-stu-id="2b0a1-130">undefined</span></span><br/>       |
| <span data-ttu-id="2b0a1-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="2b0a1-131">MaxValue</span></span><br/>     | <span data-ttu-id="2b0a1-132">整數</span><span class="sxs-lookup"><span data-stu-id="2b0a1-132">integer</span></span><br/> | <span data-ttu-id="2b0a1-133">400</span><span class="sxs-lookup"><span data-stu-id="2b0a1-133">400</span></span><br/>             |
| <span data-ttu-id="2b0a1-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="2b0a1-134">MinValue</span></span><br/>     | <span data-ttu-id="2b0a1-135">整數</span><span class="sxs-lookup"><span data-stu-id="2b0a1-135">integer</span></span><br/> | <span data-ttu-id="2b0a1-136">200</span><span class="sxs-lookup"><span data-stu-id="2b0a1-136">200</span></span><br/>             |
| <span data-ttu-id="2b0a1-137">多個</span><span class="sxs-lookup"><span data-stu-id="2b0a1-137">Multiple</span></span><br/>     | <span data-ttu-id="2b0a1-138">整數</span><span class="sxs-lookup"><span data-stu-id="2b0a1-138">integer</span></span><br/> | <span data-ttu-id="2b0a1-139">1</span><span class="sxs-lookup"><span data-stu-id="2b0a1-139">1</span></span><br/>               |
| <span data-ttu-id="2b0a1-140">強制性</span><span class="sxs-lookup"><span data-stu-id="2b0a1-140">Mandatory</span></span><br/>    | <span data-ttu-id="2b0a1-141">字串</span><span class="sxs-lookup"><span data-stu-id="2b0a1-141">string</span></span><br/>  | <span data-ttu-id="2b0a1-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="2b0a1-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="2b0a1-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="2b0a1-143">UnitType</span></span><br/>     | <span data-ttu-id="2b0a1-144">字串</span><span class="sxs-lookup"><span data-stu-id="2b0a1-144">string</span></span><br/>  | <span data-ttu-id="2b0a1-145">percent</span><span class="sxs-lookup"><span data-stu-id="2b0a1-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="2b0a1-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b0a1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b0a1-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="2b0a1-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




