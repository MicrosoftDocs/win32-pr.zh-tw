---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29918bfe48d1547a3c61b8d79425b36368f6d249
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993875"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="1b218-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="1b218-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="1b218-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="1b218-105">This topic is not current.</span></span> <span data-ttu-id="1b218-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="1b218-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1b218-107">指定影像中任何位置的四個筆墨涵蓋範圍最大允許總和。</span><span class="sxs-lookup"><span data-stu-id="1b218-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="1b218-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1b218-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1b218-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="1b218-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1b218-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1b218-110">Element Information</span></span>



| <span data-ttu-id="1b218-111">Name</span><span class="sxs-lookup"><span data-stu-id="1b218-111">Name</span></span> | <span data-ttu-id="1b218-112">值</span><span class="sxs-lookup"><span data-stu-id="1b218-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="1b218-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="1b218-113">Element Type</span></span> <br/>   | <span data-ttu-id="1b218-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1b218-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="1b218-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="1b218-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1b218-116">頁面</span><span class="sxs-lookup"><span data-stu-id="1b218-116">Page</span></span><br/>                                            |
| <span data-ttu-id="1b218-117">備註</span><span class="sxs-lookup"><span data-stu-id="1b218-117">Notes</span></span> <br/>          | <span data-ttu-id="1b218-118">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="1b218-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1b218-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="1b218-119">Structure Content</span></span>

<span data-ttu-id="1b218-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="1b218-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1b218-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="1b218-121">Structure Properties</span></span>

<span data-ttu-id="1b218-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="1b218-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1b218-123">屬性</span><span class="sxs-lookup"><span data-stu-id="1b218-123">Property</span></span>                | <span data-ttu-id="1b218-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1b218-124">xsi:type</span></span>           | <span data-ttu-id="1b218-125">值</span><span class="sxs-lookup"><span data-stu-id="1b218-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1b218-126">DataType</span><span class="sxs-lookup"><span data-stu-id="1b218-126">DataType</span></span><br/>     | <span data-ttu-id="1b218-127">字串</span><span class="sxs-lookup"><span data-stu-id="1b218-127">string</span></span><br/>  | <span data-ttu-id="1b218-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1b218-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="1b218-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1b218-129">DefaultValue</span></span><br/> | <span data-ttu-id="1b218-130">字串</span><span class="sxs-lookup"><span data-stu-id="1b218-130">string</span></span><br/>  | <span data-ttu-id="1b218-131">未定義</span><span class="sxs-lookup"><span data-stu-id="1b218-131">undefined</span></span><br/>       |
| <span data-ttu-id="1b218-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1b218-132">MaxValue</span></span><br/>     | <span data-ttu-id="1b218-133">整數</span><span class="sxs-lookup"><span data-stu-id="1b218-133">integer</span></span><br/> | <span data-ttu-id="1b218-134">400</span><span class="sxs-lookup"><span data-stu-id="1b218-134">400</span></span><br/>             |
| <span data-ttu-id="1b218-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="1b218-135">MinValue</span></span><br/>     | <span data-ttu-id="1b218-136">整數</span><span class="sxs-lookup"><span data-stu-id="1b218-136">integer</span></span><br/> | <span data-ttu-id="1b218-137">200</span><span class="sxs-lookup"><span data-stu-id="1b218-137">200</span></span><br/>             |
| <span data-ttu-id="1b218-138">多個</span><span class="sxs-lookup"><span data-stu-id="1b218-138">Multiple</span></span><br/>     | <span data-ttu-id="1b218-139">整數</span><span class="sxs-lookup"><span data-stu-id="1b218-139">integer</span></span><br/> | <span data-ttu-id="1b218-140">1</span><span class="sxs-lookup"><span data-stu-id="1b218-140">1</span></span><br/>               |
| <span data-ttu-id="1b218-141">強制性</span><span class="sxs-lookup"><span data-stu-id="1b218-141">Mandatory</span></span><br/>    | <span data-ttu-id="1b218-142">字串</span><span class="sxs-lookup"><span data-stu-id="1b218-142">string</span></span><br/>  | <span data-ttu-id="1b218-143">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="1b218-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1b218-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="1b218-144">UnitType</span></span><br/>     | <span data-ttu-id="1b218-145">字串</span><span class="sxs-lookup"><span data-stu-id="1b218-145">string</span></span><br/>  | <span data-ttu-id="1b218-146">percent</span><span class="sxs-lookup"><span data-stu-id="1b218-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1b218-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="1b218-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b218-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="1b218-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




