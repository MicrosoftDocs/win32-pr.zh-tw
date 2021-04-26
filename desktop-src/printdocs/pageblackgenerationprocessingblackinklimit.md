---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3052d8cec8fd46c2f7607e6366aa6868cccbdbda
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996185"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="9c28d-104">PageBlackGenerationProcessingBlackInkLimit</span><span class="sxs-lookup"><span data-stu-id="9c28d-104">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="9c28d-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="9c28d-105">This topic is not current.</span></span> <span data-ttu-id="9c28d-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="9c28d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9c28d-107">以指定的命名色彩標記的應用程式內容，必須出現在所有色彩分隔上。</span><span class="sxs-lookup"><span data-stu-id="9c28d-107">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="9c28d-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9c28d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9c28d-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="9c28d-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="9c28d-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9c28d-110">Element Information</span></span>



| <span data-ttu-id="9c28d-111">Name</span><span class="sxs-lookup"><span data-stu-id="9c28d-111">Name</span></span> | <span data-ttu-id="9c28d-112">值</span><span class="sxs-lookup"><span data-stu-id="9c28d-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="9c28d-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="9c28d-113">Element Type</span></span> <br/>   | <span data-ttu-id="9c28d-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9c28d-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="9c28d-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="9c28d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9c28d-116">頁面</span><span class="sxs-lookup"><span data-stu-id="9c28d-116">Page</span></span><br/>                                            |
| <span data-ttu-id="9c28d-117">備註</span><span class="sxs-lookup"><span data-stu-id="9c28d-117">Notes</span></span> <br/>          | <span data-ttu-id="9c28d-118">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="9c28d-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="9c28d-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="9c28d-119">Structure Content</span></span>

<span data-ttu-id="9c28d-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="9c28d-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="9c28d-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="9c28d-121">Structure Properties</span></span>

<span data-ttu-id="9c28d-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="9c28d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9c28d-123">屬性</span><span class="sxs-lookup"><span data-stu-id="9c28d-123">Property</span></span>                | <span data-ttu-id="9c28d-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9c28d-124">xsi:type</span></span>           | <span data-ttu-id="9c28d-125">值</span><span class="sxs-lookup"><span data-stu-id="9c28d-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="9c28d-126">DataType</span><span class="sxs-lookup"><span data-stu-id="9c28d-126">DataType</span></span><br/>     | <span data-ttu-id="9c28d-127">字串</span><span class="sxs-lookup"><span data-stu-id="9c28d-127">string</span></span><br/>  | <span data-ttu-id="9c28d-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9c28d-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="9c28d-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9c28d-129">DefaultValue</span></span><br/> | <span data-ttu-id="9c28d-130">字串</span><span class="sxs-lookup"><span data-stu-id="9c28d-130">string</span></span><br/>  | <span data-ttu-id="9c28d-131">未定義</span><span class="sxs-lookup"><span data-stu-id="9c28d-131">undefined</span></span><br/>       |
| <span data-ttu-id="9c28d-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="9c28d-132">MaxValue</span></span><br/>     | <span data-ttu-id="9c28d-133">整數</span><span class="sxs-lookup"><span data-stu-id="9c28d-133">integer</span></span><br/> | <span data-ttu-id="9c28d-134">100</span><span class="sxs-lookup"><span data-stu-id="9c28d-134">100</span></span><br/>             |
| <span data-ttu-id="9c28d-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="9c28d-135">MinValue</span></span><br/>     | <span data-ttu-id="9c28d-136">整數</span><span class="sxs-lookup"><span data-stu-id="9c28d-136">integer</span></span><br/> | <span data-ttu-id="9c28d-137">0</span><span class="sxs-lookup"><span data-stu-id="9c28d-137">0</span></span><br/>               |
| <span data-ttu-id="9c28d-138">多個</span><span class="sxs-lookup"><span data-stu-id="9c28d-138">Multiple</span></span><br/>     | <span data-ttu-id="9c28d-139">整數</span><span class="sxs-lookup"><span data-stu-id="9c28d-139">integer</span></span><br/> | <span data-ttu-id="9c28d-140">1</span><span class="sxs-lookup"><span data-stu-id="9c28d-140">1</span></span><br/>               |
| <span data-ttu-id="9c28d-141">強制性</span><span class="sxs-lookup"><span data-stu-id="9c28d-141">Mandatory</span></span><br/>    | <span data-ttu-id="9c28d-142">字串</span><span class="sxs-lookup"><span data-stu-id="9c28d-142">string</span></span><br/>  | <span data-ttu-id="9c28d-143">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="9c28d-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="9c28d-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="9c28d-144">UnitType</span></span><br/>     | <span data-ttu-id="9c28d-145">字串</span><span class="sxs-lookup"><span data-stu-id="9c28d-145">string</span></span><br/>  | <span data-ttu-id="9c28d-146">percent</span><span class="sxs-lookup"><span data-stu-id="9c28d-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="9c28d-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c28d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c28d-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="9c28d-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




