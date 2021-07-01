---
description: 深入瞭解 PageBlackGenerationProcessingBlackInkLimit 參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c753554b240a5fef0012a81c533b6efe938075e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118423"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="5fb79-105">PageBlackGenerationProcessingBlackInkLimit</span><span class="sxs-lookup"><span data-stu-id="5fb79-105">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="5fb79-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="5fb79-106">This topic is not current.</span></span> <span data-ttu-id="5fb79-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="5fb79-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5fb79-108">以指定的命名色彩標記的應用程式內容，必須出現在所有色彩分隔上。</span><span class="sxs-lookup"><span data-stu-id="5fb79-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="5fb79-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5fb79-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5fb79-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="5fb79-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5fb79-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5fb79-111">Element Information</span></span>



| <span data-ttu-id="5fb79-112">Name</span><span class="sxs-lookup"><span data-stu-id="5fb79-112">Name</span></span> | <span data-ttu-id="5fb79-113">值</span><span class="sxs-lookup"><span data-stu-id="5fb79-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="5fb79-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="5fb79-114">Element Type</span></span> <br/>   | <span data-ttu-id="5fb79-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5fb79-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="5fb79-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="5fb79-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5fb79-117">頁面</span><span class="sxs-lookup"><span data-stu-id="5fb79-117">Page</span></span><br/>                                            |
| <span data-ttu-id="5fb79-118">備註</span><span class="sxs-lookup"><span data-stu-id="5fb79-118">Notes</span></span> <br/>          | <span data-ttu-id="5fb79-119">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="5fb79-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5fb79-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="5fb79-120">Structure Content</span></span>

<span data-ttu-id="5fb79-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="5fb79-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingBlackInkLimit">
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

## <a name="structure-properties"></a><span data-ttu-id="5fb79-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="5fb79-122">Structure Properties</span></span>

<span data-ttu-id="5fb79-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="5fb79-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5fb79-124">屬性</span><span class="sxs-lookup"><span data-stu-id="5fb79-124">Property</span></span>                | <span data-ttu-id="5fb79-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5fb79-125">xsi:type</span></span>           | <span data-ttu-id="5fb79-126">值</span><span class="sxs-lookup"><span data-stu-id="5fb79-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5fb79-127">DataType</span><span class="sxs-lookup"><span data-stu-id="5fb79-127">DataType</span></span><br/>     | <span data-ttu-id="5fb79-128">字串</span><span class="sxs-lookup"><span data-stu-id="5fb79-128">string</span></span><br/>  | <span data-ttu-id="5fb79-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5fb79-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="5fb79-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5fb79-130">DefaultValue</span></span><br/> | <span data-ttu-id="5fb79-131">字串</span><span class="sxs-lookup"><span data-stu-id="5fb79-131">string</span></span><br/>  | <span data-ttu-id="5fb79-132">未定義</span><span class="sxs-lookup"><span data-stu-id="5fb79-132">undefined</span></span><br/>       |
| <span data-ttu-id="5fb79-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5fb79-133">MaxValue</span></span><br/>     | <span data-ttu-id="5fb79-134">整數</span><span class="sxs-lookup"><span data-stu-id="5fb79-134">integer</span></span><br/> | <span data-ttu-id="5fb79-135">100</span><span class="sxs-lookup"><span data-stu-id="5fb79-135">100</span></span><br/>             |
| <span data-ttu-id="5fb79-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="5fb79-136">MinValue</span></span><br/>     | <span data-ttu-id="5fb79-137">整數</span><span class="sxs-lookup"><span data-stu-id="5fb79-137">integer</span></span><br/> | <span data-ttu-id="5fb79-138">0</span><span class="sxs-lookup"><span data-stu-id="5fb79-138">0</span></span><br/>               |
| <span data-ttu-id="5fb79-139">多個</span><span class="sxs-lookup"><span data-stu-id="5fb79-139">Multiple</span></span><br/>     | <span data-ttu-id="5fb79-140">整數</span><span class="sxs-lookup"><span data-stu-id="5fb79-140">integer</span></span><br/> | <span data-ttu-id="5fb79-141">1</span><span class="sxs-lookup"><span data-stu-id="5fb79-141">1</span></span><br/>               |
| <span data-ttu-id="5fb79-142">強制性</span><span class="sxs-lookup"><span data-stu-id="5fb79-142">Mandatory</span></span><br/>    | <span data-ttu-id="5fb79-143">string</span><span class="sxs-lookup"><span data-stu-id="5fb79-143">string</span></span><br/>  | <span data-ttu-id="5fb79-144">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="5fb79-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5fb79-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="5fb79-145">UnitType</span></span><br/>     | <span data-ttu-id="5fb79-146">string</span><span class="sxs-lookup"><span data-stu-id="5fb79-146">string</span></span><br/>  | <span data-ttu-id="5fb79-147">percent</span><span class="sxs-lookup"><span data-stu-id="5fb79-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5fb79-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="5fb79-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fb79-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="5fb79-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




