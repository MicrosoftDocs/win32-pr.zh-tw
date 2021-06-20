---
description: 深入瞭解 PageBlackGenerationProcessingTotalInkCoverageLimit 元素，其指定影像中任何位置的四個筆墨涵蓋範圍的最大允許總和。
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68410cabdfafa5ce82450821e4ae45709ee8d4c9
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408441"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="29c0d-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="29c0d-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="29c0d-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="29c0d-104">This topic is not current.</span></span> <span data-ttu-id="29c0d-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="29c0d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="29c0d-106">指定影像中任何位置的四個筆墨涵蓋範圍最大允許總和。</span><span class="sxs-lookup"><span data-stu-id="29c0d-106">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="29c0d-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="29c0d-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="29c0d-108">結構內容</span><span class="sxs-lookup"><span data-stu-id="29c0d-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="29c0d-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="29c0d-109">Element Information</span></span>



| <span data-ttu-id="29c0d-110">Name</span><span class="sxs-lookup"><span data-stu-id="29c0d-110">Name</span></span> | <span data-ttu-id="29c0d-111">值</span><span class="sxs-lookup"><span data-stu-id="29c0d-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="29c0d-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="29c0d-112">Element Type</span></span> <br/>   | <span data-ttu-id="29c0d-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="29c0d-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="29c0d-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="29c0d-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="29c0d-115">頁面</span><span class="sxs-lookup"><span data-stu-id="29c0d-115">Page</span></span><br/>                                            |
| <span data-ttu-id="29c0d-116">備註</span><span class="sxs-lookup"><span data-stu-id="29c0d-116">Notes</span></span> <br/>          | <span data-ttu-id="29c0d-117">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="29c0d-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="29c0d-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="29c0d-118">Structure Content</span></span>

<span data-ttu-id="29c0d-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="29c0d-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="29c0d-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="29c0d-120">Structure Properties</span></span>

<span data-ttu-id="29c0d-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="29c0d-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="29c0d-122">屬性</span><span class="sxs-lookup"><span data-stu-id="29c0d-122">Property</span></span>                | <span data-ttu-id="29c0d-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="29c0d-123">xsi:type</span></span>           | <span data-ttu-id="29c0d-124">值</span><span class="sxs-lookup"><span data-stu-id="29c0d-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="29c0d-125">DataType</span><span class="sxs-lookup"><span data-stu-id="29c0d-125">DataType</span></span><br/>     | <span data-ttu-id="29c0d-126">字串</span><span class="sxs-lookup"><span data-stu-id="29c0d-126">string</span></span><br/>  | <span data-ttu-id="29c0d-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="29c0d-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="29c0d-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="29c0d-128">DefaultValue</span></span><br/> | <span data-ttu-id="29c0d-129">字串</span><span class="sxs-lookup"><span data-stu-id="29c0d-129">string</span></span><br/>  | <span data-ttu-id="29c0d-130">未定義</span><span class="sxs-lookup"><span data-stu-id="29c0d-130">undefined</span></span><br/>       |
| <span data-ttu-id="29c0d-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="29c0d-131">MaxValue</span></span><br/>     | <span data-ttu-id="29c0d-132">整數</span><span class="sxs-lookup"><span data-stu-id="29c0d-132">integer</span></span><br/> | <span data-ttu-id="29c0d-133">400</span><span class="sxs-lookup"><span data-stu-id="29c0d-133">400</span></span><br/>             |
| <span data-ttu-id="29c0d-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="29c0d-134">MinValue</span></span><br/>     | <span data-ttu-id="29c0d-135">整數</span><span class="sxs-lookup"><span data-stu-id="29c0d-135">integer</span></span><br/> | <span data-ttu-id="29c0d-136">200</span><span class="sxs-lookup"><span data-stu-id="29c0d-136">200</span></span><br/>             |
| <span data-ttu-id="29c0d-137">多個</span><span class="sxs-lookup"><span data-stu-id="29c0d-137">Multiple</span></span><br/>     | <span data-ttu-id="29c0d-138">整數</span><span class="sxs-lookup"><span data-stu-id="29c0d-138">integer</span></span><br/> | <span data-ttu-id="29c0d-139">1</span><span class="sxs-lookup"><span data-stu-id="29c0d-139">1</span></span><br/>               |
| <span data-ttu-id="29c0d-140">強制性</span><span class="sxs-lookup"><span data-stu-id="29c0d-140">Mandatory</span></span><br/>    | <span data-ttu-id="29c0d-141">string</span><span class="sxs-lookup"><span data-stu-id="29c0d-141">string</span></span><br/>  | <span data-ttu-id="29c0d-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="29c0d-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="29c0d-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="29c0d-143">UnitType</span></span><br/>     | <span data-ttu-id="29c0d-144">string</span><span class="sxs-lookup"><span data-stu-id="29c0d-144">string</span></span><br/>  | <span data-ttu-id="29c0d-145">percent</span><span class="sxs-lookup"><span data-stu-id="29c0d-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="29c0d-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="29c0d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29c0d-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="29c0d-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




