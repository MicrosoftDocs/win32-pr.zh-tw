---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f565b6190f9bda11727efde6e799b6fb979cecc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986029"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="9f822-104">PageBlackGenerationProcessingBlackInkLimit</span><span class="sxs-lookup"><span data-stu-id="9f822-104">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="9f822-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="9f822-105">This topic is not current.</span></span> <span data-ttu-id="9f822-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="9f822-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9f822-107">以指定的命名色彩標記的應用程式內容，必須出現在所有色彩分隔上。</span><span class="sxs-lookup"><span data-stu-id="9f822-107">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="9f822-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9f822-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9f822-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="9f822-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="9f822-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9f822-110">Element Information</span></span>



| <span data-ttu-id="9f822-111">Name</span><span class="sxs-lookup"><span data-stu-id="9f822-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="9f822-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="9f822-112">Element Type</span></span> <br/>   | <span data-ttu-id="9f822-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9f822-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="9f822-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="9f822-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9f822-115">頁面</span><span class="sxs-lookup"><span data-stu-id="9f822-115">Page</span></span><br/>                                            |
| <span data-ttu-id="9f822-116">備註</span><span class="sxs-lookup"><span data-stu-id="9f822-116">Notes</span></span> <br/>          | <span data-ttu-id="9f822-117">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="9f822-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="9f822-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="9f822-118">Structure Content</span></span>

<span data-ttu-id="9f822-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="9f822-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="9f822-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="9f822-120">Structure Properties</span></span>

<span data-ttu-id="9f822-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="9f822-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9f822-122">屬性</span><span class="sxs-lookup"><span data-stu-id="9f822-122">Property</span></span>                | <span data-ttu-id="9f822-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9f822-123">xsi:type</span></span>           | <span data-ttu-id="9f822-124">值</span><span class="sxs-lookup"><span data-stu-id="9f822-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="9f822-125">DataType</span><span class="sxs-lookup"><span data-stu-id="9f822-125">DataType</span></span><br/>     | <span data-ttu-id="9f822-126">字串</span><span class="sxs-lookup"><span data-stu-id="9f822-126">string</span></span><br/>  | <span data-ttu-id="9f822-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9f822-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="9f822-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9f822-128">DefaultValue</span></span><br/> | <span data-ttu-id="9f822-129">字串</span><span class="sxs-lookup"><span data-stu-id="9f822-129">string</span></span><br/>  | <span data-ttu-id="9f822-130">未定義</span><span class="sxs-lookup"><span data-stu-id="9f822-130">undefined</span></span><br/>       |
| <span data-ttu-id="9f822-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="9f822-131">MaxValue</span></span><br/>     | <span data-ttu-id="9f822-132">整數</span><span class="sxs-lookup"><span data-stu-id="9f822-132">integer</span></span><br/> | <span data-ttu-id="9f822-133">100</span><span class="sxs-lookup"><span data-stu-id="9f822-133">100</span></span><br/>             |
| <span data-ttu-id="9f822-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="9f822-134">MinValue</span></span><br/>     | <span data-ttu-id="9f822-135">整數</span><span class="sxs-lookup"><span data-stu-id="9f822-135">integer</span></span><br/> | <span data-ttu-id="9f822-136">0</span><span class="sxs-lookup"><span data-stu-id="9f822-136">0</span></span><br/>               |
| <span data-ttu-id="9f822-137">多個</span><span class="sxs-lookup"><span data-stu-id="9f822-137">Multiple</span></span><br/>     | <span data-ttu-id="9f822-138">整數</span><span class="sxs-lookup"><span data-stu-id="9f822-138">integer</span></span><br/> | <span data-ttu-id="9f822-139">1</span><span class="sxs-lookup"><span data-stu-id="9f822-139">1</span></span><br/>               |
| <span data-ttu-id="9f822-140">強制性</span><span class="sxs-lookup"><span data-stu-id="9f822-140">Mandatory</span></span><br/>    | <span data-ttu-id="9f822-141">字串</span><span class="sxs-lookup"><span data-stu-id="9f822-141">string</span></span><br/>  | <span data-ttu-id="9f822-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="9f822-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="9f822-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="9f822-143">UnitType</span></span><br/>     | <span data-ttu-id="9f822-144">字串</span><span class="sxs-lookup"><span data-stu-id="9f822-144">string</span></span><br/>  | <span data-ttu-id="9f822-145">percent</span><span class="sxs-lookup"><span data-stu-id="9f822-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="9f822-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f822-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f822-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="9f822-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




